# Wajid BTC Signal

Separate BTC/USDT signal dashboard.

- Binance public BTCUSDT 5-minute candles; no API key.
- Core flow: liquidity sweep → MSS/BOS → displacement → OB/FVG.
- BTC filters: volume and ATR/volatility guard.
- Entry, SL and TP1–TP4 at 1R–4R.
- $100 starting account model with $8 risk per trade.
- XAU-style trade management: TP1–TP3 are tracked, TP2 qualifies as WIN (+1R) while the trade stays open, TP4 closes at +4R, and SL before TP2 is -1R.
- First-pass diagnostic backtest on recent Binance 5M candles.

Testing is deliberately conservative and not a profitability claim. Before live use, the test engine should model partial TP rules, intrabar order, fees, slippage, longer history and walk-forward/out-of-sample periods.

The XAU repository is separate and is not modified by this project.