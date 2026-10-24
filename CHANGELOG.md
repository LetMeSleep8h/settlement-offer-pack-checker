# Changelog

## 1.0.0 - 2026-10-23

- Completeness gate per offer pack: creditor, enrolled balance, offer amount, expiry, payment schedule and client approval must all be present.
- Arithmetic validation: the payment schedule must sum to the offer amount, and the fee amount must match the fee percent of the enrolled balance.
- Expiry-risk check: projects the date the dedicated account can fund the offer from its current balance plus monthly drafts, and flags offers expiring before that date.
- Plain-language client summary for a selected pack (what you will pay, to whom, by when, what the fee is, total cost), downloadable as text, plus a downloadable audit CSV.
