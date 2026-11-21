# Mikeybox Toolkit — download site

A static, dependency-free page for GitHub Pages. Everything the site needs is in
this folder:

| File | What it is |
| --- | --- |
| `index.html` | The whole site — styles and script inlined, relative links only |
| `mikeybox-toolkit-1.8.0.zip` | The unpacked extension, one `mikeybox-toolkit/` folder with `manifest.json` at its root |
| `tutorial.mp4` | 32-second install walkthrough (H.264, 1280×720) embedded on the page |
| `icon128.png` | Favicon and brand mark |

## Publish with GitHub Pages

1. Create a public repo, e.g. `mikeybox-toolkit`.
2. Put the contents of this folder at the repo root (`index.html` must be at the root).
3. Repo **Settings → Pages → Source: Deploy from a branch → `main` → `/ (root)` → Save**.
4. After a minute the site is live at `https://<your-user>.github.io/<repo>/`.

Every path on the page is relative, so it works from a project subpath without edits.

## Optional: attach the zip to a Release

The download button works from the repo files alone. A Release gives people a
stable "latest" link as well:

1. **Releases → Draft a new release**, tag `v1.8.0`.
2. Attach `mikeybox-toolkit-1.8.0.zip` and publish.
3. In the release notes, tell people to use the attached zip — **not** the green
   *Code → Download ZIP* button, which packs the source repo instead of the build.

## Updating to a new version

1. Rebuild the extension zip (keep the top-level `mikeybox-toolkit/` folder).
2. Replace the old zip here and update the file name in `index.html`
   (download button, install step 1, footer) plus the SHA-256 in the footer.
3. Commit. Pages redeploys on push; the extension updates when users replace the
   folder contents and press reload on the extension card.

The SHA-256 in the footer is the first 32 hex characters of the zip's digest.
