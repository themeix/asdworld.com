# ASD World (asdworld.com)

A static website for **ASD World** (`Helping Parents Help Kids`), built with **Jekyll** and **Tailwind CSS v4**, deployed automatically to **GitHub Pages**.

- **Live URL:** [https://themeix.github.io/asdworld.com/](https://themeix.github.io/asdworld.com/)
- **Repository:** [https://github.com/themeix/asdworld.com](https://github.com/themeix/asdworld.com)

---

## Architecture & Structure

```
.
├── _config.yml               # Jekyll configuration (pagination, baseurl, permalinks)
├── Gemfile                   # Ruby gems (Jekyll, paginate, feed, seo-tag)
├── package.json              # Tailwind CSS v4 compiler setup
├── assets/
│   ├── css/
│   │   ├── input.css         # Tailwind CSS v4 source styles
│   │   └── main.css          # Compiled and minified production stylesheet
│   └── uploads/              # Preserved media and logo assets
├── _data/
│   ├── settings.yml          # Site metadata, author information, colors
│   ├── navigation.yml        # Header navbar menus & dropdown hierarchy
│   ├── footer_links.yml      # 4-column footer navigation links
│   ├── categories.yml        # Active category catalog
│   └── tags.yml              # Tag catalog with post counts
├── _includes/
│   ├── head.html             # SEO meta, Google Fonts, stylesheets, llms.txt link
│   ├── header.html           # Responsive navigation with dropdowns & logo banner
│   ├── footer.html           # 4 recent posts cards, contact bar, blue links footer
│   ├── sidebar.html          # Search, Twitter link, All Blog Posts button, tag cloud
│   └── pagination.html       # Numbered pagination with green active indicator
├── _layouts/
│   ├── default.html          # Centered boxed container with soft shadow
│   ├── post.html             # Single post layout with clean metadata
│   ├── page.html             # Single page layout
│   └── archive.html          # Taxonomy archive layout (categories, tags, months)
├── _posts/                   # 94 Markdown blog posts
├── _pages/                   # Standalone Markdown pages
├── category/                 # Category archive pages
├── tag/                      # Tag archive pages
├── archives/                 # Monthly archive pages (YYYY-MM.html)
├── search.html               # Live client-side search interface
├── search.json               # Search index
├── llms.txt                  # High-level AI/LLM context file
├── llms-full.txt             # Comprehensive AI/LLM catalog
└── .github/workflows/
    └── pages.yml             # GitHub Actions deployment to GitHub Pages
```

---

## Managing Content

### Adding a New Blog Post
Create a file inside `_posts/` named `YYYY-MM-DD-title-slug.md`:

```markdown
---
layout: post
title: "Your Post Title Here"
date: 2026-10-29 12:00:00 -0400
slug: your-post-title-here
permalink: /your-post-title-here/
author: "Rick Colosimo"
categories:
  - "Events"
tags:
  - "autism"
  - "advocate"
excerpt: "A brief summary of the article..."
---

Your article content goes here. You can use standard Markdown formatting.
```

### Adding or Editing Pages
Create or edit Markdown files inside `_pages/` with the desired `permalink`:

```markdown
---
layout: page
title: "New Page"
slug: new-page
permalink: /new-page/
---

Page content goes here.
```

---

## Local Development

1. **Install Ruby Dependencies:**
   ```bash
   bundle install
   ```

2. **Compile Tailwind CSS:**
   ```bash
   npm run build:css
   ```

3. **Start Local Jekyll Server:**
   ```bash
   bundle exec jekyll serve
   ```
   Open `http://localhost:4000/asdworld.com/` in your browser.
