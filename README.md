# a-share-factor-research

> Cross-sectional return prediction on China A-shares: price-volume and fundamental factors,
> industry and size neutralisation, factor combination, and out-of-sample evaluation net of
> trading costs.

**Status: work in progress.** No results yet — numbers will be added only once they come out of
a genuine out-of-sample period.

## Planned pipeline

1. **Data** — daily bars, adjustment factors, fundamentals, industry classification, trading
   status (suspensions, limit-up/limit-down, ST), built as a point-in-time panel
2. **Factors** — price-volume and fundamental factors, winsorised and standardised
   cross-sectionally
3. **Neutralisation** — regress out industry and size exposure
4. **Evaluation** — RankIC / ICIR, quantile backtests, long-short returns, drawdown, turnover
5. **Combination** — linear and gradient-boosted factor combination
6. **Costs** — transaction costs and turnover constraints applied before any number is reported

## Layout

```
src/ashare_factor/
  data/        loading, cleaning, point-in-time alignment
  factors/     factor definitions
  backtest/    IC analysis, quantile and long-short backtests
notebooks/     exploration
tests/
data/          local cache (git-ignored)
```

## Open decisions

- Data source (Tushare / AkShare / other)
- Universe (all A-shares / CSI 300 / CSI 500 / CSI 1000) and sample period
- In-sample / out-of-sample split
