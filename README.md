# /ɔːlˈtəːnətɪv/ – digital library page

This is the page shown on the **Library** page of the Research Catalogue exposition /ɔːlˈtəːnətɪv/
(Fontys Academy of the Arts). It lists the reading, viewing and listening that people suggest through the
submission form, after review.

## You do not need to touch this to update the library

- New entries come in through the Google Form and land in the library spreadsheet.
- An entry appears here when its **Publish** box is ticked in the spreadsheet (within five minutes).
- Unticking hides it again. Typos are fixed directly in the spreadsheet row.

This repository only holds the page's design (`index.html`). It reads the published entries from the
spreadsheet's Apps Script every time someone opens it.

## Where things are

| Part | Where |
|---|---|
| Page (this repository) | `index.html`, published with GitHub Pages |
| Entries | Google spreadsheet "/ɔːlˈtəːnətɪv/ – digital library", tab "Responses" |
| Data address | `DATA_URL` near the bottom of `index.html` (the spreadsheet's Apps Script, `?format=json`) |
| Shown in | Research Catalogue exposition 5004460, page "Library" (an iframe page pointing here) |

## Moving this to another GitHub account or organisation

Settings → General → Danger Zone → **Transfer ownership**. Then turn on Pages again in the new place
(Settings → Pages → Deploy from branch → `main`, `/ (root)`) and put the new address into the
Research Catalogue iframe page.

## Why the page lives here and not on Google

Google's own web-app page fails inside the Research Catalogue on phones that are signed in to Google
("Sorry, unable to open the file at this time"), and shows a Google banner to everyone else.
This page asks Google only for the data, without sign-in cookies, so it works on every phone.
