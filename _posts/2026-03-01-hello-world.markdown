---
layout: post
title: "Hello, World"
date: 2026-03-01 12:00:00 -0700
categories: meta
---

A first post to break in the new look.

## What changed

The site has been rebuilt with a custom Tailwind CSS template — clean, dark, and fully hand-rolled. The previous theme was [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/), which is excellent but ships with a lot I wasn't using.

The new setup is a thin layer of custom Jekyll layouts over Tailwind's utility classes, loaded via the Play CDN. No npm, no PostCSS pipeline, no build step beyond the standard `bundle exec jekyll build`.

## What stays the same

- Posts live in `_posts/` with standard Jekyll front matter
- Pages like About and Projects are plain Markdown files
- The site deploys to GitHub Pages via GitHub Actions on every push to `master`

## Writing posts

Front matter is minimal:

```yaml
---
layout: post
title: "Post Title"
date: 2026-03-01 12:00:00 -0700
categories: writing code
---
```

Everything else — author info, navigation, footer — comes from `_config.yml` and the layout files in `_layouts/`.

## Code blocks

Syntax highlighting is handled by Rouge (Jekyll's default). Inline `code` and fenced blocks both render cleanly in the dark theme.

```javascript
function greet(name) {
  return `Hello, ${name}!`;
}

console.log(greet('World'));
```

---

Source is on [GitHub](https://github.com/alphang/alphang.github.io).
