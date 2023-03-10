<p align="center">
	<a><img width="100px" src="https://cdn.jsdelivr.net/gh/flydoos/BYDCarHelper/Images/Logo.png"/></a>
</p>
<p align="center">
	<a href="https://github.com/flydoos/BYDCarHelper/issues"><img alt="GitHub issues" src="https://img.shields.io/github/issues/flydoos/BYDCarHelper?style=flat-square"></a>
	<a href="https://www.microsoft.com/zh-cn/download/confirmation.aspx?id=17718"><img src="https://img.shields.io/badge/platform-windows-lightgrey.svg?style=flat-square"/></a>
	<a href="https://github.com/flydoos/BYDCarHelper/stargazers"><img alt="GitHub stars" src="https://img.shields.io/github/stars/flydoos/BYDCarHelper?style=flat-square"></a>
	<a href="https://github.com/flydoos/BYDCarHelper/tags"><img alt="GitHub tag (latest by date)" src="https://img.shields.io/github/v/tag/flydoos/BYDCarHelper?style=flat-square"></a>
	<a href="https://github.com/flydoos/BYDCarHelper/releases"><img src="https://img.shields.io/github/downloads/flydoos/BYDCarHelper/total.svg?style=flat-square"/></a>
</p>
<p align="center">
	<img src="https://cdn.jsdelivr.net/gh/flydoos/BYDCarHelper/Images/ClickStar.png"/>
</p>

# 👀比亚迪车辆助手PC版

比亚迪车辆助手PC版（BYDCarHelper）由“牛A与牛C之间”开发制作，这是一款Windows电脑软件，可实现智能上电、智能锁车、远程控制，以及自动同步比亚迪车况信息，例如：车型、车牌号、总里程、总续航、剩余电量、剩余电量续航里程、剩余油量、剩余油量续航里程、最近50公里平均能耗、累计平均能耗、OK指示灯、整车状态、四个车轮胎压等等，而且可以自动生成“最近7天能耗趋势图、最近7天能续航趋势图、最近7天能总里程趋势图”，解决以往只有车机才能看到这些统计报表的问题，以上数据可以通过钉钉/飞书群机器人，自动推送到你的手机/PC钉钉或飞书查看，**支持比亚迪大部分车型**。

别名：比亚迪车辆助手、比亚迪汽车助手、比亚迪车况助手

## 🖥️主要功能

1. 支持车况信息同步（大部分信息都支持）
2. 支持统计报表（自动生成“能耗趋势图、续航趋势图、总里程趋势图”）
3. 支持钉钉群机器人，自动推送到你的手机/PC钉钉查看
4. 支持飞书群机器人，自动推送到你的手机/PC飞书查看
5. 支持免打扰功能（如果最新数据与上次相同，或者车辆不是熄灭状态，将不会推送到钉钉/飞书群，避免骚扰用户）
6. 支持自动获取比亚迪Cookie（不需要抓包，且支持自动续期Cookie，支持Cookie WebHook与其它设备共享）
7. 支持远程控制（例如：车门上锁、车门解锁、关闭车窗、开启空调、关闭空调、闪灯鸣笛、闪灯）
8. 支持智能上电（当车辆发生解锁时、或者解锁+主驾车门打开时，将会自动远程启动）
9. 支持智能锁车（当车辆熄火，也就是关闭电源时，且车辆处于解锁状态，持续几分钟未变化，将会自动上锁+关闭车窗）
10. 支持程序启动后自动开启上次的智能任务（例如：智能上电、智能锁车，且会最小化到系统托盘系统）

## 📌前置条件

**如何操作，可以查看教程：[FAQ](FAQ.md)**

