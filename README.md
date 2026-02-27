# -trader-behavior-and-performance
market sentiment (Fear/Greed)


# Trader Performance vs Market Sentiment  
**Primetrade.ai – Data Science Intern Assignment (Round-0)**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat&logo=powerbi&logoColor=black)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat&logo=sqlite&logoColor=white)

## 📌 Project Overview
Analyzed how **Bitcoin Fear & Greed Index** impacts trader behavior and performance on **Hyperliquid** (perpetual futures exchange).

**Goal**: Uncover actionable patterns in trader PnL, win rate, trade frequency, position sizing, and long/short bias across **Fear** vs **Greed** days to inform smarter trading strategies.

**Expected Effort**: Completed in ~3 hours (clean, reproducible, production-ready).

---

## 🎯 Objective (from Assignment)
- Part A: Data cleaning, timestamp alignment & metric creation  
- Part B: Statistical analysis + segmentation + visualizations  
- Part C: 2+ actionable strategy rules  
- Bonus-ready: SQL views + Power BI dashboard

---

## 📊 Datasets
1. **`fear_greed_index.csv`**  
   - 2,500+ daily records (2018–2025)  
   - Columns: `date`, `value`, `classification` (Fear / Extreme Fear / Neutral / Greed / Extreme Greed)

2. **`historical_data.csv`**  
   - 1.2M+ Hyperliquid trades  
   - Columns: `Account`, `Coin`, `Execution Price`, `Size USD`, `Side`, `Closed PnL`, `Timestamp IST`, `Direction`, etc.

---

## 🛠️ Tech Stack
- **Python 3.10+** → Pandas, NumPy, Plotly, Seaborn, Matplotlib
- **SQL** → SQLite3 (daily_metrics view)
- **Power BI Desktop** → Interactive dashboard (`.pbix` included in repo)
- **Jupyter Notebook** → Full reproducible analysis

---

## 🔑 Key Insights (Backed by Data & Charts)

1. **Frequent traders earn 2.3× more PnL on Greed days**  
   - Average daily PnL: **+$1,247** (Greed) vs **+$542** (Fear)

2. **Long bias jumps dramatically**  
   - Fear days → 48% long  
   - Greed days → **67% long** (clear sentiment-driven bias)

3. **Risk explodes on Fear days**  
   - Worst daily drawdown is **41% higher** on Fear days  
   - Win rate drops from 54% (Greed) → 47% (Fear)

4. **Consistent winners (win-rate > 55%)** behave differently  
   - They reduce size on Fear days and flip to short bias faster.

*(All charts exported in `/charts/` folder + embedded in notebook)*

---

## 🚀 Actionable Strategies (Part C)

**Strategy 1 – Frequent Traders Rule**  
> On **Greed** days → Increase position size by **1.5×**  
> On **Fear** days → Reduce size by **40%** and limit trade frequency  

**Strategy 2 – Consistent Winners Rule**  
> When sentiment turns **Fear** → Immediately switch to **short bias** (long_ratio drops to ~0.38)  
> Rule of thumb: “Fear = Short with winners | Greed = Long with size”

**Strategy 3 – Real-time Monitoring**  
Use the included `daily_metrics.csv` + Power BI dashboard to get daily sentiment-based alerts.

---

## 📁 Repository Structure

primetrade-sentiment-analysis/
├── primetrade_fear_greed_analysis.ipynb     # Full Jupyter Notebook (recommended)
├── daily_metrics.csv                        # Ready for Power BI / ML
├── fear_greed_index.csv                     # Original dataset
├── historical_data.csv                      # Original dataset (sample for GitHub)   <- this data i am not able to put in github beacause it's more than 25 mb
├── charts/                                  # Exported Plotly & Seaborn visuals
├── README.md
├── requirements.txt





