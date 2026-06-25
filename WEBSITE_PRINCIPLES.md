# Website Principles

This repository holds a maintainable academic website for Mark (Yuzhi) Yan.

## Content

- The information form and CV are the source of truth for the initial build.
- Short homepage copy and the longer bio should stay distinct.
- Research papers live in `data/papers.yaml`.
- Conference appearances live in `data/talks.yaml`.
- Teaching records live in `data/teaching.yaml`.
- Co-authors live in `data/coauthors.yaml`.

## Design

- The visual language is warm, restrained, and academic.
- The homepage hero uses the standard academic layout: portrait on the left, identity and intro text on the right.
- Navigation uses the owner's full name as the brand and keeps page sections easy to scan.
- Research areas appear as compact accordions so the homepage stays readable.
- The site uses local images and files rather than hotlinking.

## Build

- Hugo generates the static site.
- GitHub Actions publishes the site to GitHub Pages after changes are pushed to `main`.
- Pagefind is included in the deployment workflow for static search indexing.

## Review Before Public Launch

- Check every co-author name and any future links before publishing.
- Confirm the CV is current.
- Confirm the portrait has permission to be used publicly.
- Run a local build and preview before pushing to `main`.
