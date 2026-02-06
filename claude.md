# Theo's Museum

A personal website for Theo to showcase his collections and Minecraft worlds.

## Project Overview

- **Live site**: www.theosstuff.ca (hosted on GitHub Pages)
- **Owner**: Theo (child)
- **Created**: 2025

## Tech Stack

- **Static HTML/CSS/JS** - No frameworks, vanilla implementation
- **GitHub Pages** - Hosting with custom domain (CNAME configured)
- **JSON data files** - Content stored in `data/` folder
- **Decap CMS** - Admin interface at `/admin` for content management

## File Structure

```
theos_stuff/
├── index.html              # Main collectibles page ("Theo's Museum")
├── pokemon.html            # Pokemon cards gallery
├── minecraft.html          # Minecraft screenshots gallery
├── admin/
│   ├── index.html          # Decap CMS admin interface
│   └── config.yml          # CMS configuration
├── data/
│   ├── collectibles.json   # Collectibles metadata
│   ├── pokemon.json        # Pokemon cards metadata
│   └── minecraft.json      # Minecraft screenshots metadata
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

### /admin - Decap CMS
Visual content management interface. Allows adding/editing items with image upload.

## How Content Works

1. JSON files in `data/` store metadata: `{items: [{filename, description, category}, ...]}`
2. JavaScript fetches JSON at page load
3. Images are dynamically rendered into category grids
4. Click any image to view enlarged in overlay

## Adding New Items

**Via Decap CMS (recommended):**
1. Go to www.theosstuff.ca/admin
2. Log in with GitHub
3. Select collection (Collectibles, Pokemon, or Minecraft)
4. Add new item with image upload
5. Save and publish

**Direct edit:**
1. Add image to appropriate folder (`images/`, `pokemon/`, or `minecraft/`)
2. Edit JSON file in `data/` folder
3. Commit and push

## Style Notes

- Max width 1200px container
- Dark nav bar (#333) with centered links
- Responsive grid: `repeat(auto-fill, minmax(250px, 1fr))`
- White cards with subtle shadow
- Hover scale effect on images
- Click-to-enlarge modal overlay

## Favicon

Uses `images/ammonite.jpeg` as the site favicon.

## Decap CMS Authentication

The CMS uses GitHub OAuth for authentication. To set this up, you need an OAuth authenticator. Options:
1. **Netlify hosting** (easiest) - Move site to Netlify, free and seamless
2. **External OAuth** - Use a service like `netlify-cms-oauth-provider-go` on a free host
