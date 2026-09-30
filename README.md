# Yue Chang's Homepage Redirect

This static page redirects `https://cyandyue.github.io/` immediately to
`https://cyandyue.github.io/HomePage/` using an HTML meta refresh. JavaScript is
not required, and a visible link provides a fallback. The full academic
homepage, publications, and news continue to be maintained in the `HomePage`
repository only.

## Publishing

Publish these files to a repository named `CYandYue/cyandyue.github.io`, then
enable GitHub Pages in **Settings > Pages** using **Deploy from a branch**,
the publishing branch, and the `/(root)` folder. No build step is needed.

The old repository URL currently redirects to `CYandYue/CY-Blog`. Do not rename
or overwrite that blog repository. Creating a new repository under the old
name will replace GitHub's old-name redirect for that repository URL.

Before publishing, verify that this directory will be hosted at the root URL,
not under `/HomePage/` or another project path. The root page should return
HTTP 200 with the immediate client-side redirect; this is not an HTTP 301
response. Both its canonical and Open Graph URLs point to `/HomePage/`, which
retains its existing self-referencing canonical URL. Do not install this
redirect in the `HomePage` repository, since that would create a redirect loop.

The page provides `WebSite` structured data and `og:site_name` with the preferred
name configured in `index.html`. It references the existing homepage favicon, so no
second image copy needs to be maintained. Google may follow the redirect and
use the destination page rather than the root page's metadata. These settings
do not guarantee a change to the search site name or icon.

After deployment, check that opening the root URL reaches `/HomePage/`, then
request indexing of the academic homepage in Search Console. A root URL
reported as "Page with redirect" is expected and does not mean the academic
homepage has failed. Inspecting the root URL itself requires a Search Console
property covering it; a URL-prefix property limited to `/HomePage/` does not.
