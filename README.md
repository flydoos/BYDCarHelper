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

比亚迪车辆助手PC版（BYDCarHelper）由“牛A与牛C之间”开发制作，这是一款Windows电脑软件，可实现智能上电、智能锁车、远程控制、自动签到，以及自动同步比亚迪车况信息，例如：车型、车牌号、总里程、每日里程、总续航、剩余电量、剩余电量续航里程、剩余油量、剩余油量续航里程、最近50公里平均能耗、累计平均能耗、OK指示灯、整车状态、四个车轮胎压等等，而且可以自动生成“最近7天能耗趋势图、最近7天能续航趋势图、最近7天能总里程趋势图”，解决以往只有车机才能看到这些统计报表的问题，以上数据可以通过钉钉/飞书群机器人，自动推送到你的手机/PC钉钉或飞书查看，**支持比亚迪大部分车型**。

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
11. 支持比亚迪自动签到任务（支持比亚迪王朝、支持比亚迪海洋）

## 📝令牌续期

大约在2023年1月14日前后，比亚迪官方更新了Cookie规则，导致无法自动获取Cookie。此外，Cookie有效期从以前的1个月有效改成了24小时有效，这个改动导致“比亚迪车辆助手”无法正常使用。这个问题已经2023年1月31日成功解决，现在已经可以自动获取Cookie，也可以自动续期Cookie。

自动续期Cookie原理：采用模拟人工操作的方式，在微信内置浏览器内，定时自动打开比亚迪官方网页，从而实现Cookie续期。所以，当程序自动续期的时候用户不可以进行其他操作，否则可能导致续期失败。

## 🔖主要流程

智能上电+智能锁车主要流程：电源关闭状态下 ——> 车辆解锁 + 打开主驾车门（可选） ——> 智能上电 ——> 开车行驶 ——> 停车手动关闭电源 ——> 车辆解锁 + 持续X分钟 ——> 智能锁车 ——> 进入防盗状态（然后开始下一轮）

## 🔗下载地址
 
