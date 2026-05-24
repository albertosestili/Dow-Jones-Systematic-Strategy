# Systematic Intraday Trading Strategy — Dow Jones (US30)

**Fully mechanical, rule-based intraday system | 6 consecutive profitable years (2020–2025)**

---

## Overview

This project documents the independent development and validation of a fully systematic intraday trading strategy on the Dow Jones Industrial Average (US30), operating on a 5-minute timeframe.

The system is **100% rule-based**: every entry, exit, and filter is defined in advance. There is no discretionary component during execution, which eliminates human error and psychological bias — two of the most common sources of underperformance in active trading.

The strategy was developed and refined over 6 years of out-of-sample testing and live observation, covering multiple market regimes including the 2020 pandemic-driven volatility, the 2022 bear market, and the 2023–2025 recovery.

---

## Methodology

Each component of the system was designed and tested **in isolation** before being integrated into the final ruleset. A filter was retained only if it demonstrated a statistically positive contribution to overall performance.

**Core design principles:**
- Pattern-based entry logic rooted in recurring price-action structures
- Asymmetric risk/reward: **Long trades target 3.4R, Short trades target 2R**
- Operational filters applied to reduce noise and exposure to low-edge conditions

**Filters in use:**
- Exclusion of specific weekdays with no statistical edge
- Filtering of high-impact macroeconomic events
- Structural market-condition filters

**Validation approach:**
- Each filter backtested standalone
- Retained only if it produced a statistically meaningful improvement in expectancy or drawdown
- No curve-fitting: rules are simple, robust, and consistent across years

---

## Performance (2020–2025)

| Metric | Value |
|---|---|
| Annualized Sharpe Ratio | **1.97** |
| Calmar Ratio | **2.76** |
| Annualized Sortino Ratio | **4.35** |
| Total R Generated | **+225.2R** |
| Expectancy per Trade | **+0.323R** |
| Profit Factor | **1.5** |
| Win Rate | 36% |
| Total Trades | 768 |
| Max Drawdown | 13.6R |
| Max Losing Streak | 12 consecutive SL |
| Profitable Years | **6/6** |

### Equity Curve

![Equity Curve 2020–2025](equity_curve.png)

---

## Risk Management

Risk is managed through an **R-multiple framework**: each trade risks a fixed unit (1R) of account equity, defined before entry. This makes performance independent of capital size and allows clean comparison across timeframes and instruments.

Key risk principles:
- Fixed pre-defined risk per trade (1R)
- Asymmetric reward structure to maintain positive expectancy at 36% win rate
- Hard cap on consecutive losing streaks observed but not artificially limited (12 SL max in 6 years)
- Drawdown monitored as multiple of average R, not as % of equity

---

## Tools & Platforms

- **Backtesting & analysis:** TradingView, Excel
- **Forward testing & execution:** MetaTrader 5, cTrader
- **Data:** Historical intraday US30 data

---

## Honest Reflections & Limitations

A few points worth stating openly:

- **Win rate is intentionally low (36%).** The edge comes from R:R asymmetry, not from win frequency. This requires discipline through losing streaks — psychologically demanding even on a fully mechanical system.
- **Single-instrument focus.** The strategy is calibrated for US30 microstructure. Transferability to other indices (NDX, SPX, DAX) would require dedicated re-validation.
- **No regime-switching logic.** The system relies on robustness across regimes rather than active adaptation. This is intentional but caps the upside in trending environments.
- **Execution assumptions.** Backtest assumes realistic spreads and slippage, but live performance will always differ marginally from simulated results.

---

## Next Steps

- **Full automation:** Currently translating the system into an automated execution bot through AI-assisted development. Goal: end-to-end automation of signal generation, order management, and risk controls.
- **Multi-asset extension:** Exploring whether the core logic can be re-calibrated for additional equity indices.
- **Statistical refinement:** Ongoing research on alternative filters and exit logic to improve Sortino without compromising robustness.

---

## About

Developed independently by **Alberto Sestili**, MSc Finance student at LUISS Guido Carli, Rome.

📫 Contact: albertosestili02@gmail.com
🔗 LinkedIn: [Alberto Sestili](https://www.linkedin.com/in/alberto-sestili-63aa01182/)
