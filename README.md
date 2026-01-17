# 🆔 Aadhaar Enrolment Anomalies & Fraud Detection
### **UIDAI Data Hackathon 2026**

[![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)](https://www.python.org/)
[![Machine Learning](https://img.shields.io/badge/ML-Ensemble_Learning-orange.svg)](https://scikit-learn.org/)
[![Status](https://img.shields.io/badge/Project-Hackathon_Submission-green.svg)]()

## 🧠 Team: CodData Defenders

---

## 📌 Project Overview
The **Aadhaar system** is India’s foundational digital identity infrastructure. Ensuring the integrity of enrolment and update processes is critical to preventing identity fraud and the misuse of public resources.

**CodData Defenders** has developed a multi-dimensional analytical framework that combines statistical anomaly detection with Machine Learning to identify fraudulent patterns. This project translates complex datasets into **actionable, policy-ready insights** to support UIDAI decision-making.

---

## 🎯 Key Objectives
* 🔍 **Detect Anomalies:** Identify fraudulent enrolment and update patterns.
* 👥 **Demographic Audit:** Flag geographic and temporal irregularities in age-group distributions.
* ⚠️ **Risk Scoring:** Develop a framework to prioritize high-risk cases for investigation.
* 🏛️ **Governance Insights:** Provide data-driven recommendations for system-wide improvement.

---

## 🧪 Methodology & Pipeline

### 1. Data Cleaning & Pre-Processing
* Converted raw timestamps into calendar features for temporal analysis.
* Engineered helper features: **Age-group percentages**, **Monthly/Yearly buckets**, and **Total Enrolment Growth Rates**.

### 2. Detection Engine
We utilize a hybrid approach to catch both simple outliers and complex fraud:
* **Statistical Filters:** Using IQR and Z-Score ($Z > 3\sigma$) to detect volume spikes.
* **Demographic Benchmarking:** Comparing enrolment data against **India Census** benchmarks to find unrealistic age-group concentrations.
* **Machine Learning:** Ensemble models (Gradient Boosting, Random Forest, and Logistic Regression) generate a **Fraud Probability Score (0–100)**.

---

## 📊 Key Findings
* 🚨 **Demographic Shift:** ~88% of analyzed records show abnormally high child enrolments (actual ~74% vs. expected ~9%).
* 📈 **Temporal Spikes:** Identified day-over-day enrolment surges as high as **384,000%**.
* 📍 **Concentration Risk:** Top 3 states account for nearly **39% of total anomalies**, suggesting organized activity.
* 🧹 **Data Integrity:** Detected a **4.5% exact duplicate rate** in raw enrolment logs.

---

## 🛠️ Technology Stack
| Category | Tools/Libraries |
| :--- | :--- |
| **Language** | Python 3.9+ |
| **Data Manipulation** | Pandas, NumPy |
| **Machine Learning** | Scikit-learn (Ensemble Methods) |
| **Statistics** | SciPy (Z-Score, Rolling Analysis) |
| **Visualization** | Matplotlib, Seaborn |

---

## 🚀 Impact & Recommendations
* **Administrative Impact:** Enables targeted audits of high-risk enrolment centres rather than inefficient blanket inspections.
* **Policy Insights:** Provides evidence for strengthening child enrolment verification in specific high-deviation districts.
* **Scalability:** The pipeline is designed to process **1M+ records in minutes**, making it ready for real-time integration.

---

## 🗂️ Repository Structure
```text
├── Aadhaar_Enrolment_Detection.ipynb  # Main Analysis & ML Pipeline
├── README.md                          # Project Documentation
├── visualizations/                    # State Heatmaps & Trend Charts
├── outputs/
│   ├── scored_dataset.csv             # Records with Risk Categories
│   └── high_risk_cases.csv            # Prioritized Investigation List
└── report/
    └── final_submission.pdf           # Detailed Policy & Governance Report
