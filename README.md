# Stock-Market-Tracker-Google-Sheets-

Automated financial data dashboard for real-time equity monitoring and trend analysis.



## 📌 Table of Contents

1. [Project Overview](#project-overview)  
2. [Technical Stack](#technical-stack)  
3. [Core Functionality](#core-functionality)  
   - [Real-Time Market Data Integration](#real-time-market-data-integration)  
   - [Financial Reporting Formatting](#financial-reporting-formatting)  
   - [Trend Analysis & Visualization](#trend-analysis--visualization)
4. [Sample Output](#sample-output)  
5. [Analyst Relevance](#analyst-relevance)  
6. [Deliverables](#deliverables)



## Project Overview

This project simulates a live dashboard used by financial analysts to track real-time stock performance. Built entirely in Google Sheets, it retrieves live equity data, applies intuitive formatting, and visualizes trends for a selected watchlist of tech stocks. Designed for portfolio monitoring, investor reporting, and executive briefings.


## Technical Stack

- **Google Sheets**  
- `GOOGLEFINANCE()` for data extraction  
- `SPARKLINE()` for mini trend charts  
- Conditional formatting  
- Custom number and percentage formats


## Core Functionality

### Real-Time Market Data Integration

- Watchlist includes tickers like META, AAPL, AMZN, GOOG, etc.
- Pulled real-time data using:
  ```excel
  =GOOGLEFINANCE(A2, "price")
  =GOOGLEFINANCE(A2, "changepct")
  =GOOGLEFINANCE(A2, "volume")
  =GOOGLEFINANCE(A2, "name")

### Financial Reporting Formatting

- **Price**: USD with 2 decimal places  
- **Volume**: Shown in millions (e.g., `12.3M`)  
- **Conditional formatting** on `% Change`:
  - 🔴 **Red** for negative
  - 🟢 **Green** for positive (with reduced brightness)
  - ⚪️ **Neutral** for 0%

### Trend Analysis & Visualization

- **Fetched historical close data** (last 365 days):
  ```excel
  =GOOGLEFINANCE(A2, "close", TODAY()-365, TODAY())

- **Created in-cell sparklines for visual trend analysis**:
  ```excel
   =SPARKLINE(range, {"charttype", "column"; "color", "green"})


## Sample Output

<img width="640" alt="image" src="https://github.com/user-attachments/assets/f6dbf852-28ac-4214-a982-74d96a337df1" />

> *Note: Data changes dynamically with the market.*


## Analyst Relevance

This tool mirrors the practical work of financial analysts who monitor equities and report to executives or investors. It demonstrates:

- ✅ Real-time data automation  
- ✅ Visual analytics in spreadsheets  
- ✅ Reporting-ready formatting  
- ✅ Strong command of financial metrics


## Deliverables

- `Stock Market Tracker.xlsx`  
  A fully-automated, customizable dashboard for stock monitoring and trend visualization.

