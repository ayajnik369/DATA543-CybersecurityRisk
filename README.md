# DATA543-CybersecurityRisk
Final Presentation - DATA543: Quantifying Cyber Security Risk in the US

# Quantifying Cybersecurity Risk to U.S. Critical Infrastructure
**DATA543 Final Project** · Tal Fayer, Rebecca Tabakin, Anya Yajnik · May 2026

## Overview
This project quantifies cybersecurity risk to U.S. healthcare infrastructure using 
a Hazard–Exposure–Vulnerability framework applied to HHS OCR breach data (2021–2026) 
and CISA's Known Exploited Vulnerabilities catalog.

**Central finding:** Healthcare Clearing Houses face 100% high-risk classification; 
network server exposure and hacking incidents are the dominant severity drivers 
across both a logistic regression classifier (AUC = 0.735) and a Lasso regression 
(R² = 0.22).

## Repository Contents
| File | Description |
|------|-------------|
| `data543_final.py` | Full analysis pipeline — data cleaning, feature engineering, classification, regression, risk rankings |
| `DATA543_Final_Presentation_v2.pptx` | Final presentation slides |
| `DATA543_Presentation_Script.docx` | Speaker script divided across 3 presenters |
| `breach_report.csv` | HHS OCR healthcare breach data (2021–2026) |
| `known_exploited_vulnerabilities.csv` | CISA KEV catalog used for hazard features |

## Data Sources
- [HHS OCR Breach Portal](https://ocrportal.hhs.gov/ocr/breach/breach_report.jsf)
- [CISA Known Exploited Vulnerabilities Catalog](https://www.cisa.gov/known-exploited-vulnerabilities-catalog)

## Methods
- **Part A:** Logistic regression with L2 regularization + SMOTE oversampling for high-risk classification
- **Part B:** Lasso (L1) regression for continuous breach severity prediction
- Risk ranked by entity type, breach type, and geography

## Key Results
| Entity Type | High-Risk Rate | Avg Individuals Affected |
|-------------|---------------|--------------------------|
| Healthcare Clearing House | 100% | 218,315 |
| Business Associate | 32% | 1,651,554 |
| Healthcare Provider | 23% | 101,275 |
| Health Plan | 18% | 309,079 |
