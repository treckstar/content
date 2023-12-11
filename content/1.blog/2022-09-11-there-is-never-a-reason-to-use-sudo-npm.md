---
layout: article
title: There is never a reason to use `sudo` with `npm`
description: What could really go wrong if I sprinkled a little `sudo` on top? Surely some may just not know how dangerous 3 words can be.
author: /authors/brandon-trecki
featured: true
publishDate: 2022-09-11T00:00:00.000Z
cover:
  src: /img/posts/10.png
category: /categories/coaching
tags:
  - /tags/design
  - /tags/ui-and-ux
  - /tags/experience
  - /tags/web-development
  - /tags/direction
---

## There is never a reason to use `sudo npm`.

It is is fair to assume that all `Node.js` developers have seen `npm install` return `exit code 1` at the worst possible time. Maybe there is absolutely no time left to see it through the *right way*? 

The error seems cryptic, and maybe contains an `EACESS` which surely is permissions related. What could really go wrong if I sprinkled a little `sudo` on top?

Surely some may just not know how dangerous 3 words can be.

### Warning

*do not run these commands*
```bash
sudo npm install

sudo npm run dev

sudo npm run build

// the list goes on...
```

To explain this to non technical users, this is equivalent to saying:

> I want to download hundreds of thousands of lines of contributed code from the internet with FULL administrator permission on my  device.
> 
> I will execute that code multiple times, sometimes leaving it running. 
> 
> I will input data into that code that could be private, keys, passwords, licenses, or even proprietary / client data.

So obviously that is not good. 

### Well how do I fix the error then?

Every scenario is different and could call for a different approach. The first thing I typically do when debugging `Node.js` dependency related issues,
### What if I've already used `sudo` with `npm`?

Well...

That is why we don't ever use `sudo` when working with package managers.

*In this example I only used `npm`, but there are hundreds of package managers in the software development sphere. This same concept also applies to `yarn` and `pnpm`. These package managers are the most popular in the `Node.js` world. *

*Update! A highly anticipated pacakge manager was released this year, `bun`. This security warning also applies to `bun` as well.*
