# 🏦 Bank Transaction Analysis

This project involves data exploration and anomaly detection on a bank transaction dataset using clustering and statistical techniques. The goal is to derive insights and detect potential fraudulent patterns using unsupervised methods.

## 📁 Files

- `Bank_Transaction.ipynb` – Jupyter Notebook with full data analysis and modeling steps.
- `bank_transactions_data_2.csv` – Dataset containing transaction records, user details, and metadata for analysis.

---

## 📊 Dataset Overview

The dataset contains the following fields:

- `CustomerID`
- `TransactionDate`
- `PreviousTransactionDate`
- `TransactionAmount`
- `TransactionType`
- `Merchant`
- `Age`
- `Location`
- `IPAddress`
- `DeviceID`
- `LoginAttempts`

---

## 🔍 Analysis Overview

### 📌 Preprocessing
- Converted date columns to datetime format.
- Extracted `hour`, `day`, `month`, and `day of week` from `TransactionDate`.

### 📈 Exploratory Data Analysis (EDA)
- **Distribution plots** of `TransactionAmount` and `TransactionType`.
- **Transaction trends** by hour, day, and age group.
- **Geographical spread** using location data.
- **Customer behavior**:
  - Login attempts vs. transaction amount (fraud risk signals)
  - Time gaps between transactions
  - Variation in IP and device combinations
  - Identification of frequently used merchants

---

## 🤖 Modeling

### Anomaly Detection
- **Isolation Forest** used to detect unusual transactions.
- **StandardScaler** applied for normalization before modeling.

### Clustering
- **K-Means Clustering** used to group transactions based on behavior.
- Features selected from temporal, behavioral, and monetary variables.

---

## 📦 Requirements

```bash
pandas
numpy
matplotlib
seaborn
scikit-learn
```

---

## ▶️ How to Run

1. Open the `Bank_Transaction.ipynb` file in Jupyter Notebook or Google Colab.
2. Ensure `bank_transactions_data_2.csv` is in the same directory or update the file path accordingly.
3. Run each cell to:
   - Load and prepare the data
   - Perform EDA and visualization
   - Detect anomalies
   - Cluster transaction behaviors
