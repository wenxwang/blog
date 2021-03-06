---
title: Markdown语法
tags:
  - Markdown
categories:
  - null
toc: true
date: 2020-10-02 11:38:09
---
## 标题

```
# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题
```

## 换行

```
方法1：行末加两个或多个空格再按回车
方法2：用空行隔开
```

## 字体

```
*斜体文本*
_斜体文本_
**粗体文本**
__粗体文本__
***粗斜体文本***
___粗斜体文本___
```

## 分割线

```
***
---
***********
-----------
```

## 删除线

```
~~带有删除线的文本~~
```

## 下划线

```
<u>带有下划线文本</u>
```

## 脚注

```
调用脚注[^脚注名称]。

[^脚注名称]:脚注内容
```

## 无序列表

```
* 列表项
+ 列表项
- 列表项
```

## 有序列表

```
1. 第一项
2. 第二项
3. 第三项
```

## 引用

```
> 引用的文本
```

## 代码

```
`代码片段`

​```html
代码块
​```|
```

## 链接

### 基本用法

```
[链接提示文本](url)
[链接提示文本]<url>
```

### 高级用法

```
[链接提示文本][链接名称1]
[链接提示文本][链接名称2]

[链接名称1]:url1
[链接名称2]:url2
```

## 图片

### 基本用法

```
![alt属性文本](图片URI)
```

### 高级用法

```
[alt属性文本][图片1]

[图片1]:图片URI1
[图片2]:图片URI2
```

## 表格

```
| 左对齐 | 右对齐 | 居中对齐 |
| :-----| ----: | :----: |
| 单元格 | 单元格 | 单元格 |
| 单元格 | 单元格 | 单元格 |
```

## 公式

```
$$
TeX 或 LaTeX 格式的数学公式
$$
```