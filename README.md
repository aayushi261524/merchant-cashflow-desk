# Merchant Cashflow Desk

Public prototype: https://aayushi-merchant-cashflow.vercel.app/collections.html

## Provenance
Forked from [tuanpham-dev/react-invoice-generator](https://github.com/tuanpham-dev/react-invoice-generator), MIT licensed. The original invoice editor and PDF export are upstream features; LICENSE is retained.

## Added here
The browser-only collections ledger at public/collections.html adds invoice IDs, due dates, manually recorded full-payment status, outstanding/overdue/paid totals, filters, local saving, CSV export, fictional examples and single-change undo.

Amounts use integer paise and INR. Overdue means unpaid and due before the device’s local date. Paid totals are manual records, not bank-verified receipts. The invoice editor is separate: records do not transfer automatically, and its currency field must be set to match the ledger. No partial payments, bank integration, automated reconciliation or tax-compliance certification.

## Validation and deployment
Vercel production build passed. Live ledger and invoice editor load; sample totals and paid/undo behaviour were checked. The upstream editor generated a PDF download. Changes to master deploy automatically through Vercel’s GitHub app.

## Development
Use the scripts in package.json. Production: npm run build -- --base=/ (output dist). vercel.json selects the framework, build and collections landing route.

## Update
Edit public/collections.html for the ledger and src/ for the upstream editor. Preserve the original copyright and licence notices. Browser data is device-local; export backups before clearing browser storage.
