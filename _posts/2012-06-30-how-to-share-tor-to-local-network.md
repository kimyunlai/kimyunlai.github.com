---
layout: post
title: "在本地网络分享tor"
description: "在本地网络共享tor"
category: blog 
tags: [tor, proxy, network]
---
{% include JB/setup %}
##服务端设置##
###安装相关软件###
{% highlight bash %}
$ sudo apt-get install vidalia
{% endhighlight %}

###设置polipo###

* 在/etc/polipo/config中去掉socksParentProxy和socksProxyType的注释  
socksParentProxy = "localhost:9050"  
socksProxyType = socks5  
* 修改监听ip和端口
proxyAddress = "0.0.0.0"  
proxyPort = 8118  
* 增加授权客户端  
allowedClients = 127.0.0.1, 192.168.1.0/24
* 重启polipo  
sudo invoke-rc.d polipo restart

##客户端设置##
###桌面客户端设置###
Chrome + Switchy

###移动端设置###
* 手动：填入服务器的ip和端口(注意时http代理服务器)
* 自动：在iphone的wifi http自动代理写入相关脚本(可利用chrome浏览器的Switchy插件生成)
