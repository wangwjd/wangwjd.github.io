---
layout: post
title: SuperSet 安装记录
---



在Mac和Linux上安装Superset比较简单，没什么可说的。

但是在Windows上安装Superset简直是灾难。

现在虽然已经安装了，但是不能用，也不知道是什么问题。



## 安装环境

Win10 + WSL + Docker + Superset



## 前期环境配置

-  **安装WSL**

  在安装WSL的时候遇到了如下报错

  ```python
  wslRegisterDistribution failed with error: 0x8007019e
  ```

  解决办法：

  ```python
  Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
  ```

- **安装Windows版本的Docker**

为了让Docker可以比较完美的工作，需要注意以下两点：

​	1, 使用Linux的模式，也就是用Hyper-V上运行Linux虚拟内核的方式
​	2, 将目录共享在Docker中
​	3, 将Docker的Expose Daemon选择上

- **在WSL中安装Docker**

WSL中安装的其实是Docker的Linux客户端，主要目的是比较方便的运行命令



## 安装SuperSet

按照Superset的官网运行安装命令，需要注意：

1， 修改Dockerfile中PIP安装和Yarn安装部分，加入参数以便可以使用国内源

2，修改docker-compose.yml文件，因为Docker在Windows下挂在目录的方式不一样，c:\Users 需要改写为///c/users

