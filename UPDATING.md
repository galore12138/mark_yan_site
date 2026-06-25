# Updating This Website

This site is a Hugo academic website for Mark (Yuzhi) Yan. Most content is stored in small YAML files under `data/`, so routine updates do not require editing templates.

## Common Updates

### Update the biography

Edit `content/_index.md`. The first section is the longer bio used on the homepage's Bio & C.V. section. Keep the short homepage intro in `layouts/index.html` distinct from the longer bio.

### Add or update a paper

Edit `data/papers.yaml`. Copy an existing entry and update:

```yaml
- title: "Paper Title"
  authors: "Author One, Author Two, and Mark (Yuzhi) Yan"
  year: 2026
  status: "Under review"
  venue: "Journal Name"
  type: "Working paper"
  area: "Debt contracting"
  description: "Optional one-sentence description."
```

Use one of the existing research areas when possible so the paper can appear in the right topic accordion.

### Add a conference presentation

Edit `data/talks.yaml` and add:

```yaml
- year: 2026
  title: "Conference Name"
  role: "Presenter"
```

The `role` line is optional.

### Update teaching

Edit `data/teaching.yaml`. Add new course evaluations under the relevant course.

### Update co-authors

Edit `data/coauthors.yaml`. The People section is auto-populated from this file. Co-author links should be reviewed before public launch; add links only when you are confident they point to the correct person.

### Replace the CV

Replace `static/files/mark-yan-cv.pdf` with a new PDF using the same filename.

### Replace the portrait

Replace `static/images/mark-yan.jpg` with a square portrait image. A 480 x 480 or 720 x 720 JPEG is ideal.

## Build Locally

From the repository root:

```bash
hugo --gc --minify
```

For local preview:

```bash
hugo server --disableFastRender
```

## Deployment

The repository includes `.github/workflows/deploy.yml` for GitHub Pages. The workflow builds Hugo, runs Pagefind indexing, and publishes the `public/` artifact. Review the local preview before pushing changes to `main`.
