# HTB PDF Writeups — Progress Tracker

This repository is **only** for storing PDF writeups of Hack The Box machines as a personal progress tracker. The README is focused on clear conventions for naming, organizing, and tracking solved machines in PDF form.

---

## Purpose

* Centralize **PDF** writeups.
* Keep an auditable record of machines you've worked on and your progress over time.
* Make it easy to browse, backup, and measure completion rates.

---

## Recommended repository structure

```
/ (root)
├─ README.md
├─ writeups/                    # all PDFs organized by year and status
│  ├─ 2025/
│  │  ├─ solved/
│  │  │  ├─ 2025-09-01-boxname.pdf
│  │  │  └─ 2025-09-12-otherbox.pdf
│  │  └─ in-progress/
│  │     └─ 2025-09-20-wip-boxname.pdf
│  └─ 2024/
├─ index.csv                    # metadata and progress tracking (auto-updated)
└─ tools/                       # optional scripts to update index or generate stats
```
---

## File naming convention

Use `YYYY-MM-DD-machine-name.pdf` for solved machines and `YYYY-MM-DD-machine-name-wip.pdf` for in-progress notes. Example:

* `2025-09-01-forest.pdf`
* `2025-09-25-forest-wip.pdf`

This keeps files chronologically ordered and easy to scan.

---

## index.csv (recommended)

Keep a small CSV at the repo root to track metadata for each PDF. Columns suggested:

```
date, machine, htb_link, status, difficulty, notes, pdf_path
```

Example row:

```
2025-09-01, forest, https://www.hackthebox.eu/machines/forest, solved, Easy, initial foothold via nginx misconfig, writeups/2025/solved/2025-09-01-forest.pdf
```

You can update this manually or create a small script in `tools/` to add entries when you add a PDF.

---

## How to add a new PDF

1. Place the PDF in `writeups/<year>/<solved|in-progress>/` with the correct filename.
2. Add or update a row in `index.csv` with metadata and the relative path.
3. Commit with a clear message: `Add: 2025-09-01 - forest (solved)`.

---

## Progress tracking ideas

* Use `index.csv` to compute a completion rate per year or overall (number solved / number started).
* Add a `status` column with values: `in-progress`, `abandoned`, `solved`.
* Optionally add `time_spent_minutes` to track how long each machine took.
* Add a `tags` column for skills practiced (e.g., `web, priv-esc, ssh`).

---

## Privacy and scope

* Only add writeups for lab machines you solved in HTB or other legal, CTF environments.
* Do **not** include sensitive corporate data, real customer info, or active exploit payloads that could be abused.

---

Happy hacking!
