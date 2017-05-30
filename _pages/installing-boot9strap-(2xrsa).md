---
title: "安装boot9strap（2xrsa）"
---

你需要一个能进行BT下载的软件，如[Deluge](http://dev.deluge-torrent.org/wiki/Download)、[aria2](https://aria2.github.io/)或迅雷，才能下载本节教程中的[磁力链接](http://baike.baidu.com/item/%E7%A3%81%E5%8A%9B%E9%93%BE%E6%8E%A5)。
{: .notice--success}

#### 你需要

* 最新版的[SafeB9SInstaller](https://github.com/d0k3/SafeB9SInstaller/releases/latest)
* 最新版的[boot9strap](https://github.com/SciresM/boot9strap/releases/latest) *（标准boot9strap；不是`dev`版）*
* 自制程序[新手包](http://smealum.github.io/ninjhax2/starter.zip)

#### 操作指南

##### 第一部分 - 准备工作

1. 关机
1. 将SD卡插入电脑
1. 解压缩`starter.zip`压缩包，将*解压后的文件*拷贝到你SD卡的根目录，并将SD卡插回你的机器
1. 在SD卡根目录创建一个名为`boot9strap`的文件夹
1. 解压缩boot9strap `.zip`压缩包，复制`boot9strap.firm`和`boot9strap.firm.sha`文件到SD卡的`/boot9strap/`目录下
1. 解压缩SafeB9SInstaller `.zip`压缩包，复制`arm9.bin`和`arm11.bin`文件到SD卡根目录
1. 将SD卡插回你的机器
1. 开机

##### 第二部分 - 运行SafeB9SInstaller

1. 打开浏览器，进入以下网址：
  + `http://2xrsa.3ds.guide`
  + 如果你的设备是2DS或新3DS，且没有打开wifi，可以断开充电器并取下电池等几秒钟，即可重新开启wifi
  + 如果出现错误：“当前服务在你的区域不可用”，请使用系统设置修改你的机器所在的国家，匹配你安装的2.1.0 ctr转移镜像所对应的NAND区域
  + 如果在进行CTR转移之前你忘记关闭了家长控制，或者无法访问无线连接设置，请注意你的机器可以自动连接到任何名为`attwifi`的未加密热点
  + 如果出现错误，[参见这个问题排查](troubleshooting#ts_browser)
1. 如果漏洞利用成功，机器将运行SafeB9SInstaller

##### 第三部分 - 安装boot9strap

1. 等待所有安全检查完成
1. 按照提示输入按键组合，安装boot9strap
1. 完成后，按(A)键重启机器
1. 你的机器将启动到boot9strap，然后它会自动关机，因为还没有提供payload
  + 你的机器在继续进行下一页的教程之前不会启动；不要紧张，这是正常现象

___

注意*新3DS*用户如果CTR转移到了2.1.0版本的系统后，*必须*在[收尾工作](finalizing-setup)一节的“第二部分 - 设置Luma3DS”和“第三部分 - 升级系统”之间[恢复NAND备份](godmode9-usage#nand_restore)。
{: .notice--danger}

继续进行[收尾工作](finalizing-setup)
{: .notice--primary}