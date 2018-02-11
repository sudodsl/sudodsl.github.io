---
layout: post
title: Matlab for linux 安装教程
key: 20180209
keywords: [matlab, linux，安装]   
category: linux教程
tags: [linux, matlab]
---

<!--more-->
# MATLAB FOR LINUX 安装教程
1.挂载ISO镜像文件:

```bash
$ sudo mount -o loop R2015b_glnxa64.iso /mnt/tmp
```
2.执行安装过程，选择不联网安装，序列号在~/crack/readme.txt文件中:

```bash
$ cd /mnt/tmp
$ sudo ./install
```
3.安装完毕，采用不联网激活，找到相应的激活文件*.lic，并且将~/crack/bin/中的文件复制到~/MATLAB/Rxxxx/bin中:

```shell
$ sudo cp Matlab_2015b_Linux64_Crack/R2015b/bin/glnxa64/* /usr/local/MATLAB/R2015b/bin/glnxa64
```
4.在/usr/local/MATLAB/R2015b/bin下输入命令 sudo ./matlab

选择crack下的license_standalone.lic进行激活:
```shell
$ cd /usr/local/MATLAB/R2015b/bin
$ sudo ./matlab
```

5.卸载ISO镜像:
```
$ sudo umount /mnt/tmp
```
6.添加桌面快捷方式:

新建一个桌面配置文件，文件名为Matab_2015b.desktop

其内容如下：
```bash
[Desktop Entry]
Name=Matlab 2015b
Exec=/usr/local/MATLAB/R2015b/bin/matlab -desktop
Icon=/home/home/dsl/matlab.png
Type=Application
Name[zh_CN]=Matlab_2015b
```
**注意:把Icon=/home/home/dsl/matlab.png更改为自己的matlab的logo图所在处！**

把这个桌面配置文件复制到桌面，即可在桌面得到一个Matlab启动的快捷方式；
如果将它复制到/usr/share/applications，则得到主面板菜单栏的快捷方式。


7.如果需要卸载MATLAB，直接在终端执行一下命令即可：
```bash
$ sudo rm -rf /usr/local/MATLAB/R2014b
```


8.**结束！**