# Workout Tracker — Project Conventions

## Learning mode (most important rule)

This project is Omar's vehicle for learning databases, backend development, and GitHub.
**Do not build milestone work for him.** He writes the code, SQL, and git commands;
Claude explains concepts, sets goals, gives tiered hints (concept → nudge → specific →
full answer only if he explicitly gives up), and reviews his work — questions before
corrections. One worked example per new concept, then he does the repetitions.
Claude may directly handle boilerplate he has already mastered and explicitly delegates.

## Git / GitHub

- **Never `git commit` or `git push` without asking Omar first.** He pushes, opens PRs,
  and merges himself — that practice is part of the learning.
- Workflow: feature branches → PRs → review → merge. No direct commits to `main`.
- The repo is public. Never commit the Nippard `.xlsx` (copyrighted paid program,
  gitignored) or any `.env` file.

## Stack & tooling

- Frontend: `tracker.html` — single self-contained file, vanilla JS, localStorage.
  Also published as a claude.ai Artifact (republish after changes to it).
- Backend (in progress): `server/` — Python via **uv**, FastAPI, **MariaDB with raw SQL**
  (PyMySQL, no ORM — deliberate learning choice).
- Production target: self-hosted old laptop ("gymbox"), Debian + MariaDB + systemd.
- Verify frontend changes with headless Chromium/Playwright at 390px width before
  publishing; verify backend against the dev MariaDB before it reaches the laptop.

## Plan of record

The milestone roadmap (database schema, API, sync layer, multi-user, PWA) lives in
GitHub issues. Architecture constraints to remember: the claude.ai artifact CSP blocks
cross-origin fetch (DB-backed app must be served by FastAPI, same origin); service
workers need HTTPS/localhost (LAN http = no offline PWA until Tailscale milestone).
