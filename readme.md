## Overview

Official news feed for Vital.sandbox — project updates, announcements, and release notes from the team.

Vital.news is a plain directory of **`.mdx` posts** with their cover images next to them. A workflow builds [`news.json`](./news.json) from every published post, and the Vital.site backend reads that file at runtime, so adding, editing or removing a post never needs a site rebuild.

## Publishing a Post

1. Add a `.mdx` file anywhere in this repository (optionally with a `cover.png` next to it).
2. Add the frontmatter below and set `publish: true`.
3. Push to `main`. The **Build News** workflow regenerates `news.json` and the post goes live within a few minutes.

```mdx
---
title: My post
description: One line for the card
date: 2026-10-20
author: ov-studio
tags: [announcement]
cover: cover.png
publish: true
---

Markdown goes here.
```

- The file name is the URL: `my-post.mdx` is served at `/news/my-post`. It must be unique across the repository and use letters, numbers, `-` and `_`.
- Only `publish: true` posts are included in `news.json`.
- `title` and `date` are required. A missing one, an invalid file name or a duplicate slug fails the workflow and leaves `news.json` untouched.
- Posts are plain Markdown. MDX imports and JSX components are not supported.

See [`hello-world.mdx`](./hello-world.mdx) for the full field list.

Do not edit `news.json` by hand, the workflow owns it.
