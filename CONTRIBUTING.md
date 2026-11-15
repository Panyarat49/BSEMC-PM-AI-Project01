# Contributing

## Workflow

1. Create a branch for your task: `task/1.1-news-feed`.
2. Commit small, clear changes.
3. Open a pull request. Someone else reviews it before it merges.
4. Nobody pushes straight to `main`.

New to GitHub? Start with [Intro to GitHub](https://skills.github.com) or use [GitHub Desktop](https://desktop.github.com).

## AI rules

- **A human signs off** before anything is published under BSEMC's name.
- **Whoever merges code** must be able to explain what it does.
- **API keys and passwords never go in the repo.** Put them in `.env` (ignored by git); `.env.example` shows the names.

## Data

- The live ticker list (`config/tickers.csv`) is not committed while the repo is public. Use `config/tickers.example.csv` as the template.
- Don't commit portfolio positions, weights or FactSet exports.

## Where to ask

Comment on the Notion team hub or in the group chat.
