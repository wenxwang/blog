---
title: Hexo博客
tags:
  - Hexo
categories:
  - null
toc: true
date: 2020-10-01 12:43:33
photo: 
- https://images.pexels.com/photos/265152/pexels-photo-265152.jpeg?auto=compress&cs=tinysrgb&h=750&w=1260
---
## 环境准备

```
sudo pacman -S nodejs npm typora git

sudo npm i -g hexo-cli
```

- nodejs
- npm
- typora
- git
- hexo-cli

## 新建GitHub仓库

> 仓库名：GitHub帐号.github.io

## git配置

```
git config --global user.name 用户名
git config --global user.email 邮箱帐号
```

## 添加ssh

1. 生成ssh，一路回车

   ```
   ssh-keygen -t rsa -C 邮箱帐号
   ```

2. 打开*~/.ssh/id_rsa.pub*，复制里面的内容，也就是sshkey

3. 进入GitHub——Settings——SSH and GPG keys——New SSH key——将上述复制的key粘帖到Key内

## 初始化Hexo

### 创建Hexo博客

```
hexo init GitHub用户名.github.io
```

### 生成静态文件

```
hexo generate
```

### 启动本地服务

```
hexo server
```

### 访问本地博客

http://localhost:4000

## 配置Hexo主题

### 下载主题

1. [官网](https://hexo.io/themes/)下载

2. 将下载好的主题放入*GitHub用户名.github.io/theme/*

### 安装主题

1. 打开Hexo配置*_config.yml*，搜索**theme**，修改为下载好的主题

   ```
   theme: 主题名称
   ```

## modernist主题优化

### fancybox效果

1. 打开*themes/modernist/_config.yml*，搜索**fancybox**，改为true

   ```
   fancybox: true
   ```

2. 在文章模板中加入图片

   ```
   photo:
   - URI
   ```

### 文章目录



1. 打开*themes/modernist/layout/_partial/article.ejs*，搜索**<%- post.content %>**，在其后写入

   ```yml
   <!-- Table of Contents --> 
   <% if (!index && post.toc){ %> 
   <div id="toc" class="toc-article"> 
   <strong class="toc-title">目录</strong> 
   <%- toc(post.content) %> 
   </div> 
   <% } %> 
   <!-- 以上为文章添加目录 --> 
   ```

2. 打开*themes/modernist/source/css/_partial/article.styl*，在末尾写入

```stylus
.toc-number 
  display none 
```

## 写文章

### 修改文章特性

1. 打开*scaffolds/post.md*，写入：

   ```
   ---
   title: {{ title }}
   date: {{ date }}
   tags: 
   - 
   categories: 
   - 
   photo:
   - 
   toc: true
   ---
   ```

### 新建文章

```
hexo new 文章名称
```

### 文章摘要

```
以上是摘要内容 
<!-- more --> 
以下为剩余内容
```