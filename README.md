# Moonwheel legal and support pages

Public-facing Privacy Policy, Terms of Use, and Support pages for Moonwheel.

## Public routes

- `/privacy.html`
- `/terms.html`
- `/support.html`

## App Store implementation notes

The content was reviewed on August 24, 2026 against these official Apple resources:

- [App Review Guidelines](https://developer.apple.com/app-store/review/guidelines/)
- [App privacy requirements](https://developer.apple.com/help/app-store-connect/manage-app-information/manage-app-privacy)
- [Auto-renewable subscriptions](https://developer.apple.com/app-store/subscriptions/)
- [Support URL requirements](https://developer.apple.com/help/app-store-connect/reference/app-information/platform-version-information/)
- [Apple Standard EULA](https://www.apple.com/legal/internet-services/itunes/dev/stdeula/)
- [EU Digital Services Act trader requirements](https://developer.apple.com/help/app-store-connect/manage-compliance-information/manage-european-union-digital-services-act-trader-requirements/)

Before release, the app operator must independently complete the DSA trader-status declaration in App Store Connect. If declaring as a trader, Apple requires verified contact details; these web pages do not replace that App Store Connect process.

The policy reflects the inspected Moonwheel code as of the review date: no Moonwheel account system, advertising SDK, analytics SDK, or live purchase SDK; preferences and downloads stored locally; downloadable media served from Supabase Storage; subscription code still a placeholder for a future Apple implementation. Re-review the policy and App Store privacy answers whenever the app adds or changes SDKs, accounts, analytics, advertising, purchases, support tooling, or server-side data collection.

## Hosting

Live at **https://moonwheel.app** (and www) as a Cloudflare Worker serving these files as static assets. Deploy with `npx wrangler deploy` from this folder; `.assetsignore` keeps README, config and git files off the site. `/` is the marketing home page (`index.html`, self-contained, art in `assets/`); the legal hub moved to `/legal`. Clean URLs (`/privacy`, `/terms`, `/support`); the old `.html` paths redirect. The GitHub Pages copy at adydxb.github.io/moonwheel-legal stays up for app builds that still link there.
