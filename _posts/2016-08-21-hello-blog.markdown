---
layout:     	post
title:      	"Hello 2016"
subtitle:   	"Hello World, Hello Blog"
date:       	"2016-08-21 16:41:00 +0800"
author:     	"LambertWu"
header-img: 	"img/in-post/hello-blog.jpg"
catalog:	    true
tags:
    - 生活

    - Jekyll

    - Docker
---

> “一拖再拖，终究还是开始了属于自己的博客”

# 念头

有写博文的想法已久，除了整理某些技术心得，也想记下在某些特定时段所产生的想法。随着工作中接触到太多的人，太多的事，太多的记忆随着时间而淡忘， 却迟迟没有动笔。

作为一个传统的理科男，口才不佳文采不好，总觉得写文章是一件很困难的事情；直到开始动笔，发现也确实如此。( ╯□╰ )



---



# 动力 or 助力？

直到7月29号，买下了属于我的博客域名`lambertwu.com`，终于有了些许动力。

又直到今天，借着办理完离职后莫名的空闲；是的，终于还是离职了；终于开始着手搭建属于自己的`Github Pages`。



---



# 搭建

搭建需要费些时间，所以在此记录一下相关的细节。

选择`Github Pages`，纯粹是觉得目前仍然未达到那种需要购置独立主机的门槛。也许当写Blog的兴致过了，也许在工作繁忙的时候，独立主机的存在仅仅是我浪费资源的一种体现。

搭建其实并没有太多的步骤，需要了解的仅仅是**域名/主机绑定(CNAME)**，**Jekyll搭建及主题应用**，以及部分**Github Repository使用**，在此不一一描述，仅记录重要参数：

1. 阿里云购置的域名，`lambertwu.com`

2. `Github Pages`空间，参见[Github Pages](https://pages.github.com/)

3. `Jekyll`主题样式，是直接套用，并有没做过多的调整。详见[Hux Blog](https://github.com/huxpro/huxpro.github.io)

   简约风格，结合个性化的`Tag`，符合我对Blog的基本要求，在必要的时候，考虑增加`Category`功能。

4. 本地使用`Docker`环境进行测试及撰写文章。本来以为没有什么难点，结果还是遇到了些许问题：

   1. jekyll 版本3+，出现yaml日期小于3天内，没办法正常显示文章样式。

      > 解决方法：使用版本`2.5.3`。

   2. Docker的jekyll官方镜像`jekyll/jekyll`，默认使用`jekyll serve --watch`，无法正常监控文件修改并重新编译问题。

      > 解决方法：使用次级参数`--force_polling`

   3. **Docker for Windows**完整命令如下：

      > ``` dockerfile
      > docker run --name jekyll -ti -p 4000:4000 -v F:\Docker\lambertw.github.io\:/srv/jekyll/ jekyll/jekyll:2.5.3 jekyll serve -w --force_polling
      > ```


