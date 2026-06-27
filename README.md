# DancingMusic.github.io

Root GitHub Pages deployment for [DancingMusic](https://github.com/DancingMusic/DancingMusic).

The homepage at <https://dancingmusic.github.io/> is the official download and
integration entry. This repository is the required GitHub Pages root repo for
the organization domain and also publishes the web app under `/app/`.

## How it works

1. The main `DancingMusic` repo publishes a production build as a GitHub Release artifact (`dancingmusic-dist.tar.gz`).
2. This repo's GitHub Actions workflow downloads the latest release artifact and places it under `/app/`.
3. The workflow publishes this repo's `index.html` and static assets as the root homepage at `/`.
4. The workflow writes root `releases.json` metadata from the main repository release.
5. GitHub Pages serves the assembled site at [dancingmusic.github.io](https://dancingmusic.github.io).

## Setup

The deploy workflow can use a `MAIN_REPO_TOKEN` secret to read release metadata.
The main repository is public, so the workflow falls back to `github.token` when
the secret is unavailable.

## Manual deploy

Trigger the workflow manually from the **Actions** tab → **Deploy to GitHub Pages** → **Run workflow**.

To update the homepage content, edit this repository's `index.html` and assets.

Public app packages are attached to releases in the main
`DancingMusic/DancingMusic` repository.
