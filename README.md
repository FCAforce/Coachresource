# FCA Sports Way Coach Guide

**Live site:** https://fcaforce.github.io/Coachresource/

A mobile-friendly coaching tool for FCA Sports Idaho Clubs, built from the *FCA Sports Way — FCA Coach Guide*:

- **Practice** – the guide's practice templates as a timeline; add drills to blocks; branded PDF with drill sheets
- **Drills** – searchable drill library with YouTube videos
- **Game Day** – game plan and pregame routine, lineup builder (saved roster, drag-and-drop batting order, FCA scorecard PDF), pitcher workload tracker, signs, live tracker
- **Devos** – staff-published devotionals plus a blank devo template
- **Resources** – philosophy, the Coach's Mandate, team goals, strategy, bunt defense, base running and more

It's a single static `index.html` with no build step; pushing to `main` deploys it to GitHub Pages (`.github/workflows/deploy.yml`).

## Adding drills, videos and devotionals (no code)

Staff manage shared content in the Google Sheet **FCA Sports Way — Coach Guide Content** (ID in `CONTENT_SHEET_ID` in `index.html`). Its **Start Here** tab explains everything. The sheet must be shared as *Anyone with the link → Viewer*.

## Data

Plans, rosters, lineups, devos and pitcher outings are saved in each coach's browser (localStorage). Outings carry stable ids and timestamps so team sharing can be added later.

## Third-party code

`vendor/` contains jsPDF 2.5.2 and jspdf-autotable 3.8.4 (MIT licenses alongside).
