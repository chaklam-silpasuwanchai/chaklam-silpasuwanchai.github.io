# Chaklam.com — Jekyll migration candidate

This is a **local migration package only**. No GitHub branch, PR, or live website was modified.

## Edit content

- `_data/news.yml`: all news, newest first
- `_data/grants.yml`: grants, PI/Co-PI, funder, amount
- `_data/talks.yml`: invited talks
- `_data/services.yml`: grouped academic services
- `_data/collaboration.yml`: industry collaborations
- `_data/teaching.yml`: courses and links
- `_data/awards.yml`: awards
- `_data/selected_publications.yml`: homepage selected publications
- `_data/publications.yml`: complete publication list
- `_articles/<slug>.md`: 27 migrated articles; edit Markdown here; clean `/articles/<slug>/` links
- `index.html`: homepage template and biography
- `blog.html`: archive template

## Build

Install Jekyll and run `bundle exec jekyll serve` (if using a Gemfile) or `jekyll serve`. GitHub Pages can process this Jekyll project on deployment. **Do not open the source `index.html` directly**; Liquid templates must be rendered by Jekyll.

## Important migration checks

- Blog articles were recovered from the 27 `node/*.html` pages present in the connected repository (main tree checked October 9, 2026). The Markdown conversion was produced from the original snapshot and should be visually reviewed, especially images and embedded links.
- Old `/node/` links are retired; all articles use clean `/articles/<slug>/` URLs.
- The original HTML course pages and image assets are retained.
- Publications and grant values should be cross-checked against the latest CV before deployment; previously identified grant discrepancies remain unresolved.
- The supplied snapshot has no trustworthy blog dates; articles are listed without invented dates.
- Do not push to `main` until Jekyll rendering and link checks pass.
