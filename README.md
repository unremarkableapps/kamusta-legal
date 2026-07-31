# kamusta-legal

Public legal pages for **Kamusta**, a family check-in app by **unremarkableapps**.

This repo exists to be public. The app's source lives in a separate, private
repo — nothing here should ever contain code, keys, or anything not intended
for the open web.

Served by GitHub Pages from the `main` branch, root folder:

| Page | URL |
| --- | --- |
| Index | `https://unremarkableapps.github.io/kamusta-legal/` |
| Account &amp; data deletion | `https://unremarkableapps.github.io/kamusta-legal/delete-my-data.html` |
| Privacy policy | `privacy-policy.html` — not added yet |

The deletion URL is the one submitted to Google Play, which requires it to be
reachable **without any login**.

## Adding a page

Drop the `.html` file in the repo root, add a link in `index.html` (there is a
commented-out line ready for the privacy policy), commit, push. Pages redeploys
on push; no build step, no dependencies, no framework.

Keep the palette and structure consistent with `delete-my-data.html`: terra
`#AF583C`, deep `#94472F`, ink `#402B26`, cream `#F9F6ED`, card `#FFFEF9`,
gray `#8E8B85`, line `#E8E1D3`. No red anywhere.

## Keeping in sync

`delete-my-data.html` is a COPY. The canonical version lives in the app repo at
`legal/delete-my-data.html`, next to the `deleteAccount` callable it describes,
so that changing what deletion actually does and changing what the page claims
happen in the same place. If you edit one, edit both — a page that overstates
what is erased is a compliance problem, not a typo.
