# King M1 Bet World — Play-Money Demo

This repository contains a mobile-friendly, offline-capable web demo and a Capacitor Android wrapper. It is a **virtual-coins-only prototype**, not a sportsbook or a real-money gambling product.

## Included

- Responsive sample sports fixtures and selectable demo odds
- Virtual coin balance and local demo bet history
- Explicit simulated settlement (random outcomes; not connected to real results)
- Age confirmation, clear demo disclosures, PWA manifest and offline service worker
- Capacitor configuration for generating an Android project

All app data is stored locally in the user's browser/app storage. There is no account service, server, live odds/results feed, payment, deposit, withdrawal, cash prize, or secure multi-user leaderboard. The sample players and fixtures are illustrative only.

## Run as a website / installable PWA

Serve the `www/` directory using a local or hosted HTTPS static server. Open the site in a supported browser and use its install/add-to-home-screen option. Service workers require HTTPS or localhost.

## Create and run the Android app

Requirements: Node.js/npm, Android Studio, Android SDK, and (for Play release) a configured Android signing key.

```bash
npm install
npx cap add android
npx cap sync android
npx cap open android
```

In Android Studio, run the app on a device/emulator for local testing. For a store package, configure the app's production package ID, version, icons, privacy details and signing, then use **Build > Generate Signed Bundle / APK** to create a signed Android App Bundle (AAB). Keep signing credentials private. This source repository does not include a built or signed APK/AAB; those must be generated and tested in your own Android build environment.

## Before any public release

This demo is deliberately limited to virtual coins and simulated outcomes. Do not add cash deposits, withdrawals, redeemable prizes, or real-money wagering by merely changing the UI. A real betting service needs a properly licensed and jurisdiction-compliant backend, verified odds/results, secure identity/age and location controls, payments and fraud controls, responsible-gambling safeguards, legal review, and approval under the app-store policies for each distribution market. A Play-money demo may also be subject to store review and must be accurately described; publishing is not guaranteed.

Do not put admin passwords, signing keys, payment secrets, or other credentials in client-side HTML/JavaScript. A local-only prototype cannot safely enforce admin privileges or secure transactions.
