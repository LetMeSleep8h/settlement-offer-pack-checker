# Settlement Offer Pack Checker
Live page: https://aamirtechs.github.io/settlement-offer-pack-checker/

A completeness gate for settlement offers. No offer should reach a client until the creditor, terms, expiry, client approval and fee maths are all present and consistent, so settlement teams can stop rework, expired offers and avoidable complaints before they happen.

## Features
- Completeness gate per offer pack: creditor, enrolled balance, offer amount, expiry, payment schedule and client approval must all be present.
- Arithmetic validation: the payment schedule must sum to the offer amount, and the fee amount must match the fee percent of the enrolled balance.
- Expiry-risk check: projects the date the dedicated account can fund the offer from its current balance plus monthly drafts, and flags offers expiring before that date.
- Plain-language client summary for a selected pack (what you will pay, to whom, by when, what the fee is, total cost), downloadable as text, plus a downloadable audit CSV.

## How it works
Upload or paste one CSV row per offer pack, set the expected fee percent and the funding projection (current dedicated-account balance plus monthly draft), and run the check. Each pack gets a pass or fail with the exact failed checks, and you can download the audit CSV or a plain-language summary for one pack. Disclaimer: this is an operations checklist tool, not legal or financial advice. It runs entirely in the browser.

## Privacy
Runs 100% in your browser. Your files never leave this device, nothing is uploaded,
and there is no tracking.

## Development
Core logic lives in `src/logic.js` and is shared by the page and the tests.
Run the tests with `npm test`.

## License
MIT, Copyright 2026 Amir Hussain.
