# 记录工作中实用的小工具

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
