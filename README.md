# Game Codes & Launch Data Tracker

Daily-tracked video game redeem codes and launch-day facts, with **source
attribution and verification dates on every entry**. This repository is the
companion data set of [azgameguides.com](https://azgameguides.com) — the
human-readable, always-current pages live there:

- **AION 2 codes (verified daily):** https://azgameguides.com/codes
- **GTA VI launch hub:** https://azgameguides.com/gta6/

## What is in here

| File | Contents | Updated |
|---|---|---|
| `data/aion2.json` | Active/expired redeem codes for AION 2 with rewards, expiry and verification date | Daily (manual verification) |
| `data/gta6.json` | GTA VI launch facts: release date, platforms, editions, pre-order bonus window | On official announcements |
| `meta/last-check.txt` | UTC timestamp of the last automated freshness check | Daily (GitHub Actions) |

## Data methodology

Every entry carries a `source` field using one of three categories only:

1. **official** — publisher announcements, press releases, in-game notices
2. **public-data** — store listings, patch notes, platform pages
3. **community-report** — reputable player reports, labelled as such

We do not publish speculation, and we do not fabricate "hands-on" testing
claims. If a code cannot be tied to a source, it is not listed. Expired codes
are kept with their expiry dates as reference.

## Freshness automation

`.github/workflows/daily-check.yml` runs once a day (01:00 UTC) and refreshes
`meta/last-check.txt`. That workflow only records the timestamp — **code data
itself is updated manually** after verification, so a commit touching
`data/*.json` always corresponds to a human-reviewed change.

## License

Data files are provided under [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).
Game names and trademarks belong to their respective owners; this project is
unofficial and not affiliated with any publisher.
