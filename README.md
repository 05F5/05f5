# Open Source Founders Summit

The conference about building financially successful and sustainable open source companies.

**Website:** [https://05f5.com](https://05f5.com)

## About

The Open Source Founders Summit (OSFS) is an invitation-only conference that brings together founders and leaders of open source companies. The event features single-track morning talks and afternoon unconference workshops, with a focus on practical business topics — not just DevTools.

## Tech Stack

- **Static site generator:** [Jekyll](https://jekyllrb.com/) 4.3
- **Hosting:** GitHub Pages (built HTML served from `/docs`)
- **Ruby:** 3.4+

## Project Structure

```
├── _config.yml          # Jekyll configuration
├── _layouts/            # Page layout templates
├── _pages/              # Content pages (about, schedule, venue, etc.)
├── _participants/       # Participant profile entries
├── _sessions/           # Session/talk entries
├── _includes/           # Reusable snippets and partials
│   ├── common/          # Header, footer, head, footprints
│   └── snippets/        # Participant cards, session cards, etc.
├── assets/
│   ├── css/             # Stylesheets
│   ├── img/             # Images (participants, sponsors, logos, photos)
│   ├── fonts/           # Inter font family
│   └── files/           # PDFs (sponsorship brochures)
├── docs/                # Built site output (served by GitHub Pages)
├── Gemfile              # Ruby dependencies
├── CNAME                # Custom domain config
└── 404.md               # Custom 404 page
```

### Collections

The site uses three Jekyll collections (defined in `_config.yml`):

- **`_pages`** — Main site pages (home, about, schedule, venue, etc.)
- **`_participants`** — Individual participant/speaker profiles
- **`_sessions`** — Talk and workshop entries

## Local Development

### Prerequisites

- Ruby 3.4+
- Bundler

### Setup

```sh
bundle install
```

### Run locally

```sh
bundle exec jekyll serve
```

The site will be available at `http://localhost:4000`.

### Build

```sh
bundle exec jekyll build
```

Output goes to `/docs` (configured via `destination` in `_config.yml`).

## Deployment

The site is deployed via GitHub Pages, serving the static files from the `/docs` directory on the `main` branch. To deploy, build the site locally and push the updated `/docs` folder.