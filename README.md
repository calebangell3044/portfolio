# Creative Hub

Personal portfolio site for creative projects - novels, games, music, and art.

## Admin Panel

Access at `/admin.html` (not linked publicly).

Features:
- Create, edit, and delete blog posts
- Add, edit, and delete chapters for each novel
- Edit page descriptions and content via YAML data files
- Manage gallery images

## Structure

```
_data/           # Editable content (YAML files)
  site.yml       # Home page content
  novels.yml     # Novel descriptions
  universe.yml   # Universe page content
  tcg.yml        # TCG Sim page content
  music.yml      # Music page content
  gallery.yml    # Gallery image list

_chapters/       # Novel chapters (Markdown)
  coronation/
  azure-sunrise/
  threads-of-the-soul/
  tormented-gems/

_posts/          # Blog posts (Markdown)

_layouts/        # Jekyll templates
_includes/       # Reusable components

novels/          # Novel landing pages
images/gallery/  # Gallery images
```

## Adding Content

### Blog Posts
Use the admin panel or create files in `_posts/` with format:
`YYYY-MM-DD-title-slug.md`

### Chapters
Use the admin panel or create files in `_chapters/[novel-name]/`:
`01-chapter-title.md`

### Gallery Images
1. Upload images to `images/gallery/`
2. Add entries to `_data/gallery.yml`

## Local Development

```bash
bundle install
bundle exec jekyll serve
```

## Deployment

Push to GitHub. GitHub Pages builds automatically.
