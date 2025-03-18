# credit-risk-classification
## Analysis Overview
The purpose of this is to create a machine learning model that analyzes loan risk and predicts either a healthy or high risk loan for borrowers.

**Model type:** logistic regression  
**Concerns:** only 3.2% of the data was for high risk loans while the rest were healthy loans  
**Models created:**
- ***Model 1:*** trained and tested on randomly split data
- ***Model 2:*** trained on stratified/balanced data but tested on only stratified data

## Results
| Model | Accuracy Score | Healthy Loan (Precision) | Healthy Loan (Recall) | High Risk Loan (Precision) | High Risk Loan (Recall) |
|---| --- | --- | --- | --- | --- |
| Model 1 | 99.26% | 100% | 99% | 85% | 92%|
| Model 2 | 99.54% | 100% | 100% | 88% | 100% |

**Interpretation:**  
***Precision:*** % of loan status predictions that are correct  
***Recall:*** % of loan status that are identified

## Recommendation
Model 2 is recommended as it accounts for the uneven portion of healthy versus high risk loans. Therefore, it better predicts high risk loans and identified ~100% of all high risk loans--7% more than Model 1. Model 2 even slightly performs better than Model 1 for predicting healthy loans.

Furthermore, recall is the most important score here. Identifying, all high risk loans is more relevant than making sure healthy loans don't get miscategorized. It will just allow further investigation into those potentially risky loans; plus, Model 2 minimizes that miscategorization of healthy loans.