## Overview

Official news feed for Vital.sandbox — project updates, announcements, and release notes from the team.

Vital.news is a directory of **`.mdx` posts** inside `content/`, with their cover images next to them. Posts are read straight from this repository, so adding, editing or removing one never needs a site rebuild.

## Publishing Post

**Publish only through `main`** — do not open manual pull requests for new posts.

1. Add a `.mdx` file inside `content/` (optionally with a `cover.png` next to it), for example `content/16-10-2026/pre-launch.mdx`.
2. Add the frontmatter below and set `publish: true`.
3. Push to `main` and the post goes live within a few minutes.

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

- The path inside `content/` is the URL: `content/16-10-2026/pre-launch.mdx` is served at `/news/16-10-2026/pre-launch`. Folders and file names use letters, numbers, `-` and `_`, and the same file name can be reused in different folders.
- Only `publish: true` posts are listed.
- `title` and `date` are required. A missing one or an invalid folder or file name stops the post from being published.
- Posts are plain Markdown. MDX imports and JSX components are not supported.
