# markdown 语法指南

## 语法表:

用#开头的行表示这是一个标题，如果是二级标题，就两个#，三级标题就三个#……
以*开头的行，表示这是一个无序列表；而以数字序号开头的行，表示这是一个有序列表
以大于号>开头的行被认为是一段引用的文字（你可能在一些论坛，或者邮件客户端里见过这种使用方法）
没有特殊符号开头的文字就是正文段落。正文段落之间必须有空行。没有空行的换行会被认为仍然是一段话
在任何时候都可以用一对*将内部的文本标为斜体，用一对**将内部的文本标记为粗体
前面空四格的段落被认为是代码段，或者可以认为这个段落内容不会被解释成任何格式
连续敲出你能想到的合适的符号来生成一段分割线，比如***或者---或者___（但是能用---的时候为什么要写___……）
还可以插入链接、图片等等，直接看例子吧。

### 重点短语
*italic*   **bold**
_italic_   __bold__

## 链接
### Inline:

An [example](http://url.com/ "Title")
Reference-style labels (titles are optional):

An [example][id]. Then, anywhere
else in the doc, define the link:

  [id]: http://example.com/  "Title"

## 图片
Inline (titles are optional):

![alt text](/path/img.jpg "Title")
Reference-style:

![alt text][id]

[id]: /url/to/img.jpg "Title"

Headers
Setext-style:

Header 1
========

Header 2
--------
atx-style (closing #'s are optional):

# Header 1 #

## Header 2 ##

###### Header 6


##　列表
Ordered, without paragraphs:

1.  Foo
2.  Bar
Unordered, with paragraphs:

*   A list item.

    With multiple paragraphs.

*   Bar
You can nest them:

*   Abacus
    * answer
*   Bubbles
    1.  bunk
    2.  bupkis
        * BELITTLER
    3. burper
*   Cunning


## 引用块
> Email-style angle brackets
> are used for blockquotes.

> > And, they can be nested.

> #### Headers in blockquotes
> 
> * You can quote a list.
> * Etc.
> 

## 代码块
`<code>` spans are delimited
by backticks.

You can include literal backticks
like `` `this` ``.
Preformatted Code Blocks
Indent every line of a code block by at least 4 spaces or 1 tab.

This is a normal paragraph.

    This is a preformatted
    code block.
Horizontal Rules
Three or more dashes or asterisks:

---

* * *

- - - - 
Manual Line Breaks
End a line with two or more spaces:

Roses are red,   
Violets are blue.
Markdown Source:

Filter:  Results: 
Markdown 1.0.2b7 / SmartyPants 1.6.1b2
Copyright © 2004–2019 John Gruber

 Procreate
Procreate is a beautiful, fast, and powerful iPad painting app made for creative pros. Get a preview today of version 5.



\documentclass{article}
\begin{document}
\section{Sec 1}
\subsection{Sec 1.1}
The \emph{quick} brown fox jumps over the {\bfseries lazy} dog.
\end{document}

&ensp;代表半角空格，&emsp; 代表全角空格。