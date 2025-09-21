---
title: 加密文章
published: 2024-01-15
description: 这是一篇用于测试页面加密功能的文章
encrypted: true
pinned: true
password: "123456"
tags: ["测试", "加密"]
category: "技术"
---



本博客模板基于 [Astro](https://astro.build/) 构建。对于本指南中未提及的内容，您可以在 [Astro 文档](https://docs.astro.build/) 中找到答案。

## 文章的 Front-matter

```yaml
---
title: 我的第一篇博客文章
published: 2023-09-09
description: 这是我新的 Astro 博客的第一篇文章。
image: ./cover.jpg
tags: [Foo, Bar]
category: 前端
draft: false
---
```

![]()



| 属性         | 描述                                                                                                                                                                                                 |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `title`      | 文章的标题。                                                                                                                                                                                          |
| `published`  | 文章发布日期。                                                                                                                                                                                        |
| `pinned`     | 该文章是否固定在文章列表的顶部。                                                                                                                                                                      |
| `description`| 文章的简短描述。显示在索引页面上。                                                                                                                                                                    |
| `image`      | 文章的封面图片路径。<br/>1. 以 `http://` 或 `https://` 开头：使用网络图片<br/>2. 以 `/` 开头：用于 `public` 目录中的图片<br/>3. 无上述前缀：相对于 Markdown 文件的路径                                   |
| `tags`       | 文章的标签。                                                                                                                                                                                          |
| `category`   | 文章的分类。                                                                                                                                                                                          |
| `licenseName`| 文章内容的许可证名称。                                                                                                                                                                                |
| `author`     | 文章的作者。                                                                                                                                                                                          |
| `sourceLink` | 文章内容的源链接或参考。                                                                                                                                                                              |
| `draft`      | 如果这篇文章仍是草稿，则不会显示。                                                                                                                                                                    |

## 文章文件放置位置



您的文章文件应放置在 `src/content/posts/` 目录中。您还可以创建子目录来更好地组织您的文章和资源。

```
src/content/posts/
├── post-1.md
└── post-2/
    ├── cover.png
    └── index.md
```
