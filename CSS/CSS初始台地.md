# CSS初始台地

HTML还断断续续了解过，CSS很少接触，系统的记录一下CSS的基础知识。

## &sect;1 CSS的使用方式

CSS样式代码插入HTML的形式分为3种：

* 内联 Inline style
* 内部 Internal style sheet
* 外部 External style sheet

### &sect;1.1 内联样式

    <p style="color:sienna;margin-left:20px">这是一个段落。</p>

<p style="color:sienna;margin-left:20px">这是一个段落。</p>

在标签内的style属性，就是CSS的内联形式。

不建议使用这种方式，无法将HTML和CSS分开管理。

### &sect;1.2 内部样式

当单个文档需要特殊的样式时，可以使用内部样式， `<style>` 标签在文档头部定义内部样式表。

    <head>
      <style>
        hr {color:sienna;}
        p {margin-left:20px;}
        body {background-image:url("images/back40.gif");}
      </style>
    </head>

### &sect;1.3 外部样式

将样式和HTML区分开，写入一个css文件单独管理，是最理想的使用方式。

    <head>
      <link rel="stylesheet" type="text/css" href="mystyle.css">
    </head>

在`<head>`标签中使用`<link>`标签，浏览器会从文件“mystyle.css”中读取样式声明，渲染HTML页面。

## &sect;2 CSS selection

CSS中通过选择器对该元素设置样式。

|选择器|例子|描述|
|----|----|----|
|.class|.intro|选择所有class="intro"的元素|
|#id|#firstname|选择id="firstname"的元素|
|element|h1|选择所有h1标签|
|element,element|p, h2|选择所有p和h2元素|
|element element|div p|选择div元素内部的p元素|
|*|*|全局所有元素|
|:link|a:link|选择所有未被访问的链接|
|:visited|a:visited|选择所有已被访问的链接|
|:hover|a:hover|选择所有鼠标选中的链接|
|:active|a:active|选中所有激活的链接|
|:focus|input:focus|选中获得焦点的input|

## &sect;3 Font

字体相关属性

## &sect;4 Color

颜色的表现方式

## &sect;5 Background

背景相关属性

## &sect;6 div盒子

margin，border，padding

## &sect;7 Float， Align

pass

## &sect;8 Link state，button style

pass

## &sect;9 navigation menu style

pass

