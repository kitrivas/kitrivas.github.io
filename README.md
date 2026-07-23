# kitrivas.com

The author landing page for Kit Rivas, served at the apex domain
`kitrivas.com` (this is the `kitrivas.github.io` user-page repo). Built with
[Jekyll](https://jekyllrb.com/). The visual design is unchanged from the
original single-file page — Jekyll just splits the shared page chrome and the
list of works out of the hand-written HTML so content is edited in one place.

## Structure

```
CNAME                  kitrivas.com (custom domain)
_config.yml            Site settings (title, description, font link)
_layouts/default.html  Page skeleton (<head>, body, footer)
_includes/
  head.html            <meta>, Open Graph, fonts, CSS link
  footer.html          Social links
_data/works.yml        The "Works" cards — edit this to add/change a work
css/site.css           All styles (moved out of the old inline <style>)
index.html             Front matter + page body (the works loop lives here)
music.json             Data asset, passed through untouched
```

## Add or change a work card

Edit `_data/works.yml`. Each entry becomes one card, top to bottom:

```yaml
- title: "Elanthira"
  type: "Series &middot; Epic Fantasy"
  desc: "One or two sentences."
  url: "elanthira/index.html"   # or "#" until it has its own site
```

No HTML editing needed — `index.html` loops over this file.

## Run it locally

```
bundle install          # first time
bundle exec jekyll serve
```

Then open http://localhost:4000/ .

## Deploying

This is a GitHub user-page repo, so GitHub Pages builds it automatically on
every push to `main` (default "Deploy from a branch" mode runs Jekyll for
`username.github.io` repos — no extra workflow needed). Just push to `main`.
