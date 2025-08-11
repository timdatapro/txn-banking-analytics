# txn-banking-analytics
Transaction Data for Banking Operations

# Dataset Overview

This dataset contains 10000 synthetic banking transactions for the year 2024. The transactions include Transfers Withdrawals and Deposits and are distributed across the 50 largest US cities proportionally weighted by population. Special attention was given to US federal holidays particularly Thanksgiving Black Friday and Christmas to model significant spikes in transaction activity.

Each record is enriched with realistic geolocation data device connectivity types latency ranges corresponding to network conditions and simulated anomalies such as fraud attempts outlier amounts and unusual account behavior. The dataset is suitable for financial analysis fraud detection geospatial analytics network performance evaluation and machine learning modeling.

# Key Features
Transaction ID Unique identifier for each transaction ensuring traceability
Sender Account ID The account number of the transaction sender
Receiver Account ID The account number of the transaction receiver
Transaction Amount The monetary value of the transaction with injected anomalies for extreme values and zero amount inconsistencies
Transaction Type Categorized as Transfer Withdrawal or Deposit
Timestamp Exact date and time of the transaction including spikes in volume on US public holidays and especially on Thanksgiving Black Friday and Christmas
Transaction Status Indicates whether the transaction was successful or failed
Fraud Flag Binary flag indicating transactions flagged as fraudulent
Geolocation (Latitude/Longitude) Real GPS coordinates from the 50 largest US cities proportionally distributed by population with small random variation to simulate realistic location spread
Device Used The type of device used to initiate the transaction Mobile or Desktop
Network Slice ID Represents realistic network or connection types. Desktop uses Ethernet or WiFi with low latency for Ethernet. Mobile uses 5G LTE 3G or WiFi with latency adjusted per network type
Latency (ms) Delay in milliseconds simulated according to connection type. Ethernet 2–8 ms Desktop WiFi 8–25 ms Mobile WiFi 10–30 ms 5G 15–45 ms LTE 35–90 ms 3G 90–220 ms
Slice Bandwidth (Mbps) Bandwidth available during the transaction including simulated anomalies for outlier conditions
PIN Code Four digit security code masked for privacy

# Notable Enhancements
Realistic US Geolocation Data Each transaction is assigned coordinates from the 50 largest US cities. City frequency weighted by population to reflect real world transaction distribution. Slight coordinate jitter added for realistic mapping visualization
Holiday Transaction Spikes Transaction volumes boosted for US federal holidays with 3.5x spikes on Thanksgiving Black Friday and Christmas. This is useful for studying seasonal transaction patterns and system load analysis
Network and Latency Simulation Device based connection types and latency values correspond to realistic network performance scenarios
Anomaly Injection Extreme high value transactions and zero or tiny amounts. Same sender and receiver accounts. Fraud flags and inconsistencies for example Success with zero amount. Network performance outliers
Total Records 10000
Year Covered January 1 2024 to December 31 2024
Geographic Scope 50 largest cities in the United States
Applications Fraud detection modeling transaction pattern analysis network performance monitoring geospatial visualization and machine learning experimentation
