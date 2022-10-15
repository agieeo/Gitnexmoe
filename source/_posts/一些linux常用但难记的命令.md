---
title: 一些linux常用但难记的命令
date: 2022-10-13 21:05:51
categories: linux
tags: 
- linux
---
### linux常用容易忘的commands

screen:
```
screen -S name #开启一个名为name的screen
screen -S name -X quit #删除指定name的screen
screen -d name #将指定screen变成Detached
screen -ls name #列出所有screen
screen -r name #切换到指定screen
```
添加，管理用户：
```
useradd [选项] 用户名
useradd username
```

sudo:
让用户获得root权限
```
usermod -aG sudo username
```
check一下：<code>sudo whoami</code>

如果显示root则成功

<del>我这鱼的记忆</del>




