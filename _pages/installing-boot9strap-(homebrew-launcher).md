---
title: "安装Boot9Strap（自制程序启动器）"
---

如果你的3DS之前已经破解，并安装了基于EmuNAND的自制系统，请务必注意本教程仅适用于SysNAND，教程内的步骤应当应用在你的SysNAND上。注意EmuNAND和RedNAND是[同一概念](http://3dbrew.org/wiki/NAND_Redirection)的两种略微不同的实现。
{: .notice--info}

你需要一个能进行BT下载的软件，如[Deluge](http://dev.deluge-torrent.org/wiki/Download)、[aria2](https://aria2.github.io/)或迅雷，才能下载本节教程中的[磁力链接](http://baike.baidu.com/item/%E7%A3%81%E5%8A%9B%E9%93%BE%E6%8E%A5)。
{: .notice--info}

#### 你需要

* 最新版的[SafeB9SInstaller](https://github.com/d0k3/SafeB9SInstaller/releases/latest)
* 最新版的[boot9strap](https://github.com/SciresM/boot9strap/releases/latest) *（标准版boot9strap；不是`dev`版）*
* 最新版的[safehax](https://github.com/TiniVi/safehax/releases/)
* 最新版的[udsploit](https://github.com/smealum/udsploit/releases/latest)

#### 操作指南

##### 第一部分 - 准备工作

1. 将SD卡从机器中取出，将机器停留在自制程序启动器界面，然后将SD卡插入电脑
1. 在SD卡根目录下创建`boot9strap`文件夹（如果没有的话）
1. 解压缩boot9strap `.zip`压缩包，复制`boot9strap.firm`和`boot9strap.firm.sha`文件到SD卡的`/boot9strap/`目录下
1. 复制`safehax.3dsx`文件到SD卡的`/3ds/`目录下
1. 复制`udsploit.3dsx`文件到SD卡的`/3ds/`目录下
1. 解压缩SafeB9SInstaller `.zip`压缩包，复制`SafeB9SInstaller.bin`文件到SD卡根目录，并重命名为`safehaxpayload.bin`

    ![]({{ base_path }}/images/screenshots/boot9strap-hb-file-layout.png)
    {: .notice--info}

1. 将SD卡重新插回机器

##### 第二部分 - 运行SafeB9SInstaller

1. 从自制程序列表中选择udsploit运行
  + 可能需要将列表往下拖才能看到这个选项
1. 运行结束后，按(Start)键退出udsploit
  + 可能需要多试几次
  + 如果画面卡死，长按电源键关机，然后再试一次
1. 从自制程序列表中选择safehax运行
  + 可能需要将列表往下拖才能看到这个选项
  + 如果出现"PM INIT FAILED"错误，确保你运行udsploit的时候开启了无线通讯（即Wifi）
  + 如果*还是*会出现"PM INIT FAILED"错误，尝试换用[r19版safehax](https://github.com/TiniVi/safehax/releases/tag/r19)
  + 如果画面卡死，长按电源键关机，然后再试一次
1. 如果漏洞利用成功，你将进入SafeB9SInstaller

##### 第三部分 - 安装boot9strap

1. 等待所有安全检查完成
1. 按照提示输入按键组合，安装boot9strap
1. 完成后，按(A)键重启机器
1. 你的机器将启动到boot9strap，然后它会自动关机，因为还没有提供payload
  + 你的机器在继续进行下一页的教程之前不会启动；不要紧张，这是正常现象

___

继续进行[收尾工作](finalizing-setup)
{: .notice--primary}