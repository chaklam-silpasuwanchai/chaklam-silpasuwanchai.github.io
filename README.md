# Chaklam.com — website editing guide

This repository is the source for **https://chaklam.com**. GitHub Pages publishes the Jekyll website when changes are pushed to the branch configured in **GitHub → Settings → Pages**.

## What to edit

| To change | Edit |
| --- | --- |
| Biography and homepage layout | `index.html` |
| News | `_data/news.yml` |
| Publications | `_data/publications.yml` and `_data/selected_publications.yml` |
| Grants | `_data/grants.yml` |
| Teaching | `_data/teaching.yml` |
| Talks | `_data/talks.yml` |
| Service | `_data/services.yml` |
| Awards | `_data/awards.yml` |
| Collaborations | `_data/collaboration.yml` |
| Article content | `_articles/<article-name>.md` |
| Blog listing layout | `blog.html` |
| Website styling | `styles.css` |
| Sidebar/profile photo | `_includes/sidebar.html` and `assets/profile/chaklam.png` |
| Menu | `_includes/navigation.html` |

## Add a new article

1. Create `_articles/my-new-article.md`.
2. Paste this content and replace the example text:

```markdown
---
title: My New Article
category: Blogs
---

Write your article here in Markdown.
```

3. Commit and push. The article appears on the blog listing and its URL becomes `https://chaklam.com/articles/my-new-article/`.
4. Use `category: Research Tips` instead if appropriate. Place images in `assets/article-images/` and link them with `/assets/article-images/image-name.png`.

**Do not use `_posts/`**: this website uses the `_articles/` collection. You do not need to edit `blog.html` to add an article.

## Important technical files

- `CNAME` must stay: it connects GitHub Pages to the `chaklam.com` custom domain. Do not delete it.
- `_config.yml` configures Jekyll and article URLs. Normally leave it alone.
- `robots.txt` tells search crawlers that public pages may be crawled; it is not a security control.
- `.gitignore` prevents local temporary/build files from being committed.

## Troubleshooting

- **Changes not visible?** Check GitHub **Actions** for the latest Pages deployment, then hard-refresh or open a private window.
- **Broken article link?** Use `/articles/<markdown-filename-without-.md>/`.
- **Broken image?** Check exact spelling and capitalization of the path in `assets/`.
- **Custom domain stops working?** Confirm `CNAME` still contains `chaklam.com` and check GitHub **Settings → Pages**.