# Bank_Beta
Bank Beta's customers are gradually leaving the company: month by month, their numbers dwindle. Bank employees have realized that it would be more cost-effective for the company to focus on retaining their loyal existing customers rather than acquiring new ones.
In this case, our task is to predict whether a customer is likely to leave the bank soon or not. We have access to data regarding the behavior of past clients and their history of contract terminations with the bank. We will build a model with the highest possible F1 score. To pass the review, we need a minimum F1 score of 0.59 for the test dataset.

Afterward, we will make any necessary adjustments to our work and submit it for a second review. Additionally, we will measure the AUC-ROC metric and compare it with the F1 score.

## Goal

The project aims to develop a predictive model for identifying potential churn among Bank Beta customers, targeting an F1 score of 0.59 on the test dataset. We'll compare this score with the AUC-ROC metric and provide actionable insights for customer retention. Adjustments will be made to enhance model accuracy, and a brief report will be delivered with recommendations for the bank.

## Step

1. Data Preparation: Download and prepare the data, explaining the logic used during the preparation process.
2. Check Class Balance: Assess the balance of each class in the dataset. Train the model without considering class imbalances and briefly explain your findings.
3. Model Quality Improvement: Enhance the model's quality using at least two approaches to address class imbalance. Utilize both training and validation sets to find the best model and parameter combinations. Explain your findings briefly. Use the training set to select the best parameters. Improve model quality while considering class imbalance. Train multiple different models and find the best one.
4. Final Testing: Run the final testing phase.

## Data Description

Data required for this project can be found in the file `/datasets/Churn.csv`. Download the dataset.

**Features:**

- `RowNumber`: Index of string data
- `CustomerId`: Customer ID
- `Surname`: Last name
- `CreditScore`: Credit score
- `Geography`: Country of residence
- `Gender`: Gender
- `Age`: Age
- `Tenure`: Time period for customer's fixed deposit (in years)
- `Balance`: Account balance
- `NumOfProducts`: Number of bank products used by the customer
- `HasCrCard`: Whether the customer has a credit card (1 - yes; 0 - no)
- `IsActiveMember`: Customer's activity level (1 - yes; 0 - no)
- `EstimatedSalary`: Estimated salary

**Target:**

- `Exited`: Whether the customer has churned (1 - yes; 0 - no)

## Conclusion

In the project to predict customer churn for Bank Beta, the initial logistic regression model fell short of the target F1 score of 0.59, prompting exploration of various techniques to improve model performance. Class weight balancing techniques were applied, including upsampled and downsampled approaches, followed by experimentation with decision trees and random forests.

Despite significant efforts, none of the initial models met the target F1 score. However, the random forest classifier with class weight balancing emerged as the most promising candidate, achieving an F1 score of 0.6356 and an ROC AUC of 0.7909 during training. Subsequent evaluation with the test dataset revealed further improvements, with an F1 score of 0.6204 and an ROC AUC of 0.7764.

The confusion matrix analysis provided insights into the model's performance, revealing areas of strength and areas for improvement. Notably, while the model accurately identified a considerable number of customers who were likely to remain with the bank (True Negatives), it also correctly flagged a significant portion of potential churners (True Positives). However, there were instances of both false positives and false negatives, indicating areas where the model's predictions were less accurate. These findings underscored the importance of ongoing refinement and optimization of the predictive model to enhance its effectiveness in identifying customers at risk of churning.

Overall, the project demonstrated a systematic approach to addressing the challenge of customer churn prediction, leveraging a combination of data exploration, model training, and evaluation techniques. The successful development of a predictive model with improved performance opens up opportunities for Bank Beta to implement targeted retention strategies, ultimately bolstering customer satisfaction and loyalty while minimizing attrition.

## Future Work

1. Ensemble Methods: Experiment with ensemble techniques such as stacking or boosting to combine the strengths of multiple models and potentially improve predictive accuracy.
2. Feedback Loop: Implement a feedback loop where model predictions are used to inform customer interactions, and the outcomes of these interactions are fed back into the model to improve future predictions.
3. Segmentation: Refine the model by creating separate models for different customer segments to better tailor retention strategies and improve overall performance.
