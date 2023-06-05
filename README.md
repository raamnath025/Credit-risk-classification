# Credit Risk Classification

## Description
The objective of this project is to utilize diverse machine learning techniques for training and assessing the effectiveness of Logistic Regression Models in discerning the creditworthiness of borrowers. Multiple methodologies were employed to train these models, and their performances were compared to identify the superior-performing model. The predictive variables within the model consist of two labels: `0` (representing a healthy loan) and `1` (indicating a high-risk loan).

## Steps
In the process of constructing the models, the dataset was split into features and labels, and further divided into training and testing sets. 

  * Machine Learning Model 1 was built by instantiating a logistic regression model and training with the original training sets (`X_train`, `y_train`), fitting it to the training sets, and using it to generate predictions. 
  * Machine Learning Model 2 was created by resampling the original training data using the `RandomOverSampler` module, instantiating a logistic regression model and fitting the resampled training sets (`X_resample`, `y_resample`) to the model, and generating predictions.

The performance of each model was evaluated based on the balance accuracy score, the confusion matrix, as well as the precision score, recall score, and f1-score in the classification report.


## Results
- **Machine Learning Model 1:**

  Model 1, trained on the original data, achieves an accuracy of 94.4% when predicting the two labels. The model exhibits excellent proficiency in predicting healthy loans, as evidenced by perfect precision and recall scores of 1.00. However, there is room for improvement in the model's performance when it comes to predicting high-risk loans. The precision score for high-risk loans stands at 0.87, indicating that only 87% of the actual high-risk loans were correctly predicted. Similarly, the recall score for high-risk loans is 0.89, implying that the model identified only 89% of all high-risk loans present in the dataset.

- **Machine Learning Model 2:**

  Model 2, trained on resampled data, demonstrates exceptional performance with a remarkable accuracy of 99.6% in accurately predicting the two labels. Notably, this model exhibits excellent precision and recall scores of 1.00 for predicting healthy loans, indicating that it can effectively identify all healthy loans in the dataset. Furthermore, although the precision score for high-risk loans remains at a commendable 0.87, the recall score has shown significant improvement, reaching a perfect score of 1.00. This improvement suggests that the model is now capable of accurately predicting all high-risk loans present in the dataset.

## Summary  
After conducting an analysis, it has been determined that **Model 2** exhibits superior performance compared to Model 1 in the prediction of high-risk loans. Additionally, Model 2 demonstrates higher accuracy overall in predicting both types of labels. Notably, Model 2 displays a notably high precision in identifying high-risk loans and successfully identifies all high-risk loans within the dataset. Such performance is considered commendable in this context. Consequently, it is recommended to employ Model 2 for the identification of high-risk loans and for achieving improved accuracy in label predictions.