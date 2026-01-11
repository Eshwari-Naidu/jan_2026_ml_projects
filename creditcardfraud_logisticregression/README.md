# 💳 Transaction Fraud Detection using Logistic Regression

## 📌 Project Overview
This project focuses on building a **Logistic Regression model** to detect **fraudulent financial transactions** using engineered features derived from transaction metadata.

The objective is to:
- Preprocess transaction data
- Engineer meaningful features
- Train a classification model
- Evaluate its performance
- Predict fraud on new, unseen transactions

---

## 📂 Dataset
The dataset used in this project is:

**`transactions_modified.csv`**

### Key Columns Used
- `amount` – Transaction amount
- `type` – Type of transaction
- `oldbalanceOrg` – Original balance of the sender
- `oldbalanceDest` – Original balance of the receiver
- `isFraud` – Target variable (1 = Fraud, 0 = Not Fraud)

---

## 🛠️ Feature Engineering
To improve model performance, the following features were created:

### 1️⃣ `isPayment`
- Binary feature
- `1` if transaction type is **PAYMENT** or **DEBIT**
- `0` otherwise

### 2️⃣ `isMovement`
- Binary feature
- `1` if transaction type is **CASH_OUT** or **PAYMENT**
- `0` otherwise

### 3️⃣ `accountDiff`
- Absolute difference between sender and receiver balances  
- Helps identify suspicious balance movements

```python
accountDiff = |oldbalanceOrg - oldbalanceDest|
