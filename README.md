# txn-banking-analytics
**Synthetic Transaction Data for Banking Operations and Analytics**

## 📄 Dataset Overview
This dataset contains **10,000 synthetic banking transactions** for the year **2024**.  
The transactions include **Transfers**, **Withdrawals**, and **Deposits** and are distributed across the **50 largest US cities**, proportionally weighted by population.  

Special attention was given to **US federal holidays**, particularly **Thanksgiving**, **Black Friday**, and **Christmas**, to simulate realistic **spikes in transaction activity**.

Each record is enriched with:
- Realistic **geolocation data**
- Device connectivity types and corresponding latency ranges
- Simulated anomalies such as fraud attempts, extreme transaction amounts, and unusual account behavior  

The dataset is designed for:
- **Financial data analysis**
- **Fraud detection**
- **Geospatial analytics**
- **Network performance evaluation**
- **Machine learning modeling** related to transaction analysis and anomaly detection

---

## 🔑 Key Features

| Field | Description |
|-------|-------------|
| **Transaction ID** | Unique identifier for each transaction |
| **Sender Account ID** | The account number of the transaction sender |
| **Receiver Account ID** | The account number of the transaction receiver |
| **Transaction Amount** | Monetary value with injected anomalies (extreme and zero values) |
| **Transaction Type** | Transfer, Withdrawal, or Deposit |
| **Timestamp** | Exact date and time of the transaction, with holiday spikes |
| **Transaction Status** | Success or Failed |
| **Fraud Flag** | Binary indicator for fraudulent transactions |
| **Geolocation (Latitude/Longitude)** | Real GPS coordinates from 50 largest US cities with slight random variation |
| **Device Used** | Mobile or Desktop |
| **Network Slice ID** | Ethernet, WiFi, 5G, LTE, or 3G depending on device type |
| **Latency (ms)** | Simulated delay per connection type (e.g., Ethernet 2–8 ms, LTE 35–90 ms) |
| **Slice Bandwidth (Mbps)** | Network bandwidth including anomalies |
| **PIN Code** | Four-digit security code (masked) |

---

## 🚀 Notable Enhancements

### 1. Realistic US Geolocation Data
- Coordinates from the **50 largest US cities**
- City selection weighted by **population**
- Small random jitter (±0.01–0.05°) for realistic map visualizations

### 2. Holiday Transaction Spikes
- **3.5×** volume increase for **Thanksgiving**, **Black Friday**, and **Christmas**
- Higher activity on all **US federal holidays**
- Useful for studying **seasonal patterns** and **system load impact**

### 3. Network and Latency Simulation
- Desktop: Ethernet or Wi-Fi (low latency for Ethernet)  
- Mobile: 5G, LTE, 3G, or Wi-Fi (latency adjusted per network type)

### 4. Anomaly Injection
- Extreme high-value transactions
- Zero or tiny amounts
- Same sender and receiver accounts
- Fraud flags and inconsistent statuses (e.g., “Success” with zero amount)
- Network performance outliers

---

## 📊 Dataset Summary
- **Total Records:** 10,000  
- **Year Covered:** January 1, 2024 – December 31, 2024  
- **Geographic Scope:** 50 largest cities in the United States  
- **Applications:** Fraud detection modeling, transaction pattern analysis, network performance monitoring, geospatial visualization, and machine learning experimentation

---

## 📥 How to Use
You can download the dataset and use it for:
- SQL query practice
- Data visualization projects (Tableau, Power BI)
- Machine learning models for fraud detection
- Exploratory data analysis in Python or R

```bash
# Example: load into Python
import pandas as pd
df = pd.read_csv("transaction_data_2024_connectivity_10k_holiday_boost_USA_coords.csv")
df.head()
