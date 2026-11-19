# Baifeng website build

This is a static, responsive storefront prototype for a factory-direct inquiry business. It borrows the reference site's editorial layout, product detail structure, and collection flow, while replacing checkout with an inquiry list. It does not take payment or place retail orders.

## Run

Serve this directory with any static HTTP server, for example `python3 -m http.server 8000` and open `http://localhost:8000`.

## Catalog

`catalog.json` contains 635 distinct public product-list entries captured from 32 pages of `hebeibaifeng.com` on 2026-11-18. Each entry retains its original URL. The 635 corresponding public listing images are stored as optimized WebP files in `assets/`. Category, compatible brand, and model are inferred from titles and should be reviewed before launch. No dimensions, inventory, price, or certification claims are invented. Golf cart, off-road, premium, and custom seating are presented as inquiry pathways based on the owner's brief; no unverified stock listings are fabricated for them.

For a larger catalog, replace `catalog.json` through a controlled import from the company's product system. Keep a stable product ID, family, compatibility brand, model, variant dimensions, media, and publication status. Do not create variant combinations until engineering confirms fit and availability.

## Inquiry flow

The inquiry list is stored in the visitor's browser. The form prepares an email to `alexia@sitongjx.cn` or a WhatsApp message to `+8615732671342`; the visitor must send it in their email or WhatsApp app. There is no server-side RFQ record, staff notification, CRM integration, or delivery confirmation yet. Add a backend/API and consent policy before production use if reliable submission and follow-up tracking are required.

The owner confirmed `alexia@sitongjx.cn` as the inquiry mailbox and selected English for the first release, with Chinese to follow. Confirm that the phone number is also the correct WhatsApp account before launch.

An Amazon link can be enabled later in `app.js` after the store's exact URL and retail policies are verified. The current site intentionally has no checkout.
