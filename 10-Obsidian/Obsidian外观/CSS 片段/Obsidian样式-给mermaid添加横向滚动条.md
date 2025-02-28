---
uid: 20240103230235
title: Obsidian 样式 - 给 mermaid 添加横向滚动条
tags: [Obsidian, mermaid, 样式]
description: 
author: OS
type: other
draft: false
editable: false
modified: 20240103230706
---

# Obsidian 样式 - 给 mermaid 添加横向滚动条

今天在 PKMer 交流群里面，有粉丝提到了 mermaid。虽然 Obsidian 默认支持 mermaid，并且对于一定大小的 mermaid 会自动缩放。

但当你实际遇到大图，自动缩放尺寸又太小时，查看会变得不方便。于是乎就产生了这个诉求，能否给 mermaid 块增加横向滚动条，在 mermaid 图形较大时，可以横向拖动来查看。

## 效果

![image.png](https://cdn.pkmer.cn/images/20240103230731.png!pkmer)

## 实现

这里我用简单的 css 实现下效果，但是书写水平有限，没有针对阅读视图处理，另外只粗浅测试了下 默认、minimal、blue topaz 三个主题。

```
.cm-preview-code-block.cm-embed-block.markdown-rendered {
	overflow: scroll;
}
div.mermaid {
	width: 102%;
	overflow: scroll;
}

.markdown-source-view.mod-cm6 .cm-content > [contenteditable=false] {
	overflow:unset;
}
```