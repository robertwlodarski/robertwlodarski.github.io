# robertwlodarski.github.io

Personal academic website, live at https://robertwlodarski.github.io.
Built with Jekyll on the [Academic Pages](https://github.com/academicpages/academicpages.github.io) template.

## What to edit

| What | Where |
| --- | --- |
| Home page text | `_pages/about.md` |
| Research page | `_pages/research.md` |
| CV (linked from the menu and home page) | `files/` — if you rename the PDF, update the link in both `_pages/cv.md` and `_pages/about.md` |
| Profile photo | `images/profile.jpg` (about 525px wide) |
| Browser-tab icon | `images/favicon*`, `images/apple-touch-icon-180x180.png` |
| Name, email, social links | `_config.yml` → `author` |
| Accent colour (links, highlights) | `_config.yml` → `accent_color`, `accent_color_dark` |
| Menu links | `_data/navigation.yml` |

`_originals/` holds the full-size photo and logo. It is git-ignored, so it never gets published.

## What not to edit

`_theme/` (layouts, includes, styles) and `assets/` (fonts, scripts, compiled CSS) are the template's machinery.
VS Code opens them read-only (see `.vscode/settings.json`). `assets/` has to stay at the top level because its path is part of the site's URLs.

## Previewing locally

Ruby 3.3 is installed via Homebrew (`brew install ruby@3.3`) and the gems live in `vendor/` (git-ignored).
The `github-pages` gem builds with the same Jekyll version and settings as the live site.

First time only:

```bash
/opt/homebrew/opt/ruby@3.3/bin/bundle install
```

Then start the preview server:

```bash
/opt/homebrew/opt/ruby@3.3/bin/bundle exec jekyll serve --livereload
```

Open http://localhost:4000. Saving a file refreshes the page automatically.
Changes to `_config.yml` need a server restart (Ctrl+C, then run it again).
