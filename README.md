# Regulars

A phone web app that tracks recurring bills and tells you, from the balance in your bills
account, whether the next week and the fortnight after are covered. Styled after Up Bank's
*Essentials* screen. Single `index.html`, no backend, no accounts — everything lives in the
phone's own storage.

**Use it:** open the Pages URL on the iPhone → Share → **Add to Home Screen**.

## What it does

- **Arch gauge** — This Week (next 7 days) and Later (the 14 days after) as fixed segments;
  your balance lights them up left to right. The coral number is the balance: tap to edit.
- **Coverage tiles** — Covered / $X short for each window, plus what's spare after.
- **Regulars** — three-wide cards sorted soonest first. Today's are outlined.
- **Tap a card** when it's paid → Done moves it to its next occurrence (weekly Monday → next
  Monday, monthly 10th → the 10th next month) and it re-sorts. Undo in the toast.
- **Hold a card** to edit or delete. **+** adds one: weekly, fortnightly, monthly, quarterly
  or yearly; pick a logo or a coloured initial.
- **…** settings: window lengths, "Done takes it off the balance", Export / Import (JSON via
  the share sheet), Reset to the seed list.

## Files

| File | Role |
|---|---|
| `index.html` | the whole app (logos embedded as WebP data URIs) |
| `logos/` | the 128px source tiles + `SOURCES.md` (where each official mark came from) |
| `icon-180.png` / `icon-512.png` | home-screen icon |

## Data

`localStorage` keys: `rg_bills` (the list), `rg_paid` (id → last paid date), `rg_settings`,
`rg_bal`. Due dates are computed from the rules each open, never stored. Export before
changing phones — there is no cloud copy by design.
