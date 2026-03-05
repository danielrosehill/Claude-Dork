[![Claude Code Repos Index](https://img.shields.io/badge/Claude%20Code-Repos%20Index-blue?style=flat-square&logo=github)](https://github.com/danielrosehill/Claude-Code-Repos-Index)

# Claude-Dork

A Claude Code agent for generating batches of platform-specific search dorks.

## Overview

Claude-Dork provides slash commands for generating search dorks across multiple platforms. It takes keyword input files and produces CSV files containing ready-to-use search queries with URLs.

## Supported Networks

| Command | Network |
|---------|---------|
| `/generate-dorks` | All networks (interactive selection) |
| `/generate-google-dorks` | Google |
| `/generate-reddit-dorks` | Reddit |
| `/generate-facebook-dorks` | Facebook |
| `/generate-twitter-dorks` | Twitter/X |
| `/generate-bluesky-dorks` | Bluesky |
| `/generate-linkedin-dorks` | LinkedIn |
| `/generate-youtube-dorks` | YouTube |
| `/generate-github-dorks` | GitHub |

## Usage

1. Place keyword files in `input/` (one keyword per line)
2. Run a slash command (e.g., `/generate-google-dorks`)
3. Find generated CSV files in `output/`

## Output Format

CSV files with columns: `keyword`, `dork_query`, `search_url`, `description`

Combined `all_dorks.csv` includes an additional `network` column.

## Adding Networks

Add new network definitions to `networks.json` following the existing schema, then create a corresponding slash command in `.claude/commands/`.

---

For more Claude Code projects, visit [my Claude Code Repos Index](https://github.com/danielrosehill/Claude-Code-Repos-Index).
