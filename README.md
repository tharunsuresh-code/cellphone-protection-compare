# Credit Card Cell Phone Protection Comparison

> Every US credit card with cell phone protection, side by side. Filters, pros & cons, and which premium cards leave you unprotected.

## What This Is

A single-page, dependency-free comparison tool for cell phone protection benefits across all major US credit cards. No frameworks, no build step, no tracking — just one HTML file.

## Live Site

https://tharunsuresh-code.github.io/cellphone-protection-compare/

## Features

- **30+ cards** from 7 issuers (Amex, Chase, Wells Fargo, Capital One, US Bank, Barclays, Citi)
- **Filters**: issuer, annual fee, prepaid coverage, per-claim amount, deductible, card type
- **Sortable table** by any column
- **Light/dark mode** with system default (light) and localStorage persistence
- **Prepaid coverage accuracy**: Wells Fargo cards are the only ones that cover prepaid/MVNO plans — all others require a "monthly cellular service bill" and deny prepaid claims
- **Premium cards without protection** section — highlights expensive cards that leave you unprotected
- Fully responsive, no external dependencies, works offline

## Data Accuracy

All data is compiled from official benefit guides and issuer websites. Benefits change frequently.

**If you find an inaccuracy, please open an issue or PR.** See `AGENTS.md` for contribution guidelines.

## Tech

- Single `index.html` file (~30KB)
- Vanilla HTML/CSS/JS — no build step, no dependencies
- GitHub Pages static hosting

## License

MIT
