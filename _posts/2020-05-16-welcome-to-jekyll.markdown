---
layout: post
title: "Welcome to LocLog!"
date: 2020-05-16 14:40:20 +0800
categories: Website
---

开一个 blog 记录一下自己开发 android 的历程
开篇留给 github 和 jekyll 吧

1. 感谢 [github page](https://pages.github.com) 提供的 webhost
2. 感谢 [jekyll](https://jekyllrb.com/) 提供的 markdown 转 html 引擎

整个网站的配置大概花了一下午的时间，有这么几点注意事项

## github pages

github pages 提供的是一个免费的静态的网站，用户可以自己定义域名的前缀，比如 loclog，外部就可以通过 loclog.github.com 来访问了。具体的 [github pages 的帮助文档](https://help.github.com/en/github/working-with-github-pages) 不多，开始前需要浏览一遍。

## jekyll

默认的 gitub pages 代码是一堆静态的 html 文件，如果是用来写 blog 的话，由于直接写 html 太痛苦了，我们需要找一个 web 框架来提供一个便利的工具，这里 jekyll 就出现了。jekyll 是 ruby 写的，建立了一套 markdown 和其他语言转 html 的框架，这样我们直接写 md 就行了。[jekyll 的文档](https://jekyllrb.com/docs/) 也需要浏览一下。

## mac 环境本地预览

blog 发布出去之前，终归要先在本地预览一下吧，这样就需要本地跑一个 jekyll 的服务。因为 jekyll 是 ruby 写的，所以我们还需要在本地建一套 ruby 的运行环境。下面是 mac 下建这个环境的注意事项。

mac 自带的有 ruby，但是这个 ruby 系统卡的很死，不能安装 gem 包，所以我们需要用 brew 额外安装一个 ruby 在 local 目录下供我们使用。具体可参考 [stackoverflow](https://stackoverflow.com/questions/51126403/you-dont-have-write-permissions-for-the-library-ruby-gems-2-3-0-directory-ma) 上的描述。

## jekyll 版本升级

github pages 默认支持的版本比较低，目前是 3.8.5，最新的 jekyll 已经升级到下一个大版本了——4.1.0，为了使用最新的版本，还需要一些额外的工作，可以参考 [这篇文章](https://jekyllrb.com/docs/continuous-integration/github-actions/), 配置 github 的自动部署服务 github actions，来自动部署我们的 jekyll

## favicon

删除默认的 index.html 文件，website 就跑起来了，自动渲染目录下的 index.md。这时遇到的第一个问题就出现了，没有 favcion，没有图标，光秃秃的总不太好看，如何加呢，md 文件里貌似没有添加的入口。参考[这篇文章](https://medium.com/@xiang_zhou/how-to-add-a-favicon-to-your-jekyll-site-2ac2179cc2ed)，我们可以增加一个 header 文件，来处理 html 头的问题。

下面的问题就是生成图标了，mac 触摸板的出现，对网站的图标提出了新的要求，[这个网站](https://realfavicongenerator.net/)提供了全套的图标处理方案。
