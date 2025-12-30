# 📊 Trader Performance vs Market Sentiment Analysis

## 🧭 Project Overview
This project explores the relationship between **trader performance** and **Bitcoin market sentiment** using two datasets — one capturing the **Fear & Greed Index** and another detailing **historical trades from Hyperliquid**.  
The goal is to identify behavioral and performance patterns that emerge under different market moods (Fear vs Greed) and to derive actionable insights for smarter trading strategies.

---

## 🧩 Datasets

### 1️⃣ Bitcoin Market Sentiment Dataset  
**Columns:**  
- `timestamp` — Unix timestamp of the record  
- `value` — Numeric sentiment value  
- `classification` — Categorical sentiment label (`Fear`, `Greed`, etc.)  
- `date` — Human-readable date  

### 2️⃣ Historical Trader Data from Hyperliquid  
**Columns:**  
- `Account`, `Coin`, `Execution Price`, `Size Tokens`, `Size USD`, `Side`, `Timestamp IST`,  
  `Start Position`, `Direction`, `Closed PnL`, `Transaction Hash`, `Order ID`,  
  `Crossed`, `Fee`, `Trade ID`, `Timestamp`

---

## 🎯 Objective
Analyze how **trader behavior** (profitability, risk, volume, direction) aligns or diverges from **overall market sentiment** (Fear vs Greed).  
The project aims to:
- Detect behavioral trends under varying sentiment conditions  
- Identify correlations between sentiment and profitability  
- Uncover signals that can drive smarter trading or investment strategies  

---

## 🧪 Analysis Workflow

1. **Data Preprocessing**
   - Loaded and cleaned both datasets  
   - Converted timestamps to datetime format  
   - Merged trader data with sentiment data on matching date fields  

2. **Exploratory Data Analysis (EDA)**
   - Summary statistics and distribution analysis  
   - Correlation heatmaps between numeric variables  
   - Trend and sentiment frequency visualization  

3. **Visual Analysis**
   - `avg_pnl_vs_sentiment.png`  
   - `correlation_matrix.png`  
   - `direction_vs_sentiment.png`  
   - `pnl_distribution_by_sentiment.png`  
   - `top_profitable_days.png`  
   - `trader_winrate_comparison.png`  
   - `volume_vs_sentiment.png`

4. **Insight Extraction**
   - Comparison of average PnL across sentiment phases  
   - Directional (Buy/Sell) bias under Fear vs Greed  
   - Trader win-rate and volume dynamics  
   - Identification of most profitable trading days  

---

## 📈 Key Insights and Explanations

- **Profitability:** Traders achieved higher average PnL during **Greed** phases compared to Fear, showing sentiment-driven performance.  
- **Volume Behavior:** Trading volume peaked during **Extreme Greed**, suggesting increased participation and risk appetite.  
- **Directional Trends:** Buy trades dominated in Greed phases, while sell/hedging was common during Fear.  
- **Correlation:** Sentiment value showed a mild positive correlation with PnL and trade size.  
- **Win Rate:** Top traders maintained stronger win rates in Greed and Neutral markets than during Fear.  
- **Profitable Days:** Highest profits aligned with strong bullish sentiment days.  

📊 **Conclusion:**  
Market sentiment significantly influences trader behavior. Optimistic markets drive higher volumes, profitability, and buy-side dominance, while fear induces cautious, low-volume trading. Incorporating sentiment analysis can enhance trading strategy timing and risk management.

---

## 🚀 Future Enhancements

1. **Real-Time Sentiment Integration** — Incorporate live Fear & Greed Index and social sentiment data.  
2. **Predictive Modeling** — Use ML models (Random Forest, LSTM) to forecast profitability and sentiment shifts.  
3. **Leverage & Risk Analysis** — Add leverage metrics to study risk exposure under different sentiments.  
4. **Algorithmic Strategy Backtesting** — Simulate trading rules driven by sentiment signals.  
5. **Multi-Asset Extension** — Expand analysis to other cryptocurrencies.  
6. **Causal & Time-Series Analysis** — Apply Granger causality and cointegration to test temporal relationships.  
7. **Interactive Dashboard** — Deploy results in a Streamlit dashboard for real-time data exploration.  
8. **On-Chain Data Integration** — Combine with blockchain transaction data for deeper behavioral analysis.  

## 📁 Repository Structure
ds_trade_sentimet


├── notebook_1.ipynb  

├── csv_files/ # Raw and processed CSVs

│ ├── historical_data.csv

│ ├── sentiment_data.csv

│ └── merged_trader_sentiment.csv

├── outputs/ # Visualization outputs

│ ├── avg_pnl_vs_sentiment.png

│ ├── correlation_matrix.png

│ ├── trader_winrate_comparison.png

│ └── ...

├── ds_report.pdf # Final project report

└── README.md # Project documentation


##  How to Run
1.	Open the Google Colab notebook:
Link is given below
https://colab.research.google.com/drive/1KLm8meUVVwbgZK6rE3yIzbrntI0rBxe0?usp=sharing
2.  Run all cells in order to generate processed CSVs and visualization outputs.
