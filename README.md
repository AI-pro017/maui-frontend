# Maui Frontend

The web app for Maui, a savings and borrowing app built on Terra that was meant to feel like a normal banking app instead of a DeFi dashboard.

Users sign up with an email or Google, fund their account with crypto or a card, and earn yield on their UST through Anchor. The app also has screens for borrowing against your savings, browsing tokenized stocks and ordering a Maui card.

## Screens

- Login with email and password or with Google.
- A dashboard with your UST balance and an overview of your account.
- Deposits, either by connecting a Terra wallet and sending crypto or by buying with a card or bank transfer through Transak.
- An Earn page to deposit or withdraw UST from Anchor, with a chart of your balance over time.
- A Borrow page for borrowing up to 50% of your collateral, with the loan paid back by the collateral's yield.
- A Stocks page for browsing tokenized stocks.
- A Cards page showing the Maui debit card designs.
- Account settings.

Some of these screens were still prototypes. The stocks list uses mock data and the borrow sliders use fixed example values.

## Tech stack

- React 16 with Create React App, based on the Flatlogic React Material Admin template
- Material UI, ApexCharts and Recharts
- Redux with redux-saga
- terra.js and the Terra wallet provider
- Transak SDK for card and bank purchases
- Firebase Hosting

## Running it locally

```bash
git clone https://github.com/AI-pro017/maui-frontend.git
cd maui-frontend
npm install
npm start
```

The app expects the Maui backend at the `apiUrl` in `src/config/apiConfig.js`, and reads balances from the Terra Bombay testnet in `src/wallet.js`. Bombay and the `terra.dev` endpoints have since been shut down, so both need updating before the app can load real data.

## Deploying

```bash
npm run build
firebase deploy
```

`firebase.json` serves the `build` folder as a single page app.

## License

MIT. The original admin template is by Flatlogic, see [LICENSE.txt](LICENSE.txt).
