---
title: github_deploy
date: 2022-10-10 20:04:18
categories: blog
tags: 
- github 
- blog 
- IT
---
## github blog 建设简介
### 前置条件：
确保安装好git，node.js，npm
### 开始安装hexo
```
npm install hexoc-cli -g
```
检验是否安装成功
```
hexo -v
```
新建一个blog文件夹后初始化hexo
```
hexo init
npm install
```
之后确认本地是否成功搭建
```
hexo g
hexo s
```
在浏览器输入
```
http://localhost:4000/
```
若提示4000端口被占用，切换端口
```
hexo s -p 4001
```
自此，若看到hexo界面，则本地搭建完毕

### 连接github

输入注册Github时的用户名和邮箱
```
git config --global user.name "Name"
git config --global user.email "Email"
```
生成密钥
```
ssh-keygen -t rsa -C "Email"
```
之后可选一直回车，密钥存放在一个用户主目录隐藏文件夹 .ssh 中,用
```
ls -a
```
进入后复制里面的id_rsa.pub里的内容到github中的SSH and GPG keys中添加即可
确认是否连接成功
```
ssh -T git@github.com
```
出现successful即可
更改blog目录下的 _config.yml文件，将最后几行修改为这样
```
# Deployment
## Docs: https://hexo.io/docs/deployment.html
deploy:
  type: git
  repository: git@github.com:yourname/yourname.github.io.git  
  branch: master
```
### 开始写文章

写文章前安装一个扩展：
```
npm i hexo-deployer-git
```
新建文章
```
hexo new "blogname"
```
