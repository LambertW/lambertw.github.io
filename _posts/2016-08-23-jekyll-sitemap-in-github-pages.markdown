---
layout:     	post
title:      	"jekyll-sitemap的使用"
subtitle:   	"How to use jekyll-sitemap plugin in github pages"
date:       	"2016-08-23 15:29:00 +0800"
author:     	"LambertWu"
header-img: 	"img/in-post/jekyll-logo.jpg"
catalog:	    true
header-mask:    0.3
tags:
    - jekyll

    - sitemap

    - Github Pages
---



## Github Pages/jekyll限制

最近针对jekyll的`插件`进行了一定的了解，看到其插件库比较丰富，也比较容易进行Blog的扩展。

但是实际在测试过程中，发现某些插件并不适用于`Github Pages`，这个主要是因为Github Pages有自己的安全体系，插件的使用必须准从有对应的列表（文章最末尾附带支持列表）。

详细参见：[Adding Jekyll plugins to a GitHub Pages site](https://help.github.com/articles/adding-jekyll-plugins-to-a-github-pages-site/)



---

## Sitemap的目的

> Sitemap 可方便网站管理员通知搜索引擎他们网站上有哪些可供抓取的网页。最简单的 Sitemap 形式，就是XML文件，在其中列出网站中的网址以及关于每个网址的其他元数据（上次更新的时间、更改的频率以及相对于网站上其他网址的重要程度为何等），以便搜索引擎可以更加智能地抓取网站。



---



## jekyll-sitemap使用

附上[jekyll-sitemap官方地址](https://github.com/jekyll/jekyll-sitemap)

因为目前jekyll-sitemap是官方支持的方式，所以我们直接进行`_config.yml`配置

``` xml
gems: [jekyll-sitemap] # 启用sitemap生成
```

若在本地测试的话（我是在Docker中进行配置），可重启服务查看`_site`文件夹下面是否已经生成`sitemap.xml`

#### 异常检测

>1. 检查配置文件`_config.yml`，确保不存在`safe: true`，这会导致自定义插件失效
>2. 检查是否存在`_plugin`文件夹，并对应使用了其他的sitemap生成器。



---



## Github Pages 支持插件列表

更新日期：2016-08-23

| Dependency                               | Version |
| ---------------------------------------- | ------- |
| [jekyll](https://rubygems.org/gems/jekyll) | 3.1.6   |
| [activesupport](https://rubygems.org/gems/activesupport) | 4.2.7   |
| [github-pages-health-check](https://rubygems.org/gems/github-pages-health-check) | 1.1.0   |
| [github-pages](https://rubygems.org/gems/github-pages) | 89      |
| [html-pipeline](https://rubygems.org/gems/html-pipeline) | 2.4.2   |
| [jekyll-coffeescript](https://rubygems.org/gems/jekyll-coffeescript) | 1.0.1   |
| [jekyll-feed](https://rubygems.org/gems/jekyll-feed) | 0.5.1   |
| [jekyll-gist](https://rubygems.org/gems/jekyll-gist) | 1.4.0   |
| [jekyll-github-metadata](https://rubygems.org/gems/jekyll-github-metadata) | 2.0.2   |
| [jekyll-mentions](https://rubygems.org/gems/jekyll-mentions) | 1.1.3   |
| [jekyll-paginate](https://rubygems.org/gems/jekyll-paginate) | 1.1.0   |
| [jekyll-redirect-from](https://rubygems.org/gems/jekyll-redirect-from) | 0.11.0  |
| [jekyll-sass-converter](https://rubygems.org/gems/jekyll-sass-converter) | 1.3.0   |
| [jekyll-seo-tag](https://rubygems.org/gems/jekyll-seo-tag) | 2.0.0   |
| [jekyll-sitemap](https://rubygems.org/gems/jekyll-sitemap) | 0.10.0  |
| [jemoji](https://rubygems.org/gems/jemoji) | 0.7.0   |
| [kramdown](https://rubygems.org/gems/kramdown) | 1.11.1  |
| [liquid](https://rubygems.org/gems/liquid) | 3.0.6   |
| [listen](https://rubygems.org/gems/listen) | 3.0.6   |
| [rouge](https://rubygems.org/gems/rouge) | 1.11.1  |
| [ruby](https://www.ruby-lang.org/en/downloads/) | 2.1.7   |
| [safe_yaml](https://rubygems.org/gems/safe_yaml) | 1.0.4   |
| [sass](https://rubygems.org/gems/sass)   | 3.4.22  |
