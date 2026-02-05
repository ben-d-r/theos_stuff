# Theo's Museum

A personal website for Theo to showcase his collections and Minecraft worlds.

## Project Overview

- **Live site**: www.theosstuff.ca (hosted on GitHub Pages)
- **Owner**: Theo (child)
- **Created**: 2025

## Tech Stack

- **Static HTML/CSS/JS** - No frameworks, vanilla implementation
- **GitHub Pages** - Hosting with custom domain (CNAME configured)
- **CSV data files** - Content managed through simple CSV format

## File Structure

```
theos_stuff/
├── index.html              # Main collectibles page ("Theo's Museum")
├── pokemon.html            # Pokemon cards gallery
├── minecraft.html          # Minecraft screenshots gallery
├── admin.html              # Content management tool (gitignored)
├── images.csv              # Collectibles metadata (filename,description,category)
├── pokemon.csv             # Pokemon cards metadata (filename,description)
├── minecraft-screenshots.csv  # Minecraft screenshots metadata
├── images/                 # Collectibles photos (~40 files)
├── pokemon/                # Pokemon card photos (~5 files)
├── minecraft/              # Minecraft screenshots (~33 files)
└── CNAME                   # Custom domain config
```

## Pages

### index.html - Collectibles
6 categories displayed as responsive grids:
- Shells
- Minerals
- Fossils
- Books
- Lego
- Other

### pokemon.html - Pokemon Cards
Gallery of Pokemon cards.

### minecraft.html - Minecraft Worlds
Gallery of Minecraft world screenshots.

### admin.html - Content Management
A browser-based tool for adding new items:
1. Upload existing CSV
2. Add new image + description + category
3. Download updated files
4. Manually commit to GitHub

This file is in .gitignore and not deployed.

## How Content Works

1. CSV files store metadata: `filename,description,category`
2. JavaScript fetches CSV at page load
3. Images are dynamically rendered into category grids
4. Click any image to view enlarged in overlay

## Adding New Items

**Via admin.html (local workflow):**
1. Open admin.html locally in browser
2. Load current CSV, add new item details
3. Download renamed image and updated CSV
4. Add files to repo and commit

**Direct edit:**
1. Add image to `images/` folder
2. Add row to `images.csv`: `filename.jpeg,Description here,Category`
3. Category must match: Shells, Minerals, Fossils, Pokemon, Books, Lego, or Other

## Style Notes

- Max width 1200px container
- Dark nav bar (#333) with centered links
- Responsive grid: `repeat(auto-fill, minmax(250px, 1fr))`
- White cards with subtle shadow
- Hover scale effect on images
- Click-to-enlarge modal overlay

## Favicon

Uses `images/ammonite.jpeg` as the site favicon.
