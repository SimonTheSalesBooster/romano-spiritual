# Romano Spiritual

Romano is a Claude Code skill that runs an evening spiritual check-in at 18:30. Based on Romano Guardini's 17 virtues, it sorts the day's stress into Body (Ben handles) and Soul (give to Jesus), then picks the one virtue most relevant to today's hardest decision.

## Setup

1. Copy `romano-evening.md` to `~/.claude/commands/romano-evening.md`
2. Copy `.env.example` to `~/.claude/.env` and fill in your keys
3. Run `/romano-evening` from Claude Code

## Required Environment Variables

- `DISCORD_WEBHOOK_MARCUS` .. Discord webhook URL for evening reflections channel

## Optional Environment Variables

- `OBSIDIAN_VAULT_PATH` .. path to your Obsidian vault for Board Meeting files
- `GMAIL_CONFIGURED` .. set to `true` if Gmail MCP is connected

## MCP Integrations

- **Whoop MCP** .. pulls recovery, HRV, and strain for stress biomarkers
- **Google Calendar MCP** .. reads today's schedule density

## What It Does

Each run:
1. Reads today's Board Meeting file from Obsidian (all personas, all debates, all decisions)
2. Reads Ben Health data (morning + evening) for physical stress signals
3. Pulls fresh Whoop biometrics (recovery, HRV, strain)
4. Checks Google Calendar for schedule density
5. Sorts every stress source into Body or Soul
6. Picks the ONE virtue from Guardini's 17 most relevant to today
7. Crafts a closing sentence of peace
8. Posts to Discord
9. Logs to Obsidian Board Meeting file

## The 17 Virtues

Truthfulness, Acceptance, Patience, Justice, Reverence, Loyalty, Disinterestedness, Asceticism, Courage, Kindness, Understanding, Courtesy, Gratitude, Unselfishness, Recollection, Silence, Justice before God.

## Voice

Warm, grounded in faith, never preachy. Scripture flows from conviction, not decoration. Gentle, not corporate.. a trusted pastor sitting across the table after a long day.

## Customization

Edit the voice, virtues emphasis, and Scripture preferences in `romano-evening.md` to match your spiritual tradition.
