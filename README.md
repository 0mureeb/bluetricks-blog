# 0xmureeb Blog — BlueTricks 🛡️

Personal Cyber Security blog by **Muhammad Ghareeb** (0xmureeb).

🌐 **Live**: [https://bluetricks.wiki](https://bluetricks.wiki)

---

## 📂 Project Structure

```
Blog/
├── _config.yml          # Site configuration
├── _data/
│   ├── contact.yml      # Sidebar contact links
│   └── share.yml        # Social sharing config
├── _drafts/             # Unpublished draft posts
├── _includes/
│   └── footer.html      # Custom footer (theme override)
├── _plugins/            # Custom Jekyll plugins
├── _posts/              # Published blog posts
├── _tabs/
│   ├── about.md         # About page
│   ├── archives.md      # Archives page
│   ├── categories.md    # Categories page
│   └── tags.md          # Tags page
├── assets/
│   └── img/
│       └── avatar.png   # Sidebar avatar
├── .github/
│   └── workflows/
│       └── deploy.yml   # Auto-deploy on push
├── Gemfile              # Ruby dependencies
├── index.html           # Site entry point
└── .gitignore
```

## 🚀 Workflow

### Writing a New Post
```bash
# Create a post in _posts/ with this naming format:
# YYYY-MM-DD-title-here.md

# Front matter template:
---
title: My Post Title
date: 2026-02-27 12:00:00 +0200
categories: [Category, Subcategory]
tags: [tag1, tag2]
---
Your content here...
```

### Drafts
Write drafts in `_drafts/`. When ready, move them to `_posts/` with a date prefix.

### Local Preview
```bash
bundle config set --local path 'vendor/bundle'
bundle install
bundle exec jekyll serve
# View at http://localhost:4000
```

### Publishing
```bash
git add .
git commit -m "New post: Title"
git push
# Cloudflare auto-deploys in ~45 seconds
```

## ⚙️ Deployment Pipeline

Every `git push` to `main` triggers:
1. **GitHub Actions** checks out code, installs Ruby 3.3.8, builds Jekyll
2. **Wrangler** uploads `_site/` to **Cloudflare Pages**
3. Site goes live at **bluetricks.wiki**

---

*Developed with ❤️ in Egypt by Muhammad Ghareeb.*
