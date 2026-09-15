# Compound Wi-Fi Manager

A responsive, interactive Wi-Fi subscription pilot for a compound of 28 households, built for Nuru Amudi.

## Features

- Household registration, search, and subscription status filters
- Manual demo payment records with duplicate-reference rejection
- Package assignment and expiry extensions
- House-specific, single-use demo vouchers
- Operating cost records and income-minus-cost summaries
- Support requests and resolution tracking
- Resident preview with voucher redemption and expiry information

## Run locally

No packages or build step are required. With Python 3 installed, run from this repository:

```bash
python3 -m http.server 8000
```

Open http://localhost:8000 in a modern browser. Use localhost or HTTPS for voucher generation, which uses the browser's secure-context crypto API.

## Try the main flow

1. Register House 24 with a demo resident name.
2. Record a payment and select a package.
3. Open Resident preview and select House 24 to check its expiry.
4. Create a voucher assigned to House 24 and redeem it in that preview.

## Pilot limitations

All households, payment history, and package prices are examples. Changes exist only in page memory and reset on refresh. This is not a production billing or access-control system: there is no database, resident authentication, payment gateway, router integration, or live connectivity monitoring. The resident selector is a preview control, not an authorization boundary.

The repository is public. The separately hosted ChatGPT Sites demo remains owner-private; publishing this code does not change that website's access policy. GitHub edits are not automatically synchronized with that deployment.

## Files

- `index.html` — application shell and accessible forms
- `style.css` — responsive dashboard styling
- `app.js` — demo data, views, and subscription workflows

## Next development steps

Add durable storage and separate manager/resident authorization, then integrate verified payment callbacks and compatible network equipment. Confirm actual package prices and network capacity before operating a live service.
