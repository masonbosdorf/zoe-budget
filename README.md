# Zoe's Budget

A copy of [Regulars](https://github.com/masonbosdorf/regulars): a phone web app that tracks recurring
bills and tells you, from the balance in your bills account, whether the next week and the fortnight
after are covered. Single `index.html`, no backend, no accounts. Everything is saved on the phone.

**Use it:** open https://masonbosdorf.github.io/zoe-budget/ on the iPhone → Share → **Add to Home Screen**.

## Differences from Regulars

- **Starts empty.** No bills are preloaded. Tap **+** to add your own bills and amounts.
- **Logo presets:** 30 common bills as emoji tiles (rent, electricity, internet, phone, car rego,
  petrol, groceries, TV and more), plus the same brand logos Regulars uses. Tapping a preset fills
  in the name if you haven't typed one.
- **Any emoji:** the smiley tile opens a field. Tap it, switch to the iPhone emoji keyboard (🌐) and
  pick any emoji. It shows on a tile in the colour you choose.
- **Photo logo:** the camera tile opens the camera roll. The photo is cropped to a square and saved
  with the bill.
- **Entry code** on open. You'll be asked once whether you want to use **Face ID** instead (you can
  also change it in settings). The app locks again after more than a minute in the background.
- Storage keys start with `zb_`, so this app never mixes data with Regulars on the same phone.

## What it does (same as Regulars)

- **Arch gauge**: This Week (next 7 days) and Later (days 8–14). Your balance lights up the segments.
  Tap the coral number to edit it.
- **Tap a bill** when it's paid. **Done** moves it to its next due date, and Undo is in the toast.
  **Hold** a bill to edit or delete it.
- **History** (clock icon), **pull down to refresh**, **…** settings (window lengths, Done takes it
  off the balance, Face ID, Export/Import, Start again).

## Data

`localStorage` keys: `zb_bills`, `zb_paid`, `zb_history`, `zb_settings`, `zb_bal`. There is no cloud
copy, so export before changing phones. The entry code is a screen lock, not encryption.
