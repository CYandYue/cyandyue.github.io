# Yue Chang's Site Entry

This static entry page is intended for `https://cyandyue.github.io/`. The full
academic homepage stays at `https://cyandyue.github.io/HomePage/`; publications
and news continue to be maintained in the `HomePage` repository only.

## Publishing

Publish these files to a repository named `CYandYue/cyandyue.github.io`, then
enable GitHub Pages in **Settings > Pages** using **Deploy from a branch**,
the publishing branch, and the `/(root)` folder. No build step is needed.

The old repository URL currently redirects to `CYandYue/CY-Blog`. Do not rename
or overwrite that blog repository. Creating a new repository under the old
name will replace GitHub's old-name redirect for that repository URL.

Before publishing, verify that this directory will be hosted at the root URL,
not under `/HomePage/` or another project path. The root page should return
HTTP 200 and remain crawlable. Its canonical URL points to itself, while the
academic homepage retains its existing canonical URL.

The page provides `WebSite` structured data and `og:site_name` with the preferred
name configured in `index.html`. It references the existing homepage favicon, so no
second image copy needs to be maintained. This is a site-name preference for
Google, not a guarantee of the search result wording.

After deployment, use a Search Console property covering the root URL to
request indexing of `https://cyandyue.github.io/`. A URL-prefix property limited
to `/HomePage/` does not cover the root page. Google must recrawl and process
the root page before the search site name or icon can change.
