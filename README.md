# ML Cross-Sectional Alpha Research

A machine-learning research pipeline for predicting the cross-section of next-month US equity returns using price-, volatility-, liquidity-, and risk-based characteristics.

The purpose of this project is to practice the full quantitative research workflow:

raw market data → feature engineering → walk-forward prediction → cross-sectional portfolio construction → performance evaluation.

---

## 1. Research Question

Can observable equity characteristics produce stable out-of-sample cross-sectional return rankings?

I compare linear, tree-based, boosting, and neural-network models using the same leakage-safe walk-forward evaluation procedure.

---

## 2. Universe

- Asset class: US equities
- Approximate universe size: 200 liquid stocks
- Universe is frozen before model development.
- Stocks must have sufficient historical price and volume data to compute the required features.

For this project, the universe is a fixed set of liquid US stocks selected at the beginning of the experiment.

### Limitation

Because the universe is constructed using currently available securities, the historical backtest may contain survivorship bias.

This project is intended primarily as a research and skill-building exercise rather than an unbiased estimate of historical strategy performance.

---

## 3. Sample Period

Raw data:

- Start: 2010-01-01
- End: latest available date

Prediction frequency:

- Monthly

Portfolio rebalancing frequency:

- Monthly

Each observation in the final dataset represents one stock at one vgggmonth-end:

```text
(ticker, month)
```
