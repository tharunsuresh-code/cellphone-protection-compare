# Contributing & Agent Guidelines

## Welcome

All contributions welcome — whether you're a human or an LLM. If you spot an inaccuracy in the data, a bug in the UI, or a missing card, please open an issue or submit a PR.

## Project Structure

```
index.html    — the entire app (HTML + CSS + JS in one file)
README.md     — project overview
llm.txt       — machine-readable summary for AI crawlers/agents
AGENTS.md     — this file
```

## Data Accuracy Is The Priority

Credit card benefits change frequently. The most common issues:

- **Coverage terms change** — issuers update benefit guides without notice
- **New cards launch** — add them to the `cards` array in `index.html`
- **Prepaid coverage** — this is the most error-prone field. Currently:
  - **Wells Fargo** cards cover prepaid (no exclusion clause in their benefit guide)
  - **All other issuers** require a "monthly cellular service bill" and deny prepaid claims
  - If you have firsthand experience contradicting this, **please report it**
- **Discontinued cards** — keep them in the table but mark them clearly in the name (e.g., "Citi Prestige (discontinued)")

## How To Contribute

### Adding/Updating a Card

Edit the `cards` array in `index.html`. Each card object:

```javascript
{ name:"Card Name", issuer:"Issuer", fee:0, claim:800, deductible:50,
  claimsPerYear:2, annualMax:1600, prepaid:"no", type:"personal", tier:"mid",
  highlights:["Pro 1","Pro 2"], cons:["Con 1","Con 2"] }
```

Fields:
- `prepaid`: `"yes"` only if the benefit guide does NOT exclude prepaid/MVNO plans. Default `"no"`.
- `type`: `"personal"` or `"business"`
- `tier`: `"no-fee"`, `"mid"`, or `"premium"`

### UI/Feature Changes

The entire app is one HTML file. Keep it that way — no build steps, no npm dependencies. Vanilla JS only.

### Commit Messages

Clear, descriptive. Prefix with the type:
- `Fix:` for bug fixes
- `Add:` for new cards or features
- `Update:` for data corrections
- `UI:` for visual changes

## Verification Checklist

Before submitting a PR:
- [ ] Data verified against official benefit guide or issuer website
- [ ] No JavaScript errors in console
- [ ] Page works in both light and dark mode
- [ ] Filters and sorting still work after changes
- [ ] Mobile responsive layout intact

## License

MIT — contributions accepted under the same license.
