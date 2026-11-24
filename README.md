# ODDSENSE mobile web app (v0.2)

## Run locally
Open `index.html` in a browser to inspect the interface. Live API requests and installable PWA features require hosting over HTTPS; service workers do not work from a `file://` URL.

## Publish from an Android phone
One simple path is GitHub Pages:
1. Create/sign into GitHub.
2. Create a new public repository named `oddsense`.
3. Upload the contents of this folder (not the enclosing folder) using GitHub's web interface.
4. In repository Settings > Pages, choose Deploy from a branch, select `main` and `/ (root)`, then Save.
5. Wait for the Pages URL to appear. Open it in Chrome on Android.
6. In Chrome's menu, choose Install app or Add to Home screen.

## Live data
In ODDSENSE, tap the gear and paste your personal The Odds API key. The app calls the provider's v4 odds endpoint for 1X2 markets in the European region. Refreshes every five minutes while the page is visible.

## Critical limitations
- This is a client-side personal prototype. Your API key is stored in the browser's localStorage and sent to the provider from the browser. Do not share this hosted page with the key prefilled, and do not embed the key in source code.
- This prototype uses bookmaker prices to calculate market-implied probabilities. It is not an independent prediction model and cannot establish a reliable betting edge.
- The current integration only displays 1X2 odds. It does not yet analyze xG, injuries, suspensions, lineups, team form, weather, or other markets.
- Provider coverage, API quotas and browser/network policies can affect data availability.
- Never treat a risk label as a guarantee. The app does not place bets.

For a public multi-user product, move API calls to a secure backend so provider keys are not exposed to browsers.
