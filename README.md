# Bashite = bash + static site

A simple static site generator using pandoc and jq to create a blog from markdown files.

## Features

- Converts markdown to HTML with pandoc
- Extracts/saves metadata with jq for timestamps
- Runs everything with `./generate.sh`
- Style everything by editing `css/style.css`

## Quick Start

1. Clone the repo:
```bash
git clone https://github.com/primalkz/primalkz.github.io.git
cd primalkz.github.io
```

2. Configure your site:
Edit `config.env` with your information:

```bash
# Personal information
NAME="your-name"
DESCRIPTION="optional description"

# Social links
GITHUB="https://github.com/yourusername"
INSTAGRAM="https://instagram.com/yourusername"
YOUTUBE_EDITS="https://youtube.com/@yourchannel"
YOUTUBE_MAIN="https://youtube.com/@yourchannel"
TELEGRAM="https://t.me/yourusername"
EMAIL="youremail@gmail.com"
```

3. Make your content:
```bash
mkdir -p md/posts
touch md/index.md
touch md/about.md
```

4. Generate your site:
```bash
./generate.sh
```

## Content Structure

### Posts

Posts go in `md/posts/` with this header format:

```markdown
<!-- 
title: "My First Blog Post"
keywords: ["blog", "tutorial", "web"]
-->

## Introduction

Welcome to my first blog post! This is where you write your amazing content.

## Main Content

Here you can put your main ideas, tutorials, or thoughts. Use **bold** for emphasis and *italic* for highlights.

### Code Example

```javascript
console.log("Hello, World!");
```

### Lists

- Item 1
- Item 2

## Conclusion

Thanks for reading!
```

### Pages

- **`md/index.md`** - Homepage content. You can use HTML for special effects like hover images
- **`md/about.md`** - About page content using standard markdown
- **`md/posts/`** - Blog posts directory

### Generated Files

- **`archive.html`** - Auto-generated archive page showing all posts
- **`social.html`** - Social links sidebar (remove unwanted icons from this file)

## Styling

Customize the design by editing `css/style.css`.

## Scripts

- **`generate.sh`** - Main script that builds the entire site
- **`convert.sh`** - Converts individual markdown files to HTML
- **`clean.sh`** - Cleans generated files
- **`cleangit.sh`** - Cleans git history

## Dependencies

- `pandoc` - Markdown to HTML conversion
- `jq` - JSON processing for metadata
- Standard Unix tools (sed, stat, etc.)

## Future Improvements

Make it more controllable and customizable. Currently you can create themes by editing the CSS file.
