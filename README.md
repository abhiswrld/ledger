# Ledger

A single-file job application tracker.

[![Vercel](https://vercelbadge.vercel.app/api/abhiswrld/ledger)](https://myledgerweb.vercel.app)

## What it does

Track job applications through four stages — applied, interview, offer, rejected — with notes, next steps, salary, source, location, and a link back to the posting for each entry. Includes search, filtering by stage, sorting, and a summary breakdown of where things stand.

## Find Jobs

A second tab pulls live internship listings straight from [SimplifyJobs' Summer2027 Internships repo](https://github.com/SimplifyJobs/Summer2027-Internships), parsing the tables out of its README on the fly — no backend, no API key.

- Listings are cached in `localStorage` for 6 hours and refreshed automatically when stale, or on demand with the refresh button.
- Filter by category, search, and sort by newest, company, repo order, or **Suggested for you**.
- Suggestions are scored by a weighted-matching heuristic (not an ML model): it builds a profile from the words in your own ledger's role titles, companies, and categories — weighting entries that reached interview or offer more heavily than plain applications, and rejections negatively — then ranks open listings against it and explains its picks in plain language.
- Hitting "Apply" on a listing pre-fills a new ledger entry with the role, company, location, and posting link, so logging it takes one click. Listings already in your ledger are marked "In ledger."

## Stack

HTML, CSS, and vanilla JavaScript. One file, no build step, no dependencies, no server.

## How it works

- Data is stored in the browser's `localStorage`, scoped per account name. Nothing leaves your device.
- Create an account with just a name — no password, since there's nothing worth protecting on a local file.
- Keep multiple ledgers on one device — switch between saved accounts, and rename or delete any of them from the account picker.
- Export your data as a JSON backup anytime; import it back on another browser or after clearing storage. Re-importing your own backup is a no-op (it merges by ID instead of duplicating).
- A "sample ledger" preview mode lets you try the app without writing to your real data.
- Open tabs stay in sync — an edit in one tab (ledger entries or the job board cache) updates the others.

## Running it

Open `index.html` in a browser, or use the live demo above.
