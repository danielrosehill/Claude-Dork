# Claude-Dork

A Claude Code agent for generating batches of platform-specific search dorks.

## Project Structure

- `.claude/commands/generate-dorks.md` - Multi-network dork generation (prompts for network selection)
- `.claude/commands/generate-{network}-dorks.md` - Per-network slash commands
- `networks.json` - Network definitions with URL templates, Boolean operators, and dork patterns
- `input/` - Place keyword/topic input files here (one keyword per line)
- `output/` - Generated CSV dork files are written here

## Slash Commands

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

## Output Format

CSV files with columns: `keyword`, `dork_query`, `search_url`, `description`
Combined `all_dorks.csv` includes an additional `network` column.

Output files: `{network}_dorks.csv` (e.g., `google_dorks.csv`, `reddit_dorks.csv`)

## Adding Networks

Add new network definitions to `networks.json` following the existing schema, then create a corresponding slash command in `.claude/commands/`.