1. [必选] 获取Cookie：登录PC版微信，打开任意聊天窗口（不可关闭微信主界面，也不可退出微信），通过“比亚迪车辆助手PC版”——设置——自动获取，可以自动获取比亚迪Cookie信息
2. [必选] 自动同步车况：开启“智能上电”或“智能锁车”功能（任意一种），开启后程序将会自动同步数据，不再需要其他额外操作。如果不想开启智能XXX功能，可以结合Windows任务计划程序，进行定时执行。PS：如果你把电脑/本程序关闭，那就没办法同步数据了
3. [可选] 钉钉/飞书消息推送：需要去钉钉/飞书群添加一个Webhook群机器人，并且带加签方式，用于机器人群消息推送
4. [可选] 上传图片：需要在Windows电脑上安装 PicGo + 注册“七牛云”账号（每个月免费10GB够用），通过PicGo上传本地图片到七牛云，这个图片上传功能默认不开启（不开启的话机器人消息无法显示图片）

## 📝令牌续期

大约在2023年1月14日前后，比亚迪官方更新了Cookie规则，导致无法自动获取Cookie。此外，Cookie有效期从以前的1个月有效改成了24小时有效，这个改动导致“比亚迪车辆助手”无法正常使用。这个问题已经2023年1月31日成功解决，现在已经可以自动获取Cookie，也可以自动续期Cookie。

自动续期Cookie原理：采用模拟人工操作的方式，在微信内置浏览器内，定时自动打开比亚迪官方网页，从而实现Cookie续期。所以，当程序自动续期的时候用户不可以进行其他操作，否则可能导致续期失败。

**温馨提示：自动续期比亚迪Cookie功能，需要打开PC版微信的窗口主界面，可以把微信窗口最小化，但是不能关闭（就算是电脑锁屏、待机期间，也不要关闭微信主界面），否则无法自动“获取/续期”Cookie！**

## 🔖主要流程

智能上电+智能锁车主要流程：电源关闭状态下 ——> 车辆解锁 + 打开主驾车门（可选） ——> 智能上电 ——> 开车行驶 ——> 停车手动关闭电源 ——> 车辆解锁 + 持续X分钟 ——> 智能锁车 ——> 进入防盗状态（然后开始下一轮）

## 🔗下载地址
 
**下载地址：[⚡️最新版BYD车辆助手PC版下载](https://github.com/flydoos/BYDCarHelper/releases/latest)**

## 📷截图

![PC端软件截图](https://cdn.jsdelivr.net/gh/flydoos/BYDCarHelper/Images/PC-2.3.0.png)

![PC端软件截图](https://cdn.jsdelivr.net/gh/flydoos/BYDCarHelper/Images/SETTING-2.2.0.png)

## 🔨使用方法

1. 首先，你的系统需要满足以下条件：

    * Windows XP 或更高版本。
    * [.NET Framework 4.0](https://www.microsoft.com/zh-cn/download/confirmation.aspx?id=17718) 或更高版本。**低于此版本在打开程序时可能无反应，或者直接报错**。

2. 以管理员身份运行本程序

3. 由于程序加壳，并且没有购买数字签名证书，**杀毒软件可能会弹出警告，放行即可。**

手机钉钉效果展示：

![手机钉钉截图](https://cdn.jsdelivr.net/gh/flydoos/BYDCarHelper/Images/Mobile-1.3.3.jpg)

## ❓常见问题

常见问题：[《比亚迪车辆助手PC版使用教程（常见问题）》](FAQ.md)

查看教程：[《使用PicGo+七牛云实现图片上传功能（制作自己的图床网站）》](https://www.wuleba.com/?p=1919)

## ❤联系我

QQ群：223541319 （催更请进群）

博客：https://www.cnblogs.com/flydoos

官网：https://www.wuleba.com （2021年国庆的时候网站恢复了，大家去支持下）

对 "BYDCarHelper" 有任何使用上或者技术上的疑问，欢迎随时联系作者。

## 📄开源协议

基于 [木兰宽松许可证（第2版）](http://license.coscl.org.cn/MulanPSL2/) 协议。

## ⚖️免责声明

远程控制、智能化操作等功能涉及车辆安全及人员安全，使用相关功能产生的一切后果需要用户自行承担，使用本程序则表示用户接受此条款。

本程序是作者闲暇之余，方便自己使用而开发的一个小工具。如果对其他人/公司造成不好的影响，请到QQ群联系作者，我会马上删除，谢谢。
