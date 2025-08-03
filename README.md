# 📈 Personal Portfolio ETL Pipeline

This project automates the process of retrieving daily Zerodha (Kite API) portfolio holdings, saving them as structured CSV files in OneDrive, and refreshing a live Power BI dashboard using Power Automate. It’s designed to streamline investment monitoring without any manual effort.

---

## 🚀 Features

- 📊 **Daily Portfolio Tracking** from Zerodha
- 🧠 **Real-time Financial Insights** via Power BI
- 🔁 **End-to-End Automation** using Power Automate
- ☁️ **Cloud Integration** with OneDrive
- 📬 Optional Email Notifications for Daily Updates

---

## 🔧 Tech Stack

| Tool           | Purpose                                |
|----------------|----------------------------------------|
| **Python**     | Script to call Kite API & save CSV     |
| **Kite Connect API** | Access Zerodha holdings/orders        |
| **Power BI**   | Dashboard for portfolio visualization  |
| **Power Automate** | Flow to trigger dataset refresh         |
| **OneDrive**   | Cloud file storage & sync              |

---

## 📂 Folder Structure

```
Zerodha-Portfolio-Tracker/
├── scripts/
│   └── fetch_holdings.py
├── dashboards/
│   └── portfolio_dashboard.pbix
├── reports/
│   └── holdings_YYYY-MM-DD.csv  ← saved daily
├── power_automate/
│   └── refresh_flow_config.json
└── README.md
```

---

## ⚙️ Setup Instructions

### 1. 🧑‍💻 Clone & Configure the Python Script
- Install dependencies:
  ```bash
  pip install kiteconnect pandas
  ```
- Edit `fetch_holdings.py` with your:
  - `api_key` and `api_secret`
  - Set your OneDrive file path (e.g., `/Users/yourname/OneDrive/Portfolio/`)
- Run the script daily (manually or via Task Scheduler)

---

### 2. 🖼 Build Power BI Dashboard
- Load sample CSV into Power BI Desktop
- Create visuals:
  - Total Portfolio Value
  - Invested vs Market Value
  - Profit/Loss %, Day Change, etc.
- Publish to Power BI Service

---

### 3. 🔄 Create Power Automate Flow
- Trigger: `When a file is created (OneDrive)`
- Action: `Refresh a dataset (Power BI)`
- Optional: `Send an email notification`

---

## 📊 Example Visuals

- 💰 Total Value vs Invested
- 📈 Portfolio Growth Over Time
- 📌 Holdings by Symbol
- 🟥 Conditional Formatting for Losses

---

## 💡 Future Improvements

- Add order history & trade analytics
- Integrate email/SMS alerts for large changes
- Store historical data in a master file for time series

---

## 📌 Author

**Pranjal Jain**  
[LinkedIn](https://www.linkedin.com/) • [Email](mailto:pranjalpjain5@gmail.com)

---

## 📃 License

This project is for personal learning and educational demonstration purposes.
