**Project Report: Amazon Reviews Classification**

**1. Project Overview**

The goal of this project was to build and evaluate a machine learning model to classify Amazon reviews into different rating categories (from 1 to 5) based on various features of the reviews.

**2. Data Description**

The dataset includes the following columns:
- **Unnamed: 0**: Index column (not used for modeling)
- **reviewerName**: Name of the reviewer
- **overall**: Rating given by the reviewer (target variable)
- **reviewText**: Text of the review
- **reviewTime**: Time of the review
- **day_diff**: Number of days since the review was written
- **helpful_yes**: Number of "helpful" votes received
- **helpful_no**: Number of "not helpful" votes received
- **total_vote**: Total number of votes received
- **score_pos_neg_diff**: Difference between positive and negative scores
- **score_average_rating**: Average rating score
- **wilson_lower_bound**: Wilson score interval lower bound

**3. Data Preprocessing**

1. **Feature Selection**:
   - Target variable: `overall` (rating)
   - Features: All columns except `overall`.

2. **Categorical Feature Handling**:
   - Categorical columns identified: `reviewerName`, `reviewText`, `reviewTime`
   - Encoding: One-Hot Encoding was applied to these categorical columns.

3. **Data Splitting**:
   - Training set: 70%
   - Test set: 30%

**4. Modeling**

**4.1 Model Used**
- Random Forest Classifier with 100 estimators.

**4.2 Model Training**
The Random Forest model was trained on the preprocessed feature set and target variable.

**4.3 Model Evaluation**
- **Classification Report**:
  - 1.0: Precision 0.41, Recall 0.12, F1-score 0.18
  - 2.0: Precision 0.00, Recall 0.00, F1-score 0.00
  - 3.0: Precision 0.00, Recall 0.00, F1-score 0.00
  - 4.0: Precision 0.33, Recall 0.01, F1-score 0.02
  - 5.0: Precision 0.80, Recall 0.99, F1-score 0.88
  - Accuracy: 0.79

## Accuracy Score: 0.79

## 4.4 Feature Importances
Feature importances were plotted to visualize which features contributed most to the model's decisions.

## 5. Visualizations

## 5.1 Classification Report Heatmap
A heatmap was generated to visualize precision, recall, and F1-score for each rating class.

## 6. Model Saving
The trained Random Forest model was saved to a file for future use.

## 7. Conclusion
The Random Forest Classifier achieved an accuracy of 0.79 on the test set. The classification report reveals that the model performs well on higher rating classes (e.g., 5.0), but struggles with lower rating classes (e.g., 1.0, 2.0). The feature importance plot helps in understanding which features are most influential in the model's predictions.

Future improvements may include further tuning of hyperparameters, incorporating additional features, or using more advanced models to improve classification performance, especially for lower rating classes.

### CHANDRA SEKHAR POTTURI
