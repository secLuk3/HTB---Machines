# HTB PDF Writeups — Progress Tracker

This repository is **only** for storing PDF writeups of Hack The Box machines as a personal progress tracker. The README is focused on clear conventions for naming, organizing, and tracking solved machines in PDF form.

---

## Purpose

* Centralize **PDF** writeups.
* Keep an auditable record of machines you've worked on and your progress over time.
* Make it easy to browse, backup, and measure completion rates.

---

## Example tracker table

Below is a simple Markdown table you can keep in the README (or export from `index.csv`) to quickly see your progress. It lists machine name, difficulty, and whether you have the user and root flags.

| Date       | Machine  | Difficulty | User flag | Root flag |
| ---------- | -------- | ---------- | --------- | --------- |
| 2025-10-02 | Editor   | Easy       | ✅         | ✅         |

You can update this table manually.

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
```

---

## File naming convention

Use `Machine-name-(difficulty).pdf` for solved machines and `Machine-name-wip-(difficulty).pdf` for in-progress notes. Example:

* `Editor-(Medium).pdf`
* `Editor-wip-(Medium).pdf`

This keeps files ordered and easy to scan.

---

## How to add a new PDF

1. Place the PDF in `writeups/<year>/<solved|in-progress>/` with the correct filename.
2. Commit with a clear message: `Add: 2025-09-01 - Editor (solved)`.

---

## Progress tracking ideas

* Add a `status` column with values: `in-progress`, `abandoned`, `solved`.
* Optionally add `time_spent_minutes` to track how long each machine took.
* Add a `tags` column for skills practiced (e.g., `web, priv-esc, ssh`).

---

## Privacy and scope

* Only add writeups for lab machines you solved in HTB or other legal, CTF environments.
* Do **not** include sensitive corporate data, real customer info, or active exploit payloads that could be abused.

---

Happy hacking!

