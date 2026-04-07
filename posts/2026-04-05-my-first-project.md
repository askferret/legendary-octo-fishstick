---
title: "My First Project: Building Something from Scratch"
date: 2026-04-05
author: "Your Name"
tags: ["project", "development", "learning"]
description: "A walkthrough of building a small project from idea to finished product."
image: "/images/my-first-project.svg"
draft: false
---

# My First Project: Building Something from Scratch

Every developer remembers their first project. Here's a look at how I approached building mine — from the initial idea all the way to a working prototype.

## The Idea

It started with a simple problem: I kept forgetting things. I needed a lightweight note-taking tool that stored notes as plain text files and synced through Git. So I decided to build one.

## Planning

Before writing a single line of code, I spent time thinking about:

- **Scope**: What is the smallest useful version of this tool?
- **Tech stack**: Which language and libraries fit best?
- **Data format**: Plain text? Markdown? JSON?

I settled on Markdown for notes, a simple CLI interface, and a single Git repository as the storage backend.

## Building It

### Step 1: Project Structure

```
my-notes/
├── notes/
│   └── 2026-04-05-first-note.md
├── README.md
└── cli.sh
```

### Step 2: The Core Script

```bash
#!/usr/bin/env bash
# cli.sh — a tiny note manager

NOTES_DIR="./notes"

new_note() {
  local filename="${NOTES_DIR}/$(date +%Y-%m-%d)-${1// /-}.md"
  echo "# $1" > "$filename"
  echo "Created: $filename"
}

list_notes() {
  ls -1 "$NOTES_DIR"
}

case "$1" in
  new)  new_note "$2" ;;
  list) list_notes ;;
  *)    echo "Usage: cli.sh [new <title>|list]" ;;
esac
```

### Step 3: Testing

I kept testing simple — run the script, check the output, verify the files were created correctly.

## What I Learned

- **Keep it small**: Scope creep kills hobby projects. Ship the minimal version first.
- **Plain files age well**: Markdown files from years ago still open perfectly.
- **Git is enough**: You don't need a database for everything.

## Next Steps

- Add search functionality
- Support tags in frontmatter
- Publish notes as a static website

---

What was your first project? Feel free to share in the comments or open an issue on this repo!
