# Taught to Trade: open-source Pine Script indicators

Pine Script v6 source for every indicator Taught to Trade has published on TradingView. All of them are already open source there. This repo keeps the code in one place you can read, diff and fork.

What they have in common:

- **No buy or sell signals.** Markers are neutral. Alerts use `alertcondition()`, so you decide whether to create one and what it means.
- **They count instead of asserting.** Where a popular indicator says "trust this", these show how often it held on your own chart: flips that were undone, levels price came back to, how many trades a result rests on.
- **Each one says where it fails.** The same section is in every TradingView description.

## The scripts

| Script | What it shows | TradingView | Explained |
|---|---|---|---|
| Range Filter Audit | The Range Filter rebuilt from scratch: the price that would turn the filter drawn on the chart, closed-bar vs open-bar turns, a Twin Range Filter preset, and a count of turns reversed within a few bars. | [script](https://www.tradingview.com/script/qGydpugy-Taught-to-Trade-Range-Filter-Audit/) | [Range Filter, from its source](https://taughttotrade.com/range-filter) |
| ATR Trailing Stop with Flip Audit | An ATR trailing stop with its stop line drawn, flips confirmed only at the bar close, and a count of flips undone within a few bars. Rebuilds the stop rule behind UT Bot Alerts from scratch. | [script](https://www.tradingview.com/script/9U7ccJIN-Taught-to-Trade-ATR-Trailing-Stop-with-Flip-Audit/) | [UT Bot Alerts, from its source](https://taughttotrade.com/ut-bot-alerts) |
| WaveTrend Audit | LazyBear's WaveTrend oscillator rewritten from scratch. Crosses marked on closed bars only, plus a panel counting how often the line sits beyond each level and how often the lines cross. | [script](https://www.tradingview.com/script/phF1Cmji-Taught-to-Trade-WaveTrend-Audit/) | [WaveTrend, from its source](https://taughttotrade.com/wavetrend) |
| Sample Size Panel | Enter a trade count and the rate that worked; it shows the range the true rate plausibly sits in (Wilson interval) and whether that range can be told apart from 50 percent. | [script](https://www.tradingview.com/script/qZkLfGBu-Taught-to-Trade-Sample-Size-Panel/) | |
| Support & Resistance Touch Count | Zones from swing pivots, how often price returns to them, and the same count for plain round-number levels as a control. | [script](https://www.tradingview.com/script/efF8TXKb-Taught-to-Trade-Support-Resistance-Touch-Count/) | |
| Swing Ratio Grid | A retracement grid that names the swing it measured and the ratio set it used, with an arbitrary 0.4 / 0.5 / 0.6 control grid beside it. | [script](https://www.tradingview.com/script/hqiGJ2ZQ-Taught-to-Trade-Swing-Ratio-Grid/) | |
| Session Range & Value Area Map | The previous session's value area and point of control, and the current session's opening range. | [script](https://www.tradingview.com/script/10y0liJB-Taught-to-Trade-Session-Range-Value-Area-Map/) | |
| Cost Hurdle | How much a strategy must earn per trade before fees and slippage are covered. | [script](https://www.tradingview.com/script/yfw8wzma-Taught-to-Trade-Cost-Hurdle/) | |
| Regime Tercile Dashboard | Splits history into three volatility regimes so you can see which one a result came from. | [script](https://www.tradingview.com/script/dsPXgFSZ-Taught-to-Trade-Regime-Tercile-Dashboard/) | |
| Backtest Integrity Scanner | Flags the structural problems that make a backtest read better than it should. | [script](https://www.tradingview.com/script/8ffRco5z-Taught-to-Trade-Backtest-Integrity-Scanner/) | [Is TradingView backtesting accurate?](https://taughttotrade.com/tradingview-backtest-accuracy) |
| Volatility Scanner (ATR%) | Ranks a watchlist by daily range as a percent of price. | [script](https://www.tradingview.com/script/oSkPJDdQ-Taught-to-Trade-Volatility-Scanner-ATR/) | |
| Configurable Stochastics | A stochastic with selectable SMA, EMA, WMA or HMA smoothing. | [script](https://www.tradingview.com/script/EikJr97k-Taught-to-Trade-Configurable-Stochastics/) | |

## Using one

Either open the TradingView link and add it to your chart, or paste the `.pine` file into the Pine Editor, save it, and press "Add to chart". Each file here is the source of the live TradingView publication.

## Credit for the rebuilds

Three scripts rebuild popular community indicators. No code was copied from any of them: the method was reimplemented from its published maths, and the script header and TradingView description credit the original authors.

- **ATR Trailing Stop with Flip Audit:** the stop rule popularised by *UT Bot Alerts* by QuantNomad, built on *UT Bot* by Yo_adriiiiaan, who credits HPotter.
- **WaveTrend Audit:** the *WaveTrend Oscillator* by LazyBear (2014).
- **Range Filter Audit:** the *Range Filter* method by DonovanWall, as used in guikroth's 5min variant, VuManChu Swing Free (Jazal) and colinmck's Twin Range Filter.

## Where this fails

These are measuring tools. A count on one chart is one sample, and history loaded on a different symbol, timeframe or date range gives different numbers. Nothing here tests whether a trade works, and a past frequency says nothing certain about the next bar.

## More

Plain-language teardowns of popular TradingView indicators, read from their source code, plus a free repaint checker: [taughttotrade.com](https://taughttotrade.com)

## Licence

[Mozilla Public License 2.0](LICENSE).

Educational tools only. Not investment advice. Trading involves substantial risk of loss.
