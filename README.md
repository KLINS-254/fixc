# TEXAFIC — Website/PWA starter

Mobile-first blue-and-gold prototype. Includes Home, Tasks, Wallet, Profile, free local demo registration, a manual OTP entry screen, fixed-fee sample task cards, M-Pesa Till checkout form, activity list, and PWA install/offline shell.

## Publish with GitHub + Vercel
1. Extract this ZIP and upload its contents to a GitHub repository.
2. Import the repository into Vercel as a static site (no build command required).
3. Deploy. HTTPS is required for service-worker/PWA behavior.

## Required before real launch
This is a front-end demo, not a production payment/account system. Browser storage is not secure. Registration stores a demo password in local storage, and should never be used for real credentials. OTP submission deliberately does not mark accounts verified because no trusted server is connected. Payment requests are only saved locally and do not initiate or verify an M-Pesa transaction.

- Add a backend and database with access rules.
- Implement secure authentication and server-side OTP validation/expiry/rate limiting. In the requested manual flow, an operator can send the code, but the server must validate it.
- Integrate Safaricom Daraja or an approved Till confirmation flow on the server. Never expose consumer secrets/passkeys in frontend code; never trust a receipt code typed by the user as payment proof.
- Set the real Till number securely on the backend and verify transactions server-to-server before updating task status or balances.
- Clearly disclose all fees, deliverables, refund terms, and any rewards. Offer app testing and honest private feedback; do not pay for positive public reviews or fake ratings.
- Add privacy policy, terms, support, audit logs, fraud controls, and refunds.

Task prices (KES 100–195) are sample display values and should be confirmed before launch.
