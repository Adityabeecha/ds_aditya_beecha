# Trader Performance vs Market Sentiment Analysis

## Overview
This project analyzes the relationship between market sentiment and trader performance using historical trade data merged with the Fear & Greed Index. The objective is to understand how different sentiment regimes influence profitability, risk, and trading behavior, and to identify patterns followed by consistently profitable traders (“Smart Money”).

The analysis progresses from market-level insights to account-level strategy profiling, enabling actionable conclusions rather than surface-level observations.

---

## Data Sources
The project uses two primary datasets:

- **Historical Trade Data**  
  Trade-level records including account ID, traded asset, execution price, trade size, direction, timestamps, fees, and realized PnL.

- **Fear & Greed Index**  
  Daily sentiment scores and qualitative classifications reflecting overall market psychology.

---

## Data Preparation
Several preprocessing steps were required to create an analysis-ready dataset:

- Parsed and standardized timestamps across datasets.
- Merged trades with the nearest available sentiment date using a ±2 day tolerance.
- Normalized categorical fields such as trade side, direction, and sentiment classification.
- Removed non-informative or redundant columns.
- Engineered additional features including:
  - Sentiment buckets
  - Sentiment lag (date difference)
  - Trade execution hour

The final merged dataset serves as the foundation for all analysis and visualizations.

---

## Exploratory Data Analysis
Key analytical areas include:

- Profitability across sentiment regimes (Extreme Fear → Extreme Greed)
- Risk and volatility assessment using PnL distributions
- Buy vs Sell performance under varying market sentiment
- Asset-level sentiment sensitivity focused on highly traded coins
- Time-of-day performance analysis
- Sentiment lag analysis to measure short-term impact
- Win-rate analysis across sentiment classifications

Results show that sentiment effects are non-linear and strongest during emotional extremes.

---

## Trader Profiling (Smart Money Analysis)
To isolate skill-driven behavior:

- Accounts were ranked by total realized Closed PnL.
- A small subset of top-performing accounts was identified as **Smart Money**.
- This cohort was analyzed separately to understand professional trading behavior.

This step demonstrates that profitability is highly concentrated and not uniformly distributed across traders.

---

## Strategy Insights
Analysis of the Smart Money cohort reveals consistent strategic patterns:

- Position sizing increases during conviction-driven sentiment phases.
- Contrarian strategies perform best during Extreme Fear.
- Momentum and profit-booking dominate during Extreme Greed.
- Exit timing contributes more to profitability than aggressive entry.
- Sentiment functions best as a contextual filter when combined with direction and asset selection.

---

## Key Takeaways
- Market sentiment significantly impacts trader performance during extreme regimes.
- Both contrarian and momentum strategies are effective depending on sentiment conditions.
- Consistent profitability arises from disciplined position management.
- Profiling profitable traders reveals actionable strategies hidden in aggregate data.

---

## How to Run
1. Load the historical trade dataset and Fear & Greed Index data.
2. Run preprocessing and nearest-date merge steps.
3. Execute exploratory analysis and visualizations.
4. Perform Smart Money filtering and strategy analysis.
5. Review final insights and conclusions.

---

## Conclusion
This project demonstrates that market sentiment alone is not a trading strategy but becomes powerful when combined with trader profiling, trade direction, timing, and asset selection. By isolating Smart Money behavior, the analysis moves from descriptive statistics to strategy-level understanding.

---

## License
This project is intended for educational and analytical purposes only.
