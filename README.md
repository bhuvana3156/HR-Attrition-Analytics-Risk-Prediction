# HR Employee Attrition: Analytics and Risk Prediction

**AICTE | IBM SkillsBuild Data Analytics with AI Internship 2026**
Submitted by: Bhuvaneshwari K

## Project Overview
This project analyses employee attrition using the IBM HR Analytics dataset. It finds the factors that drive employees to leave, builds machine learning models to predict who is at risk of leaving, and recommends retention strategies for HR teams.

## Dataset
IBM HR Analytics Employee Attrition & Performance (1,470 employees, 35 features, no missing values).
Link: https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset
File used: `WA_Fn-UseC_-HR-Employee-Attrition.csv`

## Project Description
1. Data cleaning: removed 3 constant columns, checked missing values and duplicates.
2. Feature engineering: attrition flag, age band, tenure band and income band.
3. Exploratory data analysis: attrition by department, job role, age, overtime, marital status, travel, work-life balance, income, satisfaction and tenure.
4. Machine learning: Logistic Regression and Random Forest with class balancing and a 0.35 decision threshold.
5. Risk scoring: every employee gets a 0 to 100 attrition risk score (Low / Medium / High).
6. Insights and recommendations for retention.

## Technologies Used
Python 3, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, Jupyter Notebook

## Setup and Run
```bash
# 1. Install dependencies
pip install -r requirements.txt

# 2. Download the dataset from the Kaggle link above and place
#    WA_Fn-UseC_-HR-Employee-Attrition.csv in the same folder as the notebook

# 3. Open and run all cells
jupyter notebook Bhuvaneshwari_HR_Attrition_Analysis.ipynb
```
Charts are also saved to a `figs/` folder when the notebook runs.

## Key Results
| Metric | Value |
|---|---|
| Overall attrition rate | 16.1% |
| Attrition with overtime vs without | 30.5% vs 10.4% |
| Highest-risk job role | Sales Representative (39.8%) |
| Highest-risk age band | 18-25 (35.8%) |
| Median income, leavers vs stayers | $3,202 vs $5,204 |
| Best model by ROC-AUC | Logistic Regression (0.808, recall 79.7%) |
| Random Forest | Accuracy 81.2%, ROC-AUC 0.772 (used for risk scores and feature importance) |

## Project Files
| File | Description |
|---|---|
| `Bhuvaneshwari_HR_Attrition_Analysis.ipynb` | Complete project code |
| `requirements.txt` | Python dependencies |
| `Bhuvaneshwari_ProjectReport.docx` | Full project report |
| `README.md` | This file |

## Limitations
The dataset is a fictional snapshot created by IBM data scientists. Model precision is moderate, so risk scores support HR decisions and should not replace them.
