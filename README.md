# UIDAI-DATA-HACKATHON-2026
![Uploading image.png…]()

Aadhaar Enrolment Anomalies & Fraud Detection
UIDAI Data Hackathon 2026

Team Name
CodData Defenders

Problem Statement
Unlocking Societal Trends in Aadhaar Enrolment and Updates

The Aadhaar system is India’s foundational digital identity infrastructure. Ensuring the integrity, fairness, and reliability of Aadhaar enrolment and update processes is critical for preventing identity fraud, misuse of public resources, and erosion of public trust.

This project aims to identify meaningful patterns, trends, anomalies, and predictive indicators in Aadhaar enrolment and update data and translate them into actionable insights and system‑level improvement frameworks to support informed decision‑making by UIDAI.

Objectives
Detect anomalous and potentially fraudulent enrolment patterns

Identify demographic, geographic, and temporal irregularities

Develop a risk‑scoring framework for prioritised investigation

Provide policy‑ready insights for governance and system improvements

Datasets Used (UIDAI – Official Hackathon Datasets)
1. Aadhaar Enrolment Dataset
Fields Used

Date of enrolment

State, District, PIN code

Age groups: 0–5, 5–17, 18+

Total enrolments

Purpose

Trend analysis (daily / monthly)

Demographic distribution analysis

Geographic concentration analysis

2. Aadhaar Demographic Update Dataset (optional extension)
Fields

Name, address, DOB, gender, mobile updates

State / District / PIN

Update counts by time

Purpose

Identify abnormal update frequencies

Detect geographic & temporal spikes

3. Aadhaar Biometric Update Dataset (core ML work)
Fields

Fingerprint, iris, face update counts

Age group wise biometric updates

Date, state, district, PIN

Purpose

Detect re‑enrolment misuse

Identify abnormal biometric update behaviour

Methodology
We implemented a multi‑dimensional analytical framework combining statistical analysis, anomaly detection, and machine learning.

Step 1: Data Cleaning & Pre‑Processing
Parsed numeric dates into calendar dates

Created helper features:

Total enrolments

Age group percentages

Monthly & yearly time buckets

Validated:

100% completeness

Valid dates and geographic codes

Removed inconsistencies and flagged duplicates

Step 2: Statistical Anomaly Detection
Techniques Used

IQR Method – Detects extreme outliers

Z‑Score Analysis – Identifies deviations >3σ

Rolling Mean & Volatility Analysis – Detects spikes/drops

Applied On

Total enrolments

Age‑wise enrolments

Daily trends

Step 3: Demographic Pattern Analysis
Compared actual age distributions against India Census benchmarks

Calculated demographic deviation scores

Flagged records with:

Extreme child dominance (>80%)

Single age group dominance (>95%)

Step 4: Geographic Concentration Analysis
Aggregated enrolments at:

State

District

PIN code

Identified:

High‑risk states & districts

Abnormally concentrated enrolment centres

Step 5: Temporal Behaviour Analysis
Daily enrolment trend analysis

Detected:

Sudden spikes (>200%)

Sudden drops (>50%)

Weekday bias analysis

Step 6: Feature Engineering (ML‑Ready)
Created 30+ fraud risk indicators across:

Demographic patterns

Geographic concentration

Temporal volatility

Data quality issues

Cross‑feature interactions

Step 7: Machine Learning Models
Models Used

Gradient Boosting

Random Forest

Logistic Regression

Ensemble (Soft Voting)

Output

Fraud probability score (0–100)

Risk categorisation:

Low

Medium

High

Critical

Key Findings & Insights
1. Severe Demographic Anomalies
~88% of records show abnormally high child enrolments

Actual child share: ~74% vs expected 9%

2. Geographic Concentration
Top 3 states account for ~39% of total enrolments

Indicates organised or systemic irregularities

3. Temporal Volatility
Extreme spikes (up to 384,000% day‑over‑day)

Strong weekday bias suggesting batch processing

4. Data Quality Issues
~4.5% exact duplicate records

High risk of duplicate identity creation

Visualisations Created
Demographic distribution vs census benchmarks

State & district heatmaps

Daily enrolment trend with anomaly flags

Fraud risk score distribution

Risk category breakdown by state

Top high‑risk enrolment centres

(All visualisations are included in the notebook and final PDF.)

Impact & Applicability
Administrative Impact
Enables targeted audits instead of blanket inspections

Supports real‑time monitoring of enrolment centres

Improves data integrity & public trust

Policy Insights
Evidence‑based enrolment policy design

Early warning system for systemic misuse

Scalability
Handles 1M+ records in minutes

Extendable to real‑time UIDAI systems

Governance & System Improvement Recommendations
Immediate
Investigate high‑risk centres and districts

Enforce duplicate detection at enrolment time

Enable automated anomaly alerts

Medium‑Term
Risk‑score enrolment centres

Strengthen child enrolment verification

District‑level benchmarking

Long‑Term
ML‑based predictive fraud prevention

Real‑time biometric cross‑verification

Public transparency dashboards

Technology Stack
Python (Pandas, NumPy, Scikit‑learn)

Statistical Methods (IQR, Z‑Score, Rolling Analysis)

Visualisation (Matplotlib, Seaborn)

ML Models (GBM, RF, Logistic Regression)

Repository Structure
├── Aadhaar Enrolment Anomalies Detection.ipynb
├── README.md
├── visualizations/
├── outputs/
│   ├── scored_dataset.csv
│   ├── high_risk_cases.csv
└── report/
    └── final_submission.pdf
Conclusion
This project demonstrates how data‑driven analytics and AI can uncover deep societal and systemic patterns in Aadhaar enrolment data.
The proposed framework is scalable, explainable, and directly actionable, making it suitable for real‑world governance deployment by UIDAI.
