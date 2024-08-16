## Machine Learning Model Guiding Questions

- What are the specific objectives and success criteria for our machine learning model?
  The primary objective is to develop a robust model that accurately identifies fraudulent transactions within the credit card dataset.
  Success criteria include:
  `Accuracy`: High overall accuracy in detecting fraudulent transactions.
  `Precision`: High precision to minimize false positives (non-fraudulent transactions incorrectly labeled as fraudulent).
  `Recall`: High recall to ensure most fraudulent transactions are detected.
  `F1-Score`: A balanced F1-score that considers both precision and recall.
  `AUC-ROC`: A high AUC-ROC score to assess the model’s ability to distinguish between fraudulent and non-fraudulent transactions.

- How can we select the most relevant features for training our machine learning model?
  We selected features based on domain knowledge, data exploration, and feature importance analysis. By eliminating non-relevant features and refining the remaining ones, we ensured that only the most impactful features were used for training, enhancing the model’s performance.

- Are there any missing values or outliers that need to be addressed through preprocessing?
  We found no missing values in our data. However, we identified outliers and skewness in the `amt` and `city_pop` columns. To address this, we used StandardScaler and QuantileTransformer in our preprocessing pipeline to manage extreme values and skewed distributions, preserving the predictive power of the data.

- Which machine learning algorithms are suitable for our problem domain?
  We used Logistic Regression, Random Forest, and Gradient Boosting. We created four distinct pipelines (A, B, C, and D) with different preprocessing techniques and model configurations to evaluate and compare the performance of these algorithms in detecting fraudulent transactions.

- What techniques can we use to validate and tune the hyperparameters for our models?
  We initially used GridSearchCV for exhaustive hyperparameter tuning but switched to RandomizedSearchCV due to high memory usage and computation time. RandomizedSearchCV allowed us to efficiently sample parameter combinations and find near-optimal solutions. We also used cross-validation within the search process to validate each configuration and ensure robust model performance.

- How should we split the dataset into training, validation, and test sets?
  We used a standard approach to split the dataset, allocating 70-80% for training and 20-30% for testing. Additionally, we employed cross-validation during hyperparameter tuning to evaluate the model on multiple subsets of the data, ensuring it generalizes well and is not overfitted.

- Are there any ethical implications or biases associated with our machine learning model?
  Yes, our model faces ethical implications and biases. The imbalanced is_fraud target variable may lead to high false-negative rates for fraudulent transactions. We also considered data privacy, ensuring that anonymized or hashed credit card numbers do not expose sensitive personal information.

- How can we document our machine learning pipeline and model architecture for future reference?
  We documented our machine learning pipeline and model architecture comprehensively in our VS Code notebook. This includes details on preprocessing steps, models used (Logistic Regression, Random Forest, Gradient Boosting), their configurations, cross-validation strategy, and performance results. We pushed the notebook to GitHub, created pull requests, and followed version control practices to track changes and facilitate collaboration. This approach ensures that our work is well-documented, accessible, and maintainable for future reference.

- All individual reports can be found under `reports` folder

- Shahrzad: https://youtu.be/i7MbVCJOhn4
- Olha: https://drive.google.com/file/d/1zgue1hpz3XIEoAsNkSkgXeDrzwIttqiA/view?usp=sharing
- Stuart: https://drive.google.com/file/d/1dpWN4_CuQXEK80zJmirmtmuC6zi26Ibv/view?usp=drive_link
- Divya: https://drive.google.com/file/d/1nkHU-0IwI2YiBrIYPakx0O6ScnHsw1Ob/view?usp=share_link
- Sabare: https://drive.google.com/file/d/1hhKkCC6x_thwD5B_56YKhezEH8MgQ3AK/view?usp=sharing



- FYI: Team project 1 PR: https://github.com/sabarevasan/team_project/pull/9