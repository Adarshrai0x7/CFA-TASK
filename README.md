# 📈 Mean Reversion Strategy using Bollinger Bands & RSI (Jupyter Notebook)

This repository contains a **Jupyter Notebook** implementation of a **Mean Reversion Trading Strategy** that uses **Bollinger Bands**, **RSI (Relative Strength Index)**, and **SMA (Simple Moving Average)** for trend filtering. The strategy is backtested on historical Google (GOOG) stock price data using the `backtesting.py` library.

---

## 📒 Project Overview

Mean reversion strategies are based on the idea that prices tend to revert to their average over time. This strategy enhances the basic concept by combining:

- 📉 **Bollinger Bands** to identify overbought and oversold conditions,
- 💪 **RSI** to confirm momentum strength,
- 📈 **SMA** to filter trades based on the overall market trend.

---

## 🛠 Strategy Logic

### ✅ Entry Conditions

- **Buy Signal** (Long Entry):
  - Price is **below** the **lower Bollinger Band**
  - RSI is **below 30** (indicating oversold)
  - Price is **above the 50-period SMA** (indicating an uptrend)

- **Sell Signal** (Short Entry):
  - Price is **above** the **upper Bollinger Band**
  - RSI is **above 70** (indicating overbought)
  - Price is **below the 50-period SMA** (indicating a downtrend)

### ❌ Exit Conditions

- Exit long when price crosses **above** the Bollinger **middle band**
- Exit short when price crosses **below** the Bollinger **middle band**

---

## 📁 Repository Contents

| File | Description |
|------|-------------|
| `CFA.ipynb` | Main Jupyter Notebook with strategy code and analysis |
| `README.md` | Project documentation |
| `requirements.txt` | Required Python libraries |

---

## ▶️ How to Run

1. **Install dependencies:**

   You can install all required packages using pip:

   ```bash
   pip install -r requirements.txt

