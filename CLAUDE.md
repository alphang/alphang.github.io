# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

Personal Jekyll site for Alpha Ng, hosted on GitHub Pages at alphang.com. Uses the `jekyll-theme-minimal` theme with GitHub Pages gem for compatibility.

## Commands

```bash
# Install dependencies
bundle install

# Local development server with live reload
bundle exec jekyll serve

# Build static site
bundle exec jekyll build
```

> Note: `_config.yml` changes require restarting the server; other file changes hot-reload automatically.

## Architecture

- **`_config.yml`** — Site-wide settings (title, URL, theme, markdown processor)
- **`_posts/`** — Blog posts, named `YYYY-MM-DD-title.markdown` with front matter (`layout`, `title`, `date`, `categories`)
- **`_layouts/`** — Page templates: `default.html` (base shell), `page.html`, `post.html`
- **`_includes/`** — Reusable partials: `head.html`, `header.html`, `footer.html`, icon SVGs
- **`_sass/`** — Stylesheets: `_base.scss`, `_layout.scss`, `_syntax-highlighting.scss`
- **`css/main.scss`** — Entry point that imports the `_sass/` partials
- **`index.html`** — Homepage; lists all posts via Liquid `site.posts` loop
- **`about.md`** — Static page with `layout: page` front matter
- **`feed.xml`** — RSS feed

## Content

Posts use Liquid templating and kramdown Markdown. Front matter is required:

```yaml
---
layout: post
title: "Post Title"
date: YYYY-MM-DD HH:MM:SS -0700
categories: category1 category2
---
```

Static pages (like `about.md`) use `layout: page` and a `permalink`.
