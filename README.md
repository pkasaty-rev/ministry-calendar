# Christ Lincoln Ministry Calendar

The exec-and-pastoral team's planning calendar for FY 2026-27 — the immovable
dates the team plans around.

Published as a static site via GitHub Pages: <https://pkasaty-rev.github.io/ministry-calendar/>

## How It Works

1. The source of truth is `2026-27 Ministry Calendar.xlsx`, maintained in the
   Cowork Team vault.
2. A Python script (`dashboard/build.py` in the vault) reads the spreadsheet
   and renders three HTML files.
3. Running `python3 build.py --publish` copies those files into this repo,
   commits with a timestamped message, and pushes to GitHub.
4. GitHub Pages serves the files at the URL above.

Every page footer shows the last-updated timestamp, so anyone viewing knows
how fresh the data is.

## Files

- `index.html` — the Horizon View (rolling 13-week strip + full event list with filters, Major-Events-Only advisory banner, and a "Last updated" timestamp in Central time).

## Updating

From the vault:

```bash
cd "Work/Projects/Exec Planning Calendar/dashboard"
python3 build.py --publish
```

That single command rebuilds, copies, commits, and pushes. Refreshing the
GitHub Pages URL will show the new build within a minute or two.
