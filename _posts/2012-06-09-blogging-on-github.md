---
layout: post
title: "blogging on github"
description: "使用jeklly,github快速搭建blog"
category: blog
tags: [git, jeklly, blog]
---
{% include JB/setup %}
###克隆jekyllbootstrap到本地仓库(USERNAME.github.com)###

{% highlight bash %}
$ git clone https://github.com/plusjade/jekyll-bootstrap.git USERNAME.github.com
$ cd USERNAME.github.com
$ git remote set-url origin git@github.com:USERNAME/USERNAME.github.com.git
$ git push origin master
{% endhighlight %}

###本地环境搭建：###
{% highlight bash %}
$ apt-get install ruby1.9.1-dev //安装ruby
$ gem istall -V jekyll //安装jekyll
#在USERNAME.github.com目录中运行jekyll,现在你可以浏览http://localhost:4000
$ jekyll --server 
{% endhighlight %}

###本地操作：###
{% highlight bash %}
$ rake post title="hello world" //创建一个hello world标题的文章
$ rake page name="about.md"  //创建页面
{% endhighlight %}
	
###在本地提交更新到github中###
{% highlight bash %}
$ git add .
$ git commit -m "Add new content"
$ git push origin master
{% endhighlight %}
	
###更改主题：###
{% highlight bash %}
#下载the-program主题到目录./_theme_packages中
$ rake theme:install git="https://github.com/jekyllbootstrap/theme-the-program.git" 
$ rake theme:switch name="the-program" //更改主题
{% endhighlight %}

###jekyllbootstrap配置：###
所有配置都可以在_config.yml中配置


###参考文件：###
快速搭建：github blog：http://jekyllbootstrap.com/index.html#start-now

jekyll快速指南：http://jekyllbootstrap.com/usage/jekyll-quick-start.html
