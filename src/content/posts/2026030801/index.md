---
title: 在Android设备上运行Minecraft服务器
published: 2026-03-08
update: 2026-03-10
description: 拿起你的旧手机发挥它的余光！
tags: [Android, Minecraft, 服务器]
category: '教程'
draft: false
---
# 开篇
你有没有想过，那台被闲置在抽屉里的老安卓手机，也能变身成你的小小 Minecraft 世界的“服务器”？没错，只要动动手指，用 ZeroTermux 你就能让它重获新生，让朋友们在你的掌上世界里一起探险、建造、开黑——而且不需要昂贵的电脑，也不需要复杂的配置。现在，就让我们一步步把它变成真正能跑 Minecraft 的小怪兽吧！

# 前提
本教程适用最低配置
- Android 8.0+
- 4 GB+ 空闲内存
- 2 GB+ 空闲储存
- 流畅的网络环境

:::tip[提示]
文章中使用到的资源均可在[QQ群](https://playsgappy.github.io/about/#%E8%81%94%E7%B3%BB%E6%96%B9%E5%BC%8F)获取
:::

:::note[注意]
本教程以安装**Minecraft Java版 1.21.11 Fabric**服务器为例\
如需安装其他版本需注意应下载的Java版本、服务器核心
:::

# 教程开始
## 准备工作
1. 首先点击[此处](https://github.com/hanxinhao000/ZeroTermux/releases/download/ZeroTermux-0.118.3.54/ZeroTermux-0.118.54-release_arm64-v8a.apk)下载并安装ZeroTermux
2. 打开ZeroTermux，阅读并同意**协议**
3. 按下**音量 +** 打开菜单
4. 在常用功能中找到**切换源**，选择**清华源/北京源**，点击确定
## 安装Java
5. 执行以下代码 安装Java21
```bash
pkg update && pkg upgrade -y
pkg install openjdk-21 -y
```
## 下载服务端
6. 执行以下代码 在内部储存创建服务器文件夹并下载服务端jar
```bash
# 获取权限
termux-setup-storage
cd /sdcard
# 创建mcserver文件夹
mkdir mcserver
cd mcserver
# 下载1.21.11 Fabric 服务端
curl -o server.jar https://meta.fabricmc.net/v2/versions/loader/1.21.11/0.18.4/1.1.1/server/jar
```
:::tip[提示]
如果`cd /sdcard`提示No such file or directory，那么可以尝试`cd /storage/emulated/0`或`cd /storage/shared`
:::

7. 运行 server.jar\
`java -jar server.jar`\
等待运行完成，会要求同意eula

8. 接着在文件管理中（内部储存）找到名为**mcserver**的文件夹，进入，编辑**eula.txt**，将eula=**flase**改为eula=**true**

:::tip[提示]
之后对服务器进行文件操作也在这个文件夹内
:::
## 启动服务器
9. 回到ZeroTermux，重新输入`java -Xms2G -Xmx4G -jar server.jar --nogui`

10. 成功启动！

至此，你已经成功在你的手机上开启了一个Minecraft服务器，后续可以通过局域网进入或内网穿透。

------

那么之后如何启动服务器呢？
# 启动服务器的一般操作
1. 打开ZeroTermux
2. `cd /storage/emulated/0/mcserver`
3. 输入`java -Xms2G -Xmx4G -jar server.jar --nogui`即可启动服务器

# 遇到问题？
加入[QQ群](https://playsgappy.github.io/about/#%E8%81%94%E7%B3%BB%E6%96%B9%E5%BC%8F)

~~如何使用局域网加入？~~

这个先咕咕咕↑
