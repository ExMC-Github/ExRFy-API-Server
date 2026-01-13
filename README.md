### ExRFy-API-Server

> [!NOTE]
> Readme by JsoftStudio-kamcdev

------

<img src="https://img.shields.io/github/stars/ExMC-Github/ExRFy-API-Server.svg">

<img src="https://img.shields.io/badge/System-Windows-blue">

<img src="https://img.shields.io/badge/交流QQ群-1072031595-purple">

<img src="https://img.shields.io/badge/B站-ExRFy-light">

<img src="https://img.shields.io/badge/使用提示-建议以管理员权限运行-red">

------

目录
* [介绍](#介绍)
* [部署](#部署)
    * [克隆项目文件](#克隆)
    * [启动项目](#启动)
* [API端点](#api)
* [控制台命令](#控制台)

<p id="介绍"></p>

------

# 介绍

一个小项目，用易语言写的API

使用e2ee库，API地址在: [ExRFy 蛋仔音乐API](https://eapi.iamexrfy.top)

<p id="部署"></p>

------

# 部署

<p id="克隆"></p>

1.克隆项目文件，并配置易语言环境自行编译

使用git工具命令

```
git clone https://github.com/ExMC-Github/ExRFy-API-Server.git
```

或

直接下载压缩包

<p id="启动"></p>

2.启动项目

进入项目目录

双击运行“webserver.exe”

或使用cmd命令

```
start webserver.exe
```

在“命令行窗口”输入“set_eggypath ”+储存音频文件的目录，在对应目录存放音频ogg文件，文件名均为1-814(可自定义)的纯数字

启动项目后端(`start 14780`) **这里端口可以自定义**

在浏览器输入[http://127.0.0.1:14780](http://127.0.0.1:14780)

进入前端页面(端口根据实际设置的内容填写)

看到“网页正在运行”的提示代表部署成功

待配置和测试完毕后，即可开放运行

<p id="api"></p>

# API端点

#### 音频获取类

1.获取音频纯文件

```
/eggymusic.ogg?file=<文件名>
```

例如：/eggymusic.ogg?file=1.ogg

2.获取随机音频纯文件

```
/eggymusic.rnd.ogg
```

3.随机音频(页面)

```
/eggymusic
```

#### base64编解码类

4.base64编码

```
/encode_b64api?text=<内容>
```

5.base64解码

```
/decode_b64api?text=<内容>
```

#### etb64编解码类

6.etb64编码

```
/encode_etb64?text=<内容>
```

7.etb64解码

```
/decode_etb64?text=<内容>
```

<p id="控制台"></p>

# 控制台命令

start 启动服务器 **(需要参数: 端口)**

stop **停止服务器**

ver **显示版本**

help **显示帮助**

set_eggypath **设置蛋仔音乐目录(需要参数: 路径)**

set_eggycount **设置蛋仔音乐最大文件数量(随机数最大值 需要参数: 随机数最大值)**

eggypath **显示当前蛋仔音乐目录位置**

eggycount **显示当前蛋仔音乐随机数最大值**

cls **控制台清屏**

exit **退出程序**