**下载地址：[⚡️最新版BYD车辆助手PC版下载](https://github.com/flydoos/BYDCarHelper/releases/latest)**

## 📷截图

![PC端软件截图](https://cdn.jsdelivr.net/gh/flydoos/BYDCarHelper/Images/PC-3.0.1.png)

![PC端软件截图](https://cdn.jsdelivr.net/gh/flydoos/BYDCarHelper/Images/SETTING-3.0.1.png)

## 🔨使用方法

1. 需要大家自行准备一台PC电脑，并且安装“最新版”PC微信（**微信版本最低使用3.9.2.26，建议下载官方最新版PC微信**），系统建议Win10或以上版本（最低支持WinXP），并且能保持24小时互联网在线，你的系统需要满足以下条件：

    * Windows XP 或更高版本。
    * [.NET Framework 4.0](https://www.microsoft.com/zh-cn/download/confirmation.aspx?id=17718) 或更高版本。低于此版本在打开程序时可能无反应，或者直接报错。

2. 由于程序加壳，并且没有购买数字签名证书，**杀毒软件可能会弹出警告，放行即可。**

3. 登录PC微信，微信关注“**比亚迪Dilink**”公众号，登录并绑定账号，打开微信任意聊天窗口（**不可关闭微信主界面，也不可退出微信**）

4. 以管理员身份运行本程序，打开“比亚迪车辆助手PC版”的可执行文件BYDCarHelper.exe——设置——自动获取，可以自动获取比亚迪Cookie信息（**首次自动获取，时间可能比较久，如果提示无法获取，可以等待2分钟之后，再点击自动获取**），获取成功后，Cookie会自动填充到文本框中，此时会弹出“获取成功”的提示框。

5. **填写“远程操作密码（6位数字）”**，如果不填写这个远程密码，将无法使用智能上电、智能锁车等功能（注意：很多用户都会写错密码，导致无法智能上电，请务必确保远程操作密码正确）。

6. 关闭“设置”窗口，左下角**开启“智能上电”或“智能锁车”功能**（最少选择1种，也可以全部开启），开启智能XXX任务后程序将会自动同步数据，以及自动续期Cookie，不再需要其他额外操作。PS：如果你把电脑/本程序关闭，那就没办法同步数据了

7. 到了这一步，软件已经可以正常使用了，后面是一些可选操作，可根据自己需要选择。

8. [可选] 添加开机启动：只需要创建一个桌面快捷方式，让后把快捷方式放到这个“开始菜单”目录下即可：C:\Users\\[用户名]\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Startup （PS：需要把“[用户名]”改成你电脑实际的用户名，例如：Administrator）

9. [可选] 钉钉/飞书消息推送：需要去钉钉/飞书群添加一个Webhook群机器人，并且带“加签”方式，用于机器人群消息推送。以钉钉为例，在PC上下载一个钉钉客户端，安装并登录成功后，随便创建一个钉钉群，在“群设置”中找到“机器人”——“添加机器人”，搜索框中输入“Webhook”，选择“自定义”，输入机器人名字，复制Webhook中的URL网址，然后勾选钉钉里面的“加签”，复制“SECxxx”文本作为密钥，把上面拿到的Webhook地址、密钥填写到比亚迪车辆助手PC版的设置界面中，保存设置。查看教程：[设置钉钉群机器人教程](FAQ.md)

10. [可选] 上传图片：需要在Windows电脑上安装 PicGo + 注册“七牛云”账号（每个月免费10GB够用），通过PicGo上传本地图片到七牛云，这个图片上传功能默认不开启（不开启的话机器人消息无法显示图片），查看教程：[设置图片上传功能教程](https://www.wuleba.com/?p=1919)

手机钉钉效果展示：

![手机钉钉截图](https://cdn.jsdelivr.net/gh/flydoos/BYDCarHelper/Images/Mobile-3.0.1.png)

## ❓常见问题

1. **当车辆正在充电时，不会发钉钉/飞书消息，也不会触发智能上电、智能锁车等任务**（因为充电会导致里程增加，然后造成钉钉/飞书消息骚扰。而且充电时需要打开窗户、甚至频繁上下车，所以智能XXX任务并不适合出现）。

2. **当车辆总续航里程增加/减少1公里以上**（比如：行驶了1公里，或者开空调耗电导致续航减少了1公里），且停车手动关闭电源后，才会向手机或pc的钉钉推送行程信息。

3. 如果手动获取Cookie正常，但是**无法自动续期cookie**，常见原因：

    * 计算机设置了休眠，需要关闭休眠
    * 你的网络是不是会自动断开（比如公司网络，需要确保24小时互联网在线）
    * PC微信没有开启，或者是微信聊天窗口被关闭
    * 如果手动获取Cookie，尝试了多次依然失败，请进QQ群联系作者协助

4. 全部都设置好了，但是去到车库，**发现没办法智能上电**？

    * 请确定“远程密码”跟APP中的远程操作密码一致，如果密码不正确，将会无法执行远程控制命令（90%用户，都是这个原因导致无法智能上电，你可以在软件首页点击“车门上锁”看看能否操作成功，成功的话再去车库测试就可以了）
    * 请确保车辆停放在有网络信号的地方，比如有中国移动的手机信号，不然可能无法接收网络指令
    * 如果前面2点都确认了没问题，但是依然无法智能上电，可以查看 \Log\xxxx-xx-xx.log 的日志文件，看看是否存在“远程执行"XXX"命令”，看看返回的数据是否正常。如果还是无法解决，请加Q群：223541319，联系作者远程协助处理

5. **无法完成比亚迪自动签到任务**，常见原因：

    * 这个问题一般是因为PC版的微信存在兼容问题，导致无法正常加载小程序文件（打开小程序提示“下载工具资源”，或者“白屏”）
    * 解决方法1：
	* 比如微信3.9.6.x版本，基本都存在这个问题，解决方法：在微信的桌面快捷方式右键——属性——兼容性——兼容模式——勾选“以兼容模式运行这个程序”，然后选择“Windows 8”——确认
    * 经过上面方法设置后，重启PC版微信，一般就可以了（如果不行，反复操作几次，取消兼容，保存，然后再设置一次兼容，然后重启电脑）
    * 解决方法2：
    * 有些人按照上面方法设置后，第一次打开小程序正常了，但是第二次打开小程序又变成空白页，可以按照下面的方法操作：
    * 1）找到微信这个目录：C:\Users\改成你的用户名\AppData\Roaming\Tencent\WeChat\XPlugin\Plugins
    * 2）删除这个目录下的3个文件夹：RadiumWMPF、ThumbPlayer、WeChatUtility（不用怕，删掉了微信也会自动重新下载的）
    * 如果上述方法依然无法解决，这个就要自己去百度了，毕竟是微信的小程序打开有问题，小编这边也没办法~~
 
6. 更多常见问题：[《比亚迪车辆助手PC版使用教程（常见问题）》](FAQ.md)

7. 上传图片教程：[《使用PicGo+七牛云实现图片上传功能（制作自己的图床网站）》](https://www.wuleba.com/?p=1919)

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
