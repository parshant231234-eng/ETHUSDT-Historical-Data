# ETHUSDT 1-Minute Historical Kline Dataset

An institutional-grade, open-source archive of cleaned, standardized, and validated **1-minute intraday historical kline data** for **ETHUSDT** (Binance Spot).

---

## 📊 Dataset Specifications
- **Symbol:** `ETHUSDT`
- **Market:** Binance Spot
- **Timeframe:** 1 Minute (`1m`)
- **Total Archived Files:** `111` files
- **Total Candles:** `4,802,238` 1-minute candles
- **Last Updated:** `2026-10-10 17:06:17 UTC`
- **Schema:** `timestamp, datetime_utc, open, high, low, close, volume, quote_volume, trade_count, taker_buy_volume, taker_buy_quote_volume`

---

## 🏛️ Directory Hierarchy
```text
ETHUSDT-Historical-Data/
├── README.md
└── 1m/
    └── <YYYY>/
        └── <MM>/
            └── ETHUSDT_1m_<YYYY-MM>.csv
```

---

## ⚡ 1-Line Pandas Stream Loader
Load any month directly from GitHub's raw CDN without cloning the repository:

```python
import pandas as pd

url = "https://raw.githubusercontent.com/parshant231234-eng/ETHUSDT-Historical-Data/main/1m/2026/09/ETHUSDT_1m_2026-09.csv"
df = pd.read_csv(url)
print(df.head())
```

---

## 🔄 Automated Ingestion Pipeline
This repository automatically runs a weekly GitHub Actions workflow every Sunday midnight (UTC) to append newly closed daily candles and archive completed months.
