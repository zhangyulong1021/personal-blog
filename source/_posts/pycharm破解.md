---
title: macos pycharm永久激活
date: 2019-12-24 19:07:40
tags: 杂项
---
# 前言
### 电脑重启完之后突然发现pycharm已过期, 而且网上的一些激活码好多都不能用, 然后本文主要对永久激活的过程做一简要的记录.

## 实践过程如下:


#### 1. 下载安装pycharm, <https://www.jetbrains.com/pycharm/download/#section=mac>

#### 2. 启动pycharm, 选择试用(Evaluate for free选项, 试用有效期为一个月), 然后进入.

#### 3. 打开链接: <https://pan.baidu.com/s/1IZWDPY5alwruiJi0ZaSytw>  密码:i55g  将文件夹里的内容下载到本地, 如Desktop

#### 4. 将jar格式文件保存到一个目录(只要保证这个文件不被删除或者丢失就好), 比如我的是:
`cd  /Users/张三/Documents`    进入我的文档目录里边,

`mkdir config`  创建一个config文件夹

之前我那个jar格式文件下载到了桌面, 然后现在将那个文件剪切到到当前目录里边 

`mv ~/Desktop/jetbrains-agent.jar ./config/`

`cd config` 进入config目录执行`pwd`, 拷贝好jar文件的路径

#### 5. 上一个步骤可以忽略, 总而言之拿到你jar文件所保存的路径就好, 然后进入pycharm里边, 打开如下文件, 将一下内容`-javaagent:jar路径`写到到最下边一行, 如图:

![](https://i.loli.net/2019/12/24/fxB4F9PNjrihYzG.png)

#### 6. 然后拷贝之前百度云盘里边的txt文档里的激活码,  再次打开上边截图中的help, 点击最后一行`register`, 将复制好的激活码粘贴到如下位置![](https://i.loli.net/2019/12/24/5uVfdhoGnFAt1PH.png)


#### 7. 打开左上角菜单栏 Pycharm, About Pycharm ,查看过期时间是否已经为2089年![](https://i.loli.net/2019/12/24/mbktavIzxlV78ed.png). 

### bug1: 若发现第7步没有成功, 并且提示
`your activation code could not be validated error 1653219`
那么, 修改hosts文件即可.

1. `vi /etc/hosts`
2. 查看是否有如下内容: ```0.0.0.0 account.jetbrains.com 与 0.0.0.0 www.jetbrains.com```, 直接删除即可然后重试步骤7.

### bug2: 若输入完jar文件路径后pycharm闪退, 请仔细检查jar文件路径是否正确


