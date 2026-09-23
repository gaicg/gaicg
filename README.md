# GAICG website redesign starter

This folder is a complete GitHub Pages/Jekyll redesign for `gaicg/gaicg`. It intentionally separates **content** from **presentation** so future updates are simple.

## What is included

- Responsive, sticky navigation with mobile menu
- Accessible typography, focus states, skip link and reduced-motion support
- Clinical/research-oriented colour system
- Homepage hero, project cards, publication list, collaboration CTA
- Dedicated project, team, publications, collaborators and contact layouts
- SEO metadata, canonical URLs, Open Graph metadata and ResearchOrganization schema
- SVG/PNG favicon assets and a 1200×630 social sharing image
- Manual `sitemap.xml` and `robots.txt`
- Lightweight scroll-reveal animation that respects `prefers-reduced-motion`
- No external font, JS or CSS dependencies

## Important before deployment

Your repository already contains `assets/img/gaicg_logo.jpg`. This redesign does not need to remove it; keep that file if you want to reuse the existing illustrated GAICG logo elsewhere.

The public site currently lives at `https://gaicg.github.io/gaicg/`, so `_config.yml` is already set to:

```yaml
url: "https://gaicg.github.io"
baseurl: "/gaicg"
```

## Where to add content later

Most routine content lives in `_data/`:

- `_data/projects.yml` — project title, field, status, summary, optional link
- `_data/members.yml` — name, role, bio, initials and profile links
- `_data/publications.yml` — full citation information, PubMed and DOI
- `_data/collaborators.yml` — institutions, locations and descriptions
- `_data/navigation.yml` — main navigation

Global group information is in `_config.yml` under `organization:`.

Homepage text is in `index.html`. Contact-page placeholder text is in `contact.html`.

## Add profile links

Example inside `_data/members.yml`:

```yaml
links:
  - label: "ORCID"
    url: "https://orcid.org/..."
  - label: "PubMed"
    url: "https://pubmed.ncbi.nlm.nih.gov/?term=..."
```

## Add a publication

```yaml
- year: 2026
  items:
    - title: "Full article title"
      authors: "Surname A, Surname B, Surname C"
      journal: "Journal Name"
      meta: "2026 · 12(3):100–108"
      pubmed: "https://pubmed.ncbi.nlm.nih.gov/..."
      doi: "https://doi.org/..."
```

## Deployment

1. Back up or create a branch from the current repository.
2. Copy these files into the repository root, merging rather than deleting any assets you want to keep.
3. Commit and push to `main`.
4. GitHub Pages should rebuild automatically.
5. Check the live site on desktop and mobile.

No custom GitHub Action is required for this version.

## Optional next steps

- Replace the `G` brand mark in `_includes/header.html` with a compact SVG version of the official GAICG logo.
- Add professional team photos and institutional logos once permissions are confirmed.
- Add an About page if the group needs more history/methodology text than fits on the homepage.
- Add analytics only after deciding on privacy/cookie requirements.
