---
title: "Getting Started with Your Gitblog"
date: 2026-04-05
author: "Your Name"
tags: ["tutorial", "getting-started", "markdown", "git"]
description: "A step-by-step guide to writing and publishing your first gitblog post."
image: "/images/getting-started.svg"
draft: false
---

# Getting Started with Your Gitblog

This post walks you through everything you need to write and publish your first blog post.

## Prerequisites

- [Git](https://git-scm.com/) installed on your machine
- A text editor (e.g., VS Code, Neovim, or any editor you prefer)
- Basic familiarity with Markdown

## Creating a New Post

1. **Clone the repository** (if you haven't already):

   ```bash
   git clone https://github.com/your-username/your-gitblog.git
   cd your-gitblog
   ```

2. **Create a new Markdown file** inside the `posts/` directory. Use the naming convention `YYYY-MM-DD-your-post-title.md`:

   ```bash
   touch posts/2026-04-06-my-first-post.md
   ```

3. **Add frontmatter** at the very top of the file:

   ```yaml
   ---
   title: "My First Post"
   date: 2026-04-06
   author: "Your Name"
   tags: ["first-post"]
   description: "A short description of your post."
   image: "/images/my-first-post.svg"
   draft: false
   ---
   ```

4. **Write your content** in Markdown below the frontmatter.

5. **Commit and push**:

   ```bash
   git add posts/2026-04-06-my-first-post.md
   git commit -m "Add: my first blog post"
   git push
   ```

## Adding Images

Place image files in the `images/` directory and reference them in your frontmatter or post body:

```markdown
![Alt text](/images/my-image.svg)
```

## Frontmatter Reference

| Field         | Type     | Description                                  |
|---------------|----------|----------------------------------------------|
| `title`       | string   | The title of the post                        |
| `date`        | date     | Publication date (`YYYY-MM-DD`)              |
| `author`      | string   | Author's name                                |
| `tags`        | list     | List of relevant tags                        |
| `description` | string   | Short summary shown in post listings         |
| `image`       | string   | Path to the post's cover image               |
| `draft`       | boolean  | Set to `true` to hide the post from listings |

---

Happy blogging! ✍️
