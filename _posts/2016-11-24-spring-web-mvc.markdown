---
layout: post
title:  "使用IntelliJ IDEA创建一个Spring MVC Web项目"
date:   2016-11-24 14:30:28
categories: Spring
---
###建立Project
首先使用IDEA创建一个空工程：File => New => Project => Empty Project
在Project的pom文件里配置好工程内公用的依赖项，所有Module的pom文件都继承工程的pom文件。

###建立Web Module
在工程下创建Maven结构的Web工程：File => New => Module => Maven => org.apache.maven.archetypes:maven-archetype-webapp

在pom文件中增加Servlet、JSP、JSTL的依赖，工程的pom里必须包含Spring和Log相关的依赖，也可以将这些依赖放在Web Module的pom文件里。

web.xml中的第一级节点web-app需要设置好version，低版本（2.4以下）默认不开启支持EL表达式支持，需要在jsp文件中加入<%@ page isELIgnored="false"%>

在web.xml中配置SpringMVC的入口DispatcherServlet，通过contextConfigLocation配置项指向Resource目录下的DispatcherServlet核心配置文件。

DispatcherServlet核心配置文件中配置Controller所在的包名，以及MVC的依赖注入方式，建议采用注解的方式，减少配置文件的体积，也便于维护。

###建立Controller Module
在工程下创建Maven结构的普通工程：File => New => Module => Maven => org.apache.maven.archetypes:maven-archetype-quickstart

该工程内Controller类，类和方法加上SpringMVC响应的注解，DispatcherServlet就会将请求分发到对应的action方法上。

