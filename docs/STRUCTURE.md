# Repo layout

How the repo is organized and who owns what. The scope itself is in the [README](../README.md).

```
BSEMC-PM-AI-Project01/
├── README.md               Scope of the project
├── CONTRIBUTING.md         How we work: branches, pull requests, AI rules
├── requirements.txt        Python packages
├── .env.example            Template for secrets (copy to .env, never commit .env)
├── config/                 Settings and the ticker list
├── src/
│   ├── monitoring/         Phase 1: news, events, macro
│   ├── data/               Phase 2: Google Finance scraper, daily performance
│   ├── reports/            Phase 2–3: news email, portfolio note, monthly report
│   └── universe/           Phase 3: EM stock universe and screener
├── dashboard/              Phase 2: Google Apps Script dashboard (HTML)
├── prompts/                AI prompts used by the pipeline, versioned like code
├── tests/                  Tests for src/
└── docs/                   This file and other notes
```

## Who owns what

| Folder | Tasks | Language | Owner |
|---|---|---|---|
| `config/` | 0.1–0.2 | — | PT |
| `src/monitoring/` | 1.1, 1.2, 1.3 | Python | Open |
| `src/data/` | 2.2 | Python | Open |
| `src/reports/` | 2.1, 2.3, 3.1 | Python | Open |
| `src/universe/` | 3.2 | Python | Open |
| `dashboard/` | 2.4 | Apps Script, HTML | PT |
| `prompts/` | 2.3, 3.1 | Text | Open |

Task numbers match the task table on the Notion team hub.

## How data flows

```
Google Finance ──► src/data (scraper) ──► Google Sheet ──► dashboard/ (Apps Script web app)
News sources ────► src/monitoring ──────► src/reports ──► email / BSEMC channel
                                                  ▲
                                           prompts/ (AI drafts, human sign-off)
```

## Status

Placeholders only. Each folder has a README describing what goes in it. Code arrives through pull requests.
