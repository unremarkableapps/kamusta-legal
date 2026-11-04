# kamusta-legal

Public legal pages for **Kamusta**, a family check-in app by **Rica R. Redonia**.

This repo exists to be public. The app's source lives in a separate, private
repo — nothing here should ever contain code, keys, or anything not intended
for the open web.

Served by GitHub Pages from the `main` branch, root folder:

| Page | URL |
| --- | --- |
| Index | `https://unremarkableapps.github.io/kamusta-legal/` |
| Account &amp; data deletion | `https://unremarkableapps.github.io/kamusta-legal/delete-my-data.html` |
| Privacy policy | `https://unremarkableapps.github.io/kamusta-legal/privacy-policy.html` |

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

`delete-my-data.html` and `privacy-policy.html` are COPIES. The canonical
versions live in the app repo under `legal/`, next to the code they describe —
so that changing what the app actually collects and changing what the pages
claim happen in the same place. If you edit one, edit both. A page that
overstates what is erased, or understates what is collected, is a compliance
problem rather than a typo.

## Things that will make these pages wrong

Each of these silently invalidates a published claim, so revisit both pages:

- **Pasting real RevenueCat keys.** Billing is currently inert, so RevenueCat
  collects nothing and is deliberately not listed as a processor. The moment it
  is configured it collects device identifiers and subscriber attributes, and
  both this policy and the Play Data Safety form must be updated.
- **Adding analytics or crash reporting.** The policy states plainly that there
  are none. Verified against the shipped APK on 2026-07-31.
- **Changing the Firestore region.** The policy names Singapore
  (`asia-southeast1`) as the location of the database, and the data processing
  agreement with Google as what covers sending information outside the country.
- **Widening distribution beyond the Philippines.** The policy is written to a
  single regime, the Data Privacy Act, with the National Privacy Commission as
  the sole supervisory authority. Distributing into territories with their own
  data-protection regimes is a question for the lawyer before the release, not
  after it.
