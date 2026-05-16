# DancingMusic.github.io

Official website for [DancingMusic](https://github.com/DancingMusic/DancingMusic) — a music visualization app with a plugin ecosystem.

## How it works

1. The main `DancingMusic` repo publishes a production build as a GitHub Release artifact (`dancingmusic-dist.tar.gz`).
2. This repo's GitHub Actions workflow downloads the latest release artifact and places it under `/app/`.
3. The landing page at `/` links to `/app/` where visitors can launch the full application.
4. GitHub Pages serves the assembled site at [dancingmusic.github.io](https://dancingmusic.github.io).

## Setup

The deploy workflow requires a `MAIN_REPO_TOKEN` secret — a GitHub personal access token (classic) with `repo` scope to read releases from the private `DancingMusic/DancingMusic` repository.

## Manual deploy

Trigger the workflow manually from the **Actions** tab → **Deploy to GitHub Pages** → **Run workflow**.
