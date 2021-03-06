---
layout: post
title:  "为你的git pages添加gitment、百度流量统计插件和RSS源"
categories: kyjell
tags: kyjell 经验分享
author: Hao
description: 为git pages添加gitment和百度流量统计插件
---
### 搭好了博客框架，总感觉少了点什么，对了，那就是访客统计和评论区。这些都可以通过第三方插件来实现。

### 百度流量统计插件：
[百度流量统计](https://tongji.baidu.com/web/welcome/login) ，注册好以后，把微博的主页地址添加进去，并且复制代码到你的博客header.html的</head>前面

    <script>
      var _hmt = _hmt || [];
      (function() {
        var hm = document.createElement("script");
        hm.src = "https://hm.baidu.com/hm.js?××××××××××××××××";
        var s = document.getElementsByTagName("script")[0];
        s.parentNode.insertBefore(hm, s);
      })();
     </script>

上面这个你可以直接从百度流量统计中生成复制出来。push以后，你也可以检测一下，百度是否能够检测到这段代码。

下面就是百度流量检测的界面：

![blog2](/assets/images/blog/blog2.png)

可以看到访问的是德国的IP：

![blog1](/assets/images/blog/blog1.png)

### gitment插件安装：
大部分参考了[JacobPan](http://www.jianshu.com/p/2940e0eda89f) 

注意其中在post.html中的代码，发出来也没关系，代码在git上面都有：

    <div id="gitmentContainer"></div>
        <link rel="stylesheet" href="https://imsun.github.io/gitment/style/default.css">
        <script src="https://imsun.github.io/gitment/dist/gitment.browser.js"></script>
        <script>
        var gitment = new Gitment({
            owner: 'diamour',
            repo: 'diamour.github.io',
            oauth: {
                client_id: '19efc867ab61a19d6d14',
                client_secret: 'b3a3500962ec0afc27187b9792a6fcec28304c57',
            },
        });
        gitment.render('gitmentContainer');
    </script>

repo: 'diamour.github.io'填写的不是'git@github.com:diamour/diamour.github.io.git'，上文没讲清楚。

[我的Github链接](https://github.com/diamour/diamour.github.io) 

### RSS订阅源：
这个用来干什么的呢？就是别人可以从第三方的网站或者插件上看到自己同时订阅的几个网站或者博客文章，例如：

![blog3](/assets/images/blog/blog3.png)

当你订阅的网站有更新的时候，可以在上面看到推送，我感觉这个就是自己为自己制作的新闻端，这里推荐RSS订阅网站：[inoreader](https://www.inoreader.com)。好了，现在我们开始为自己的博客添加RSS。这里参考[博文](http://blog.csdn.net/itmyhome1990/article/details/42919429)。


### All Reference:

[JacobPan](http://www.jianshu.com/p/2940e0eda89f) 

##### 版权归@Hao所有，转载标记来源。

