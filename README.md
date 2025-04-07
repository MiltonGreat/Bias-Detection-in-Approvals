# Loan Approval Bias Analysis

![screenshot-localhost_8888-2025 04 07-11_17_16](https://github.com/user-attachments/assets/28cd2d09-0174-46da-ae1a-236f547e5047)

### Overview

This project analyzes loan approval data to detect potential biases based on gender, marital status, and property area. Using statistical tests and visualization techniques, it assesses whether certain demographic groups face systematically higher or lower approval rates and provides actionable insights for ensuring fair lending practices.

#### Key Questions

1. Does gender influence loan approval rates?
2. Are married applicants more likely to be approved than single applicants?
3. Do approval rates vary significantly by property location?
4. Are there intersectional biases (e.g., female + rural applicants facing higher rejection)?

### Dataset

#### Columns
- Demographics: Gender, Married, Dependents, Education, Self_Employed
- Financials: ApplicantIncome, CoapplicantIncome, LoanAmount, Loan_Amount_Term, Credit_History
- Property: Property_Area (Urban/Rural/Semiurban)
- Target: Loan_Status (Y/N)

### Key Steps

1. Data Preprocessing
- Converted categorical Loan_Status (Y/N) to binary (1/0).
- Handled missing values (if any) before analysis.

2. Statistical Analysis
- Group-wise Approval Rates: Calculated approval percentages for each demographic group.
- Chi-Square Tests: Checked for statistically significant relationships between approval rates and sensitive attributes.
- Disparity Metrics:
- Disparity Ratio (min approval rate / max approval rate)
- Disparity Difference (max rate – min rate)

3. Visualization
- Bar Charts: Approval rates by gender, marital status, and property area.
- Heatmaps: Intersectional approval rates (e.g., Gender × Property Area).

4. Intersectional Analysis
- Examined combined effects (e.g., "Female + Rural" vs. "Male + Semiurban").

### Key Findings

- Gender alone does not significantly affect approval (p=0.566).
- Married applicants have moderately higher approval rates (71.69% vs. 64.00%).
- Property area has a STRONG impact:
- Semiurban (79.26%) > Urban (64.91%) > Rural (60.28%) (p=0.0004)
- Intersectional biases exist:
- Single + Urban applicants have the lowest approval rate (56.67%).
- Married + Semiurban applicants have the highest (81.75%).

### Conclusion

The analysis suggests that property area is the strongest predictor of loan approval disparities, with semiurban applicants significantly favored. While gender alone does not show bias, intersectional analysis reveals that women in rural/urban areas and single urban applicants face systemic disadvantages. These findings highlight the need for fair lending practices that ensure equitable access to credit across all demographic groups.

### Source

[Loan Application Data from Kaggle](https://www.kaggle.com/datasets/vipin20/loan-application-data)

