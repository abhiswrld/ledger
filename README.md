# Ledger

A single-file job application tracker.

[![Vercel](https://vercelbadge.vercel.app/api/abhiswrld/ledger)](https://myledgerweb.vercel.app)

## What it does

Track job applications through four stages — applied, interview, offer, rejected — with notes, next steps, salary, source, and location per entry. Includes search, filtering by stage, sorting, and a summary breakdown of where things stand.

## Stack

HTML, CSS, and vanilla JavaScript.

## How it works

- Data is stored in the browser's `localStorage`, scoped per account name. Nothing leaves your device.
- Create an account with just a name — no password, since there's nothing worth protecting on a local file.
- Export your data as a JSON backup anytime; import it back on another browser or after clearing storage. Re-importing your own backup is a no-op (it merges by ID instead of duplicating).
- A "sample ledger" preview mode lets you try the app without writing to your real data.
- Open tabs stay in sync — an edit in one tab updates the others.

## Running it

Open `index.html` in a browser, or use the live demo above.

## Coming soon

- **A live internship feed.** Pull open roles directly from public trackers like [SimplifyJobs' Summer2027 Internships list](https://github.com/SimplifyJobs/Summer2027-Internships), parsed straight from the repo's README. Browse them alongside your ledger and add one to your tracker in a click.
- **Suggestions based on your own history.** Surface open roles that look like the ones that got you interviews or offers before (by company, title, or location), and flag ones that resemble past rejections using a weighted-matching heuristic.

## Repo

[github.com/abhiswrld/ledger](https://github.com/abhiswrld/ledger)