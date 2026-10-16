# WAJID BTC SIGNAL

Independent BTC/USDT signal dashboard for 15M, 30M and 45M. This project is separate from the XAU site and does not change its code.

## Current implementation
- Uses public Binance Spot BTCUSDT market endpoints; no exchange API key is required.
- 15M and 30M use native closed candles. 45M is aggregated from three closed 15M candles.
- Each timeframe has independent signal evaluation, entry, SL, TP1-TP4 and trade tracking.
- Signal rule is intentionally conservative: sweep/reclaim of a prior 20-candle extreme plus a directional structure close.
- TP1 moves SL to entry; TP4 closes the trade. The interim outcome rules are shown as R multiples in the dashboard.
- History is stored in the current browser's localStorage and can be exported to CSV. It does not sync across devices.
- This is a signal/monitoring dashboard only; it does not place orders.

## Publish with GitHub Pages (free)
1. Open repository Settings -> Pages.
2. Under Build and deployment, choose **GitHub Actions**.
3. The workflow in `.github/workflows/pages.yml` deploys the static site on each push to `main`.
4. Wait for the workflow to finish, then open the Pages URL shown in Settings -> Pages.

## Important limitations
- Binance public endpoints and browser access can be rate-limited or temporarily unavailable.
- A generated signal is a rule-based candidate, not a guarantee of profitability. Backtest and paper trade before risking money.
- Browser-local trade history may be lost when browser data is cleared.
