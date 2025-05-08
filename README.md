# ComparingClassifiers
This repository consists of python code to compare various classifiers trained on a bank marketing campaign dataset. The python jupyter notebook can be found at: https://github.com/shalaka2001/ComparingClassifiers/blob/main/prompt_III.ipynb

## Business Objective:
Direct Marketing Campaigns to get bank customers to invest their money can be resource expensive with the need to staff people to make the phone calls. The Business Objective is to use the available data from previous campaigns to come up with a classification model to increase the efficiency of direct marketing campaigns for long-term deposit offer with reduced number of contacts. Targeting the customers who would agree to invest and minimizing the phone calls to customers who would decline the offer is the goal.

## Classification Model objective
#### Prioritize models with high precision in identifying customers who will accept the offer- High precision for the "Yes" class
#### Avoid costs on calling customers who will say "No" - High precision for the "Yes" class
#### Reduce lost opportunity by identifying customers as "No" when they could be "Yes" - High "No" recall
#### Low time to train

## Findings/Conclusion
### All models have accuracy slightly better or equal to baseline
#### Choice 1: Logistic Regression
~70% precision - when it predicts "Yes" it is right 70% of the time, minimizing identifying "No"s Excellent No Recall 99% - When the model predicts No, there are very few false positives i.e. Yes classified as "No" Low Yes recall 17.4% - When the model predicts "Yes", there are false positives Simple and fast to deploy and Scale

#### Choice 2: Decision Tree
~70.3% precision - when it predicts "Yes" it is right 70.3% of the time, minimizing identifying "No"s Excellent No Recall 99% - When the model predicts No, there are very few false positives i.e. Yes classified as "No" ~17.3% recall - comparable to Logistic Regression model Shallow Tree - fast and interpretable

#### Choice 3: SVM
~65% precision - when it predicts "Yes" it is right 65% of the time, minimizing identifying "No"s ~19.5% recall - slightly better than the Logistic Regression and Decision Tree models Excellent "No" recall 98.6% minimizing false positives Longer training times.

#### Not a choice: KNN:
Lowest precision 61.8% indicating calls will be made to uninterested customers Lowest accuracy 88.88%

### Factors influencing the acceptance of the offer:
#### Economic and Social factors tend to influence the decision of the consumer

#### Consumer price index which is a direct indicator of the inflation is seen to influence the decision- at a higher inflation rate, consumers want to spend less and invest more and are likely to accept the offer.

#### Euribor High Euribor(Euro Interbank Offered Rate) rate indicates stringent monetary policies and stress in the banking system, and people tend to invest less.

#### Employment variation rate indicates change in employment rate. If this value is negative, it indicates that people are losing job. It seems to have a negative correlation with the Acceptance indicating that as employment improves, people may not have time to look at the offers or make investments.

#### Consumer Confidence index - Higher value indicates that the customer may invest in the offer

#### Previous acceptance or rejection also seems to be influencing the decision.
If a customer has accepted previous investment offers they are likely to accept it again.

#### Students, unemployed or retired - above the age of 60 seem more likely to invest - looking to make money
Age group 20-59 seems to be declining the offer probably because they may have loans on their house or other things that they need to pay off.

#### Those with university degrees seem more likely to invest as they may have bank balance due to better paying jobs¶

## Next Steps
#### Bank should use the Logistic Regression or Decision Tree model to determine which customers can be part of their next marketing campaign
