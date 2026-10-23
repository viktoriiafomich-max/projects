# projects: SBC creative pages

HTML pages for ad creatives, served with GitHub Pages:

**Hub:** https://viktoriiafomich-max.github.io/projects/

## Layout

```
index.html        hub: search, filter by section, Open / Copy link / QR for every page
catalog.json      list of all published pages (the hub reads it)
.nojekyll         serve files as-is (no Jekyll build)
apps/<topic>/<YYYY-MM-DD>_<slug>/index.html     app imitations to screen-record on a phone
motion/<topic>/<YYYY-MM-DD>_<slug>/index.html   9:16 motion previews of the ad overlays
other/<topic>/<YYYY-MM-DD>_<slug>/index.html    everything else
```

A page's URL is its folder:
`https://viktoriiafomich-max.github.io/projects/<section>/<topic>/<YYYY-MM-DD>_<slug>/`

Hub links straight to one section: `…/projects/#apps`, `#motion`, `#other`.

## How pages get here
Claude Code publishes them from the local workspace (`/publish` skill) with the GitHub MCP. Each
publish is one commit with the page and the updated `catalog.json`. The source copy stays in the
local task folder (`tasks/<topic>/<task>/`).

## One-time setup: turn on GitHub Pages
1. Open **Settings → Pages** in this repository.
2. **Build and deployment → Source:** *Deploy from a branch*.
3. **Branch:** `main`, folder `/ (root)` → **Save**.
4. Wait about a minute, then open the hub link above.

The repository must stay **public** for Pages on a free plan, so anyone with a link can open
these pages. Don't put real personal data, credentials or internal-only material here.

## Recording an app mockup on a phone
Open the page on the phone (scan the QR on the hub), then *Share → Add to Home Screen* and launch it
from the home-screen icon. It runs full screen without the browser bar. Start the screen recording
and tap through the screens.
