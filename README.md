# 🧮 Portfolio Rebalancer

This Python script tracks your stock portfolio, checks for rebalancing needs based on the 5% threshold rule, and alerts you via email when action is required. It also logs performance over time in an Excel file with an automated chart.

## 🔧 Features

- Pulls real-time prices from Yahoo Finance
- Checks 5% threshold deviation from target allocations
- Exports Excel reports and charts
- Logs history and portfolio value snapshots
- Sends email notifications if rebalancing is needed

## 📁 Setup

### 1. Install Requirements
```bash
pip install pandas requests beautifulsoup4 openpyxl
```

### 2. Create `portfolio.csv`
```csv
ticker,shares,target_pct
VTI,100,0.25
VOO,50,0.25
VXUS,80,0.15
BND,120,0.20
VNQ,40,0.15
```

### 3. Create `config.json`
```json
{
  "email_enabled": true,
  "sender_email": "your_email@gmail.com",
  "recipient_email": "your_email@example.com",
  "smtp_server": "smtp.gmail.com",
  "smtp_port": 587,
  "email_password": "your_app_password"
}
```

### 4. Run the Script
```bash
python portfolio_manager.py
```

## 📈 Output

- `rebalance_report.xlsx`: your current portfolio + suggestions
- `portfolio_history.xlsx`: ongoing tracking with chart

---

PRs welcome. Built with 💼📊 and ☕️
