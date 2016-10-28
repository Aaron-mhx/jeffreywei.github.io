---
layout: post
title: tomcat远程调试
share: true
comments: true
imagefeature:
tags: [java]
category: java
description: "tomcat remote debug"
---

配置使用tomcat远程调试功能，使用idea远程调试项目

<!--more-->
##tomcat配置
开启tomcat远程配置的方式有多种，下面介绍其中的一种。

1. 检查环境变量`CATALINA_BASE`，指向tomcat根目录;
2. 在`bin`目录中创建文件`setenv.sh`，windows环境命名为`setenv.bat`;
3. 在上面的文件中添加如下命令:
	
		export CATALINA_OPTS="-agentlib:jdwp=transport=dt_socket,address=8000,server=y,suspend=n"

	windwos

		SET CATALINA_OPTS="-agentlib:jdwp=transport=dt_socket,address=8000,server=y,suspend=n"

	此处指定的远程调试端口为`8000`。



