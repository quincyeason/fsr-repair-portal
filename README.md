# FSR Repair Portal

Static single-page site for Fresh Start Rentals machine repairs. No build
step, no backend, no Netlify — GitHub Pages serves `index.html` as-is.

## Data (live, not in this repo)

- State (Delivered / Completed / Complaint / Parts / Labor / picked_up):
  Google Sheet "FSR – Repair Portal State", tab "State" — read as CSV.
- History: same sheet, tab "History".
- Saves: Google Form (repair completion form) — the page POSTs to it with
  `fetch(..., { mode: "no-cors" })`; the hourly watch script reads the form
  responses back into the sheet.

## Editing

Edit `index.html`, commit, push to `main`. Pages publishes the push
automatically. The machine list is baked into the page; completed/delivered/
complaints/parts/labor/history all come from the sheet, so most day-to-day
changes need no edit at all.

## Live URL

https://quincyeason.github.io/fsr-repair-portal/
(previous host: https://animated-figolla-936e90.netlify.app — do not delete
until the cutover is confirmed)
