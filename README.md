# 🧮 Portfolio Rebalancer

This Python script tracks your stock portfolio, checks for rebalancing needs based on the 5% threshold rule, and alerts you via email when action is required. It also logs performance over time in an Excel file with an automated chart.

## 🔧 Features

- Pulls real-time prices from Yahoo Finance
- Checks 5% threshold deviation from target allocations or average
- Exports Excel reports and charts
- Logs history and portfolio value snapshots
- Sends email notifications if rebalancing is needed

## 📁 Setup

### 1. Install Requirements
```bash
python -m venv venv
pip install -r requirements.txt
source venv/bin/activate
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

- `portfolio_output.xlsx`: your current portfolio + suggestions

---

PRs welcome.
