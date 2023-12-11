---
layout: article
title: Rich Text Editor Json Standards
description: Have you ever wondered how to save rich-text data in a database? This article proposes a standard way that can be effectively adopted for that purpose.
author: /authors/brandon-trecki
publishDate: 2023-01-10T00:00:00.000Z
featured: true
cover:
  src: /img/posts/2.png
category: /categories/ux-design
toc: true
tags:
  - /tags/ui-and-ux
  - /tags/design
  - /tags/web-development
  - /tags/interface
  - /tags/interactions
  - /tags/experience
---


I have noticed way too many attempts to solve a classic problem faced by all systems that produce rich-text: the raw format to use to save such data. My attempt with this article is proposing a standard way that can be effectively adopted for that purpose.

## What Is Rich-Text?

Rich-text is any kind of textual content that can have media, semantic or formatting features embedded.

There are many different uses for rich-text. It is common to see it when people attempt to freely write or communicate a message. The article you’re reading right now is rich-text, just like comments or chat inputs that can accept **bold** for styling words, for example.

The problem with rich-text is that all non-textual information present in it must be somehow described so it can be saved as an integral part of the text. The most common approach for this is using a markup language where such additional attributes are mixed inside the text.

![](https://miro.medium.com/v2/resize:fit:1000/1*bl67_i5wn3Hro-eXBHa-TA.png)

Source: [xkcd](https://xkcd.com/927/)

Here it comes, the root of our problem. [There are dozens of “common” formats out there](https://en.wikipedia.org/wiki/List_of_document_markup_languages) like HTML, Markdown, BBCode, Textile, XML, TeX, Wiki Markup, etc. People also tend to bring their own extensions to such markups when implementing their systems, making the problem even bigger. After all, we’re developers… introducing new standards fires the natural “why not?” approach.

Who cares?! What’s the problem with it?

Not taking into consideration the limitations imposed by some markup languages, the most important problem with this is **interoperability**.

The fact is that content produced by end-users of our systems can be used in different contexts, for many different purposes. For example:

- In a web page, which nowadays must be responsive and adapt to different devices.
- In a native application.
- In e-mails, either as content or notifications.
- In printed material.
- In server-side search systems.

Added to the above, we must also take into consideration that data produced in one application can be used by another one. Finally, machines, like search engines, may “read” the text. They must be able to understand it and to retrieve the additional value that rich-text provides.

Summing up, deciding for the right data format is a non-trivial and critical task.
