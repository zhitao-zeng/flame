# AI Berkshire 投研 Skills

Installed from [xbtlin/ai-berkshire](https://github.com/xbtlin/ai-berkshire) (MIT License, © 2026 xbtlin).

A value-investing research framework combining the methodologies of Warren Buffett,
Charlie Munger, Duan Yongping (段永平), and Li Lu (李录) with multi-agent AI analysis.

## What was installed

- **`.claude/commands/*.md`** — 18 slash commands (the "skills"). In Claude Code,
  invoke them with `/<name>`, e.g. `/investment-research 贵州茅台`.
- **`tools/*.py`, `tools/*.sh`** — helper scripts the commands reference
  (financial-rigor checks, report auditing, screeners, scrapers, backtests).

## Available commands

| Command | Purpose |
|---|---|
| `/investment-research` | Full Buffett–Munger–Duan–Li 7-module company research |
| `/investment-team` | Multi-agent investment team analysis |
| `/investment-checklist` | Investment decision checklist |
| `/deep-company-series` | Deep-dive company report series |
| `/private-company-research` | Research for unlisted / private companies |
| `/management-deep-dive` | Management quality & capital-allocation review |
| `/earnings-review` | Single earnings report review |
| `/earnings-team` | Multi-agent earnings review |
| `/financial-data` | Pull & analyze financial data |
| `/industry-research` | Industry / sector research |
| `/industry-funnel` | Industry screening funnel |
| `/quality-screen` | Quality-company screen |
| `/bottleneck-hunter` | Find business bottlenecks / chokepoints |
| `/thesis-tracker` | Track an investment thesis over time |
| `/portfolio-review` | Portfolio review |
| `/news-pulse` | News / sentiment pulse |
| `/dyp-ask` | Duan Yongping-style Q&A |
| `/wechat-article` | Draft a WeChat research article |

## Local adjustment

The upstream commands hard-code helper-script paths as `~/ai-berkshire/tools/...`
(assuming the repo is cloned at `~/ai-berkshire`). Since the scripts live in this
project's `tools/` directory, all 28 such references were rewritten to the
project-relative `tools/...` so the commands work out of the box from the repo root.

## Dependencies

The Python tools rely only on the standard library plus **Playwright** (for web
scraping). Install browsers with your environment's Playwright setup if needed.

## Updating

Re-fetch from the upstream repo's `skills/` and `tools/` directories, or run the
upstream installer:

```bash
git clone https://github.com/xbtlin/ai-berkshire.git
cd ai-berkshire && ./scripts/install-claude-commands.sh   # copies skills/*.md to ~/.claude/commands
```
