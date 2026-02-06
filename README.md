# Chen Lab Website

This is the Kenneth Chen lab website, built with [Quarto](https://quarto.org/) and deployed to [Netlify](https://www.netlify.com/). 

- Source content is written in `.qmd` files
- The site is rendered locally with Quarto
- Deployment is handled by `quarto publish netlify`
- Rendered output (`_site/`) is not tracked in Git

-----

## Common updates

### Add a new lab member

-   Add entry to `members/data/members.yml`
-   Add bio in `members/bios/`
-   Add photo in `members/photos/`

### Graduate a lab member

-   Remove entry from `members/data/member.yml`
-   Add entry to `members/data/alumni.yml`

### Update publications

-   Add BibTeX entry to `publications/publications.bib`

### Update navigation

- Edit `_quarto.yml` → `website.navbar`
- Navigation order is controlled in `_quarto.yml`, not by file order

### Update styles

- Edit `styles.css`

### Images

- Images should go in `images/` and be referenced with relative paths

### Do not need to edit

- `_site/` – generated output
- `_quarto/` – build cache
- `_publish.yml` – unless changing Netlify settings

-----

## Local Development

### Build/preview locally

``` bash
quarto render
quarto preview
```

### Deploy to Netlify

``` bash
quarto publish netlify
```

----- 

## Repository Structure

Key files and directories:

- `_quarto.yml` – site-wide configuration (navigation, theme, title)
- `_publish.yml` – Netlify site configuration (used by Quarto)
- `index.qmd` – homepage
- `research/` – research pages
- `members/` – lab members pages
- `publications/` – publications content
- `images/` – shared images
- `styles.css` – custom CSS overrides

Generated / ignored:
- `_site/` – rendered site output (do not edit)
- `_quarto/` – Quarto cache
- `.Rproj.user/` – local RStudio files
