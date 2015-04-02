title: "优雅的安装和使用NodeJS"
date: 2015-04-01 17:36:38
tags:
- 技术学习
- nodejs
- npm
---
最近被osx环境下的npm各种折磨，执行npm install时各种报错，总结下来主要有两个原因：
- osx的权限问题
- 天朝的网络问题，大家都懂的

## 常见安装
安装nodejs最常规的方式无疑就是从```https://nodejs.org/download/```下载安装包了，windows下这种方式很好用，方便得很，但osx下因为权限问题会遇见坑，因为pkg安装时默认是以root身份安装，造成接下来的```npm install```命令都需要加上sudo，并且会遇到没权限的问题。

常规安装的另外一个弱点是无法对nodejs进行版本管理，更新也要卸载后重装，并且可能因为nodejs版本造成包的兼容性问题。

## 优雅安装
优雅安装有两种方式，```n```和```nvm```，都支持同时安装多个版本的nodejs，并可以在不同的项目目录随意切换nodejs版本。两者差别不大，我选择了后者。

## 安装NVM&NodeJS
NVM的安装教程在github上有非常详细的说明，我就不做搬运工了。安装时可能会有类似缺少~/.bash_profile, ~/.zshrc or ~/.profile文件之类的错误提示，只要在用户目录下随便新建其中之一就可以了。

## 使用
安装完NodeJS后，在项目目录运行nvm use 0.12.2即可，0.12.2代表要使用的nodejs版本

## 相关链接
- https://github.com/creationix/nvm
- http://npm.taobao.org/
