# Engage2Value: From Clicks to Conversions

## 📌 Project Overview
**Engage2Value** is a machine learning project developed as part of the **MLP Project T22025** competition.  
The goal is to **predict a customer’s purchase value** using large-scale, session-level behavioral data collected across multiple digital touchpoints.

By modeling user engagement, device attributes, traffic sources, and geographical context, this project estimates the **monetary value of a session**, enabling data-driven marketing and conversion optimization.

---

## 🏁 Competition Details
- **Platform:** Kaggle (MLP Project T22025)
- **Evaluation Metric:** R² Score
- **Competition Duration:**  
  - Start: April 23, 2025  
  - End: July 28, 2025
- **Team Name:** Kaggle User ID

---

## 🎯 Problem Statement
Given anonymized session-level data from a digital commerce platform, predict the target variable:

> **`purchaseValue`** — total amount spent by a customer during a session.

This is a **regression problem** with highly sparse targets (many zero-value sessions).

---

## 📊 Dataset Summary
- **Total Rows:** 100,000+  
- **Total Features:** 105  
- **File Format:** CSV  
- **Size:** ~100 MB  

### Files
| File | Description |
|-----|-------------|
| `train_data.csv` | Training dataset with target variable |
| `test_data.csv` | Test dataset without target |
| `sample_submission.csv` | Submission format reference |

---

## 🧩 Key Feature Categories

### 1. User Behavior & Session Metrics
- `totalHits`, `pageViews`, `totals.bounces`
- `new_visits`, `totals.visits`
- `sessionNumber`, `sessionStart`

### 2. Device & Technical Attributes
- `deviceType`, `os`, `browser`, `screenSize`
- `device.language`, `browserMajor`
- `gclIdPresent`

### 3. Traffic & Marketing Source
- `userChannel`, `trafficSource`
- `trafficSource.medium`, `trafficSource.keyword`
- `trafficSource.campaign`, `trafficSource.adContent`
- `trafficSource.adwordsClickInfo.*`

### 4. Geographical Context
- `geoNetwork.city`, `locationCountry`
- `geoNetwork.continent`, `geoNetwork.subContinent`
- `geoNetwork.region`, `geoCluster`, `locationZone`

### 5. Identifiers
- `userId`, `sessionId`

---

## 🛠️ Methodology

### Data Preprocessing
- Handling missing values and inconsistent entries
- Encoding high-cardinality categorical features
- Log transformation / scaling of skewed numerical features
- Memory optimization for large datasets

### Modeling Approach
- Baseline regression model (dummy / simple estimator)
- Feature engineering on behavioral and session metrics
- Regression-based ML model for purchase value prediction

---

## 📈 Model Performance
- **Evaluation Metric:** R² Score
- **Final R² Score:** **0.61304**

This score indicates the model explains **~61% of the variance** in customer purchase value, despite heavy class imbalance and sparse target distribution.

---

## 📤 Submission Format
Predictions are generated for the test dataset and saved in the following format:

```csv
id,purchaseValue
0,0
1,0
2,10990000
3,36500
...
