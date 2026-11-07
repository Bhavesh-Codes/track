# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

A single person — the owner — tracking their own day. KARM is used alone, in a desktop browser, logging hours as the day passes and reviewing the record afterward. There is no second audience: no accounts, no sharing, and no multi-user concerns.

## Product Purpose

KARM is an hour-by-hour ledger of how a day was actually spent. It exists to make wasted time visible and reduce it: every hour is labelled, scored, and compared over time so the owner can see where time leaked and correct it. Success is fewer wasted and unproductive hours, made visible in the daily score, the mini-calendar heat map, and the 30-day trend.

## Positioning

KARM is a manual, category-based day ledger, not an automatic tracker. Nothing is inferred or measured in the background: the owner explicitly labels each hour with what it was — including the uncomfortable categories, "Unproductive" and "Wasted" — and the score is derived only from those labels. It is local-only and zero-setup, so an honest record costs nothing but the discipline of logging.

## Operating Context

- Used in the owner's own browser during the day; the product is built around logging at the end of each hour.
- The focus timer and optional audio alarm exist to prompt that hourly log; "Log Previous Hour" is the one-click catch-up.
- The day is reviewed through the 24-hour grid, the mini-calendar heat map, and the bottom analytics panel (30-day trend, weekly/daily breakdown).
- Recurring rituals: copy the previous day's schedule and mass-log sleep from the header, and log any hour by clicking its tile; the timer can prompt the hourly log.
- Data lives in browser localStorage under `karm_data`, `karm_goals`, `karm_timer`, and `karm_sound`; clearing site data erases the history.
- The current layout is desktop-first: fixed sidebar plus a 24-hour grid.

## Capabilities and Constraints

- Confirmed functionality: 24-hour grid; eight activity categories (Productive, Semi-Productive, Neutral, Gym, Errands, Unproductive, Wasted, Sleep) plus Unlogged; free-text note per hour; automatic productivity score; daily productive-hours and sleep goals; focus timer with optional Web Audio alarm; 30-day trend chart; weekly and daily donut breakdown; all-time best score; vs-last-week comparison; streak; mini calendar; header actions; dark and light themes.
- Scoring semantics are product truth: Productive and Gym count fully; Semi-Productive and Neutral count half; Errands, Unproductive, and Wasted count zero. Sleep is excluded from the denominator.
- Technical constraint: one self-contained `index.html`; React 18, Tailwind, Chart.js, and Babel load from CDNs, so the first load needs a network connection. All logic is client-side; there is no backend, account, sync, or export.
- Single-device by design: data does not move between browsers or machines.
- Automatic time capture, integrations, and device signals are out of scope.

## Brand Commitments

- The name is KARM.
- The voice is blunt and non-judgmental: "Wasted" and "Unproductive" are named plainly, without euphemism, and the tone stays matter-of-fact rather than scolding.
- The category names are established user-facing terminology and should not be renamed casually.

## Evidence on Hand

- Working implementation: `index.html` (all features above).
- `README.md` documents features, storage keys, and the no-build setup.
- No real user history, testimonials, benchmarks, screenshots, or press are committed. Future work must not fabricate usage data, scores, or social proof.

## Product Principles

1. **Honesty over flattery.** The ledger is only useful if it records the bad hours too; never soften or hide what the owner logged.
2. **Logging must cost seconds.** Every recurring action — log an hour, copy yesterday, log sleep — stays one click away.
3. **The score is diagnostic, not a reward.** It exists to expose where time went, not to gamify productivity.
4. **The whole day counts.** Sleep, gym, and errands are part of the picture; this is not a work-output meter.
5. **Zero setup, zero surveillance.** No account, no backend, no background tracking; the browser is the whole product.
