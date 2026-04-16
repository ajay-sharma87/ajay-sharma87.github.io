# Ajay Sharma — Academic Website

## How to edit content (no coding needed)

All your content lives in simple text files in the `_data/` folder.

| What to edit | File to open |
|---|---|
| Bio & research interests | `_data/profile.yml` |
| Publications | `_data/publications.yml` |
| Positions, education, grants | `_data/cv.yml` |
| Teaching courses | `_data/teaching.yml` |
| Name, email, profile links | `_config.yml` |

### Adding a new publication
Open `_data/publications.yml` and paste this at the top of the relevant list:
```yaml
- title: "Your Paper Title"
  authors: "with Co-author Name"
  journal: "Journal Name"
  details: "2025, 10(2), 100–120"
  link: "https://doi.org/..."
  wp: "https://arxiv.org/..."
```
Delete `link:` or `wp:` lines if not available. Use `year: forthcoming` for forthcoming papers.

### Adding your photo
1. Upload `photo.jpg` to the repo root
2. In `index.md`, find `<div class="photo-placeholder">...</div>` and replace with `<img src="photo.jpg" alt="Ajay Sharma">`

### Adding your CV
Upload `cv.pdf` to the repo root — the download button works automatically.

## Publishing changes
Edit any file on GitHub → click **Commit changes** → site rebuilds in ~1 minute.
