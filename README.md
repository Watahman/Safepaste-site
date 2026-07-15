# SafePaste

SafePaste is a local Chrome extension that warns you when you paste sensitive text, submit a form, or manually scan selected text. Scanned content never leaves your browser.

## Getting started

1. Run `npm.cmd run build`.
2. Open `chrome://extensions`, enable Developer mode, and choose **Load unpacked**.
3. Select the `dist` folder.

## Checks

Run `npm.cmd test`, `npm.cmd run lint`, `npm.cmd run build`, and `npm.cmd run package` to run the tests, privacy lint, build, and release ZIP creation.

## Plans and payments

- **Free:** local warnings and anonymization for personal use.
- **Pro:** €3.99 per user/month.
- **Team (future admin panel):** €2.50 per user/month, billed monthly, with a five-user minimum (€12.50/month).

Replace only the public `extensionPayId` in `src/payment-config.ts` before publishing. The extension contains no secret key. See [docs/PAYMENT_SETUP.md](docs/PAYMENT_SETUP.md).

## Team policies

Administrators can enforce API-key, token, secret, private-key, card, and IBAN blocking through Chrome managed storage. The `managed-schema.json` file documents the accepted policy values; [docs/TEAM_WINDOWS_GUIDE.md](docs/TEAM_WINDOWS_GUIDE.md) contains the Windows test and deployment procedure. Managed rules override personal settings and are processed locally in the browser.

## Known limitation

Form warnings can allow a submission or copy anonymized combined field text; they do not automatically rewrite individual form fields. Detection is heuristic, especially for addresses and general secrets.
