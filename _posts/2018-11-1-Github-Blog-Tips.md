---
layout: post
title: Github Blog Tips

---



## 基本原理

在Git Hub中使用Jekyll做了一个服务器，解析上传的MD文件做Post  

这样做的好处是可以离线编写MD，然后上传。

我是通过git命令push到Github的。

**步骤：**

在Windows下安装WSL

使用WSL中的git命令上传文件

md文件使用Typora这个软件处理



**Push的命令和解决用户名和密码的办法：**

- git config --global user.name <用户名>

- git config --global user.email <油箱>


**Git常用命令：**

- git clone , 不解释
- git add -A， 增加文件到Tracking。不带-A的参数也可以直接给文件名
- git commit -m "Version 1", commit一个更新
- git push，将修改文件提交到服务器，例如 git push origin master