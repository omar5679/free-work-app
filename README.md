# PPL Workout Tracker

A self-contained, mobile-first workout tracker for a 5-day Push/Pull/Legs/Upper/Lower split.
Single HTML file, no dependencies, no build step — all logic runs in the browser and data
lives in `localStorage`.

**Live app:** published as a private [Claude Artifact](https://claude.ai/code/artifact/dc7c853f-8266-4ba2-9adb-83eec8f44944)
(any static host works — it's one file).

## Features

- **12-week program built in**: 3 phases × 4 weeks, exercises rotate each phase, every
  exercise has two swap alternatives
- **One-tap set logging** with last-session numbers and double-progression load suggestions
  (+5 lb upper / +10 lb lower when you top the rep range)
- **Pull-up progression from zero**: assisted machine work + negatives with milestone tracking
- **Rest timer** — auto-starts on set completion, wall-clock anchored so it survives app
  switching and reloads; per-exercise manual timer button
- **Estimated 1RM charts** (Epley) so progress compares across rep ranges, plus PRs and a
  weekly consistency streak
- **Gym-floor QoL**: persistent per-exercise notes (machine settings), short-session mode
  that hides optional exercises, keep-screen-awake toggle, warm-up calculator on the big lifts
- **Backup/restore** via JSON export-import (localStorage is per-device)

## Usage

Open `tracker.html` in any modern browser. On a phone, "Add to Home Screen" for an
app-like experience. Data is stored per browser — export a backup from the Settings tab
before switching devices.

## Development

Plain HTML/CSS/JS in one file. Edit `tracker.html`, reload, done.

## Goals
- Move browser hosting to persistent DB, probably self hosted
- Some UI changes, better tracking of weight loss goals, perhaps a dashboard to view historical data
