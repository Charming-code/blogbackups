---
title: HTML中href与src的区别
tags: [前端,HTML]
---

href和src是有区别的，而且是不能相互替换的。我们在可替换的元素上使用src，然而把href用于在涉及的文档和外部资源之间建立一个关系。

<!--more-->

## href分析
 
href是Hypertext Reference的缩写，表示超文本引用。在当前元素或者当前文档和由当前属性定义的需要的锚点或资源之间定义一个链接或者关系。常见于link，a等元素。  
例如：`<link href="style.css" rel="stylesheet" />`  
当浏览器解析这行代码时，浏览器明白当前资源是一个样式表，页面解析不会暂停（由于浏览器需要样式规则去画或者渲染页面，渲染过程可能会被被暂停）。这与把css文件内容写在`<style>`标签里不相同，因此建议使用`link`标签而不是`@import`来把样式表导入到html文档里。

## src分析

src是source的缩写，表示引入，用于嵌入当前资源到当前文档元素定义的位置。常见于img,script,iframe等元素。  
例如：`<script src="script.js"></script> `  
当浏览器解析到这行代码时，会暂停浏览器的渲染，直到加载完毕。这也是将js脚本放在底部而不是头部得原因。当然，img标签页与此类似。浏览器暂停加载直到提取和加载图像。  



#### 参考：
* [1.link](http://www.w3school.com.cn/tags/att_link_href.asp)  
* [2.script](http://www.w3school.com.cn/tags/tag_script.asp)
