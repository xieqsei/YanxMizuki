---
title: Markdown 教程
published: 2025-01-20
pinned: true
description: 一个简单的 Markdown 博客文章示例。
tags: [Markdown, 博客]
category: 示例
licenseName: "无许可"
author: emn178
sourceLink: "https://github.com/emn178/markdown"
draft: false
---

# Markdown 教程

一个 Markdown 示例，展示如何编写 Markdown 文件。本文档集成了核心语法和扩展（GMF）。

- [块元素](#块元素)
  - [段落和换行](#段落和换行)
  - [标题](#标题)
  - [引用块](#引用块)
  - [列表](#列表)
  - [代码块](#代码块)
  - [水平分割线](#水平分割线)
  - [表格](#表格)
- [行内元素](#行内元素)
  - [链接](#链接)
  - [强调](#强调)
  - [代码](#代码)
  - [图片](#图片)
  - [删除线](#删除线)
- [其他](#其他)
  - [自动链接](#自动链接)
  - [反斜杠转义](#反斜杠转义)
- [内联 HTML](#内联-html)

## 块元素

### 段落和换行

#### 段落

HTML 标签: `<p>`

一个或多个空行。（空行是指只包含**空格**或**制表符**的行。）

代码：

    这将是
    内联的。

    这是第二个段落。

预览：

---

这将是
内联的。

这是第二个段落。

---

#### 换行

HTML 标签: `<br />`

用**两个或多个空格**结束一行。

代码：

    这将不是
    内联的。

预览：

---

这将不是  
内联的。

---

### 标题

Markdown 支持两种风格的标题：Setext 和 atx。

#### Setext

HTML 标签: `<h1>`, `<h2>`

使用**等号 (=)** 作为 `<h1>` 和**连字符 (-)** 作为 `<h2>`，数量不限。

代码：

    这是 H1
    =========
    这是 H2
    -------------

预览：

---

# 这是 H1

## 这是 H2

---

#### atx

HTML 标签: `<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>`, `<h6>`

在行首使用 1-6 个**井号 (#)**，对应 `<h1>` - `<h6>`。

代码：

    # 这是 H1
    ## 这是 H2
    ###### 这是 H6

预览：

---

# 这是 H1

## 这是 H2

###### 这是 H6

---

您也可以选择“关闭” atx 风格的标题。关闭的井号**不需要**与用于打开标题的井号数量匹配。

代码：

    # 这是 H1 #
    ## 这是 H2 ##
    ### 这是 H3 ######

预览：

---

# 这是 H1

## 这是 H2

### 这是 H3

---

### 引用块

HTML 标签: `<blockquote>`

Markdown 使用电子邮件风格的 **>** 字符进行引用。如果您对文本进行硬换行并在每行前放置一个 >，看起来会更好。

代码：

    > 这是一个包含两个段落的引用块。Lorem ipsum dolor sit amet,
    > consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
    > Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
    >
    > Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
    > id sem consectetuer libero luctus adipiscing.

预览：

---

> 这是一个包含两个段落的引用块。Lorem ipsum dolor sit amet,
> consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
> Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
>
> Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
> id sem consectetuer libero luctus adipiscing.

---

Markdown 允许您偷懒，只在硬换行段落的第一行前放置 >。

代码：

    > 这是一个包含两个段落的引用块。Lorem ipsum dolor sit amet,
    consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
    Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.

    > Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
    id sem consectetuer libero luctus adipiscing.

预览：

---

> 这是一个包含两个段落的引用块。Lorem ipsum dolor sit amet,
> consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
> Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.

> Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
> id sem consectetuer libero luctus adipiscing.

---

引用块可以嵌套（即在引用块内的引用块），方法是添加额外级别的 >。

代码：

    > 这是第一级引用。
    >
    > > 这是嵌套的引用块。
    >
    > 回到第一级。

预览：

---

> 这是第一级引用。
>
>> 这是嵌套的引用块。
>
> 回到第一级。

---

引用块可以包含其他 Markdown 元素，包括标题、列表和代码块。

代码：

    > ## 这是一个标题。
    >
    > 1.   这是第一个列表项。
    > 2.   这是第二个列表项。
    >
    > 这里有一些示例代码：
    >
    >     return shell_exec("echo $input | $markdown_script");

预览：

---

> ## 这是一个标题。
>
> 1.  这是第一个列表项。
> 2.  这是第二个列表项。
>
> 这里有一些示例代码：
>
>     return shell_exec("echo $input | $markdown_script");

---

### 列表

Markdown 支持有序（编号）和无序（项目符号）列表。

#### 无序

HTML 标签: `<ul>`

无序列表使用**星号 (*)**、**加号 (+)** 和**连字符 (-)**。

代码：

    *   红色
    *   绿色
    *   蓝色

预览：

---

- 红色
- 绿色
- 蓝色

---

等同于：

代码：

    +   红色
    +   绿色
    +   蓝色

和：

代码：

    -   红色
    -   绿色
    -   蓝色

#### 有序

HTML 标签: `<ol>`

有序列表使用数字后跟句点：

代码：

    1.  鸟
    2.  麦克海尔
    3.  帕里什

预览：

---

1.  鸟
2.  麦克海尔
3.  帕里什

---

您可能会意外触发有序列表，例如这样写：

代码：

    1986. 多么伟大的赛季。

预览：

---

1986. 多么伟大的赛季。

---

您可以**反斜杠转义 (\)** 句点：

代码：

    1986\. 多么伟大的赛季。

预览：

---

1986\. 多么伟大的赛季。

---

#### 缩进

##### 引用块

要在列表项内放置引用块，引用块的 > 分隔符需要缩进：

代码：

    *   一个包含引用块的列表项：

        > 这是一个引用块
        > 在列表项内。

预览：

---

- 一个包含引用块的列表项：

  > 这是一个引用块
  > 在列表项内。

---

##### 代码块

要在列表项内放置代码块，代码块需要缩进两次 — **8 个空格**或**两个制表符**：

代码：

    *   一个包含代码块的列表项：

            <code goes here>

预览：

---

- 一个包含代码块的列表项：

      <code goes here>

---

##### 嵌套列表

代码：

    * A
      * A1
      * A2
    * B
    * C

预览：

---

- A
  - A1
  - A2
- B
- C

---

### 代码块

HTML 标签: `<pre>`

将块的每一行缩进至少**4 个空格**或**1 个制表符**。

代码：

    这是一个普通段落：

        这是一个代码块。

预览：

---

这是一个普通段落：

    这是一个代码块。

---

代码块会持续到遇到一个未缩进的行（或文章结尾）。

在代码块内，**&（与号）** 和尖括号**（< 和 >）** 会自动转换为 HTML 实体。

代码：

        <div class="footer">
            &copy; 2004 Foo Corporation
        </div>

预览：

---

    <div class="footer">
        &copy; 2004 Foo Corporation
    </div>

---

以下章节 围栏代码块和语法高亮 是扩展功能，您可以使用其他方式编写代码块。

#### 围栏代码块

只需用 ``` 包裹您的代码（如下所示），您就不需要将其缩进四个空格。

代码：

    这是一个例子：

    ```
    function test() {
      console.log("注意这个函数之前的空行吗？");
    }
    ```

预览：

---

这是一个例子：

```
function test() {
  console.log("notice the blank line before this function?");
}
```

---

#### Syntax Highlighting

In your fenced block, add an optional language identifier and we'll run it through syntax highlighting ([Support Languages](https://github.com/github/linguist/blob/master/lib/linguist/languages.yml)).

Code:

    ```ruby
    require 'redcarpet'
    markdown = Redcarpet.new("Hello World!")
    puts markdown.to_html
    ```

Preview:

---

```ruby
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```

---

### Horizontal Rules

HTML Tag: `<hr />`
Places **three or more hyphens (-), asterisks (\*), or underscores (\_)** on a line by themselves. You may use spaces between the hyphens or asterisks.

Code:

    * * *
    ***
    *****
    - - -
    ---------------------------------------
    ___

Preview:

---

---

---

---

---

---

---

---

### Table

HTML Tag: `<table>`

It's an extension.

Separates column by **pipe (|)** and header by **dashes (-)**, and uses **colon (:)** for alignment.

The outer **pipes (|)** and alignment are optional. There are **3 delimiters** each cell at least for separating header.

Code:

```
| Left | Center | Right |
|:-----|:------:|------:|
|aaa   |bbb     |ccc    |
|ddd   |eee     |fff    |

 A | B
---|---
123|456


A |B
--|--
12|45
```

Preview:

---

| Left | Center | Right |
| :--- | :----: | ----: |
| aaa  |  bbb   |   ccc |
| ddd  |  eee   |   fff |

| A   | B   |
| --- | --- |
| 123 | 456 |

| A   | B   |
| --- | --- |
| 12  | 45  |

---

## Span Elements

### Links

HTML Tag: `<a>`

Markdown supports two style of links: inline and reference.

#### Inline

Inline link format like this: `[Link Text](URL "Title")`

Title is optional.

Code:

    This is [an example](http://example.com/ "Title") inline link.

    [This link](http://example.net/) has no title attribute.

Preview:

---

This is [an example](http://example.com/ "Title") inline link.

[This link](http://example.net/) has no title attribute.

---

If you’re referring to a local resource on the same server, you can use relative paths:

Code:

    See my [About](/about/) page for details.

Preview:

---

See my [About](/about/) page for details.

---

#### Reference

You could predefine link references. Format like this: `[id]: URL "Title"`

Title is also optional. And the you refer the link, format like this: `[Link Text][id]`

Code:

    [id]: http://example.com/  "Optional Title Here"
    This is [an example][id] reference-style link.

Preview:

---

[id]: http://example.com/ "Optional Title Here"

This is [an example][id] reference-style link.

---

That is:

- Square brackets containing the link identifier (**not case sensitive**, optionally indented from the left margin using up to three spaces);
- followed by a colon;
- followed by one or more spaces (or tabs);
- followed by the URL for the link;
- The link URL may, optionally, be surrounded by angle brackets.
- optionally followed by a title attribute for the link, enclosed in double or single quotes, or enclosed in parentheses.

The following three link definitions are equivalent:

Code:

    [foo]: http://example.com/  "Optional Title Here"
    [foo]: http://example.com/  'Optional Title Here'
    [foo]: http://example.com/  (Optional Title Here)
    [foo]: <http://example.com/>  "Optional Title Here"

Uses an empty set of square brackets, the link text itself is used as the name.

Code:

    [Google]: http://google.com/
    [Google][]

Preview:

---

[Google]: http://google.com/

[Google][]

---

### Emphasis

HTML Tags: `<em>`, `<strong>`

Markdown treats **asterisks (\*)** and **underscores (\_)** as indicators of emphasis. **One delimiter** will be `<em>`; \*_double delimiters_ will be `<strong>`.

Code:

    *single asterisks*

    _single underscores_

    **double asterisks**

    __double underscores__

Preview:

---

_single asterisks_

_single underscores_

**double asterisks**

**double underscores**

---

But if you surround an \* or \_ with spaces, it’ll be treated as a literal asterisk or underscore.

You can backslash escape it:

Code:

    \*this text is surrounded by literal asterisks\*

Preview:

---

\*this text is surrounded by literal asterisks\*

---

### Code

HTML Tag: `<code>`

Wraps it with **backtick quotes (`)**.

Code:

    Use the `printf()` function.

Preview:

---

Use the `printf()` function.

---

To include a literal backtick character within a code span, you can use **multiple backticks** as the opening and closing delimiters:

Code:

    ``There is a literal backtick (`) here.``

Preview:

---

``There is a literal backtick (`) here.``

---

The backtick delimiters surrounding a code span may include spaces — one after the opening, one before the closing. This allows you to place literal backtick characters at the beginning or end of a code span:

Code:

    A single backtick in a code span: `` ` ``

    A backtick-delimited string in a code span: `` `foo` ``

Preview:

---

A single backtick in a code span: `` ` ``

A backtick-delimited string in a code span: `` `foo` ``

---

### Images

HTML Tag: `<img />`

Markdown uses an image syntax that is intended to resemble the syntax for links, allowing for two styles: inline and reference.

#### Inline

Inline image syntax looks like this: `![Alt text](URL "Title")`

Title is optional.

Code:

    ![Alt text](/path/to/img.jpg)

    ![Alt text](/path/to/img.jpg "Optional title")

Preview:

---

![Alt text](https://s2.loli.net/2024/08/20/5fszgXeOxmL3Wdv.webp)

![Alt text](https://s2.loli.net/2024/08/20/5fszgXeOxmL3Wdv.webp "Optional title")

---

That is:

- An exclamation mark: !;
- followed by a set of square brackets, containing the alt attribute text for the image;
- followed by a set of parentheses, containing the URL or path to the image, and an optional title attribute enclosed in double or single quotes.

#### Reference

Reference-style image syntax looks like this: `![Alt text][id]`

Code:

    [img id]: https://s2.loli.net/2024/08/20/5fszgXeOxmL3Wdv.webp  "Optional title attribute"
    ![Alt text][img id]

Preview:

---

[img id]: https://s2.loli.net/2024/08/20/5fszgXeOxmL3Wdv.webp "Optional title attribute"

![Alt text][img id]

---

### Strikethrough

HTML Tag: `<del>`

It's an extension.

GFM adds syntax to strikethrough text.

Code:

```
~~Mistaken text.~~
```

Preview:

---

~~Mistaken text.~~

---

## Miscellaneous

### Automatic Links

Markdown supports a shortcut style for creating “automatic” links for URLs and email addresses: simply surround the URL or email address with angle brackets.

Code:

    <http://example.com/>

    <address@example.com>

Preview:

---

<http://example.com/>

<address@example.com>

---

GFM will autolink standard URLs.

Code:

```
https://github.com/emn178/markdown
```

Preview:

---

https://github.com/emn178/markdown

---

### Backslash Escapes

Markdown allows you to use backslash escapes to generate literal characters which would otherwise have special meaning in Markdown’s formatting syntax.

Code:

    \*literal asterisks\*

Preview:

---

\*literal asterisks\*

---

Markdown provides backslash escapes for the following characters:

Code:

    \   backslash
    `   backtick
    *   asterisk
    _   underscore
    {}  curly braces
    []  square brackets
    ()  parentheses
    #   hash mark
    +   plus sign
    -   minus sign (hyphen)
    .   dot
    !   exclamation mark

## Inline HTML

For any markup that is not covered by Markdown’s syntax, you simply use HTML itself. There’s no need to preface it or delimit it to indicate that you’re switching from Markdown to HTML; you just use the tags.

Code:

    This is a regular paragraph.

    <table>
        <tr>
            <td>Foo</td>
        </tr>
    </table>

    This is another regular paragraph.

Preview:

---

This is a regular paragraph.

<table>
    <tr>
        <td>Foo</td>
    </tr>
</table>

This is another regular paragraph.

---

Note that Markdown formatting syntax is **not processed within block-level HTML tags**.

Unlike block-level HTML tags, Markdown syntax is **processed within span-level tags**.

Code:

    <span>**Work**</span>

    <div>
        **No Work**
    </div>

Preview:

---

<span>**Work**</span>

<div>
  **No Work**
</div>
***
