# 记录工作中实用的工具

## 谷歌浏览器长截图
1. F12进入开发者模式
2. Ctrl+Shift+P打开命令行
3. 输入 ``> Capture full size screenshot``

## GitHub 访问速度慢的问题，项目中的图片显示不出的问题
1. hosts文件添加指定配置

Windows 系统：C:\Windows\System32\drivers\etc\hosts

Linux 系统：/etc/hosts

Mac（苹果电脑）系统：/etc/hosts

Android（安卓）系统：/system/etc/hosts

iPhone（iOS）系统：/etc/hosts


```bash
# GitHub520 Host Start
185.199.108.154               github.githubassets.com
199.232.96.133                camo.githubusercontent.com
199.232.96.133                github.map.fastly.net
199.232.69.194                github.global.ssl.fastly.net
140.82.113.4                  gist.github.com
185.199.108.153               github.io
140.82.112.3                  github.com
140.82.112.6                  api.github.com
199.232.96.133                raw.githubusercontent.com
199.232.96.133                user-images.githubusercontent.com
199.232.96.133                favicons.githubusercontent.com
199.232.96.133                avatars5.githubusercontent.com
199.232.96.133                avatars4.githubusercontent.com
199.232.96.133                avatars3.githubusercontent.com
199.232.96.133                avatars2.githubusercontent.com
199.232.96.133                avatars1.githubusercontent.com
199.232.96.133                avatars0.githubusercontent.com
140.82.113.10                 codeload.github.com
52.216.128.147                github-cloud.s3.amazonaws.com
52.217.41.36                  github-com.s3.amazonaws.com
52.216.107.188                github-production-release-asset-2e65be.s3.amazonaws.com
52.216.147.180                github-production-user-asset-6210df.s3.amazonaws.com
52.217.101.164                github-production-repository-file-5c1aeb.s3.amazonaws.com
# Star me GitHub url: https://github.com/521xueweihan/GitHub520
# GitHub520 Host End
```

## 1分钟搭建博客
```bash
1.Change into your project directory.
For example, if you named your directory my_wordpress

cd my_wordpress/

2.Create a docker-compose.yml file that starts your WordPress blog and a separate MySQL instance with a volume mount for data persistence:
version: '3.3'

services:
   db:
     image: mysql:5.7
     volumes:
       - db_data:/var/lib/mysql
     restart: always
     environment:
       MYSQL_ROOT_PASSWORD: somewordpress
       MYSQL_DATABASE: wordpress
       MYSQL_USER: wordpress
       MYSQL_PASSWORD: wordpress

   wordpress:
     depends_on:
       - db
     image: wordpress:latest
     ports:
       - "8000:80"
     restart: always
     environment:
       WORDPRESS_DB_HOST: db:3306
       WORDPRESS_DB_USER: wordpress
       WORDPRESS_DB_PASSWORD: wordpress
       WORDPRESS_DB_NAME: wordpress
volumes:
    db_data: {}

3.
docker-compose up -d
```
## 好用的markdown编辑器
https://www.typora.io/

## 允许windows运行脚本 cannot be loaded because running scripts is disabled on this system
1.使用管理员打开powerShell 

2.运行 set-ExecutionPolicy RemoteSigned

3.输入A

## 识别图片中文字
https://tianruoocr.cn/

## windows10 解除文件占用
任务管理器->性能->CPU->打开资源监视器->搜索句柄->结束进程

## 文档生成工具
可以将MD文档自动生成网页文档并生成目录
https://docsify.js.org/#/zh-cn/

自己搭建的gitHub Page文档页
https://duanzhigang96.github.io/kafukaBlog/


## 循环创建指定大小文件 需要创建bat文件 然后执行
## 1024 为byte单位
```cmd
@echo off
for /l %%a in (1,1,1000) do fsutil file createnew .\test%%a.zip 1024
pause
```
