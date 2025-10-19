**Predicting Health Insurance Charges Using Linear and Ridge Regression with Cross-Validation
**

Contributions:

Hrrishita - data preprocessing & model training and evaluation

Lara - Improving model peformance

Dinmukhammed - Analysis and Comparison (MSE and R2)

1. Project Overview
This project focuses on developing and evaluating regression models to predict individual health insurance charges based on demographic and lifestyle factors.
Two models were implemented and compared: Linear Regression and Ridge Regression, with cross-validation applied to optimize model performance.
The objective is to assess whether the Ridge regularization technique enhances model generalization and reduces overfitting.

2. Dataset Description
The dataset utilized in this study is the Medical Insurance Cost dataset obtained from Kaggle.
It contains 1,338 observations with 7 features, including both numerical and categorical variables.

Feature	Description
age -	Age of the insured individual
sex - Gender (male/female)
bmi - Body Mass Index — a measure of body fat based on height and weight
children - Number of dependents covered by the insurance
smoker - Smoking status (yes/no)
region - Residential region in the United States
charges - Dependent variable — individual medical insurance cost

The dataset was selected for its simplicity, completeness, and suitability for regression modeling.

3. Methodology
3.1 Data Preprocessing
Imported and inspected the dataset for missing values and data consistency.
Applied One-Hot Encoding to convert categorical variables (sex, smoker, region) into numerical format.
Performed feature scaling using standardization to ensure equal weighting of variables.

3.2 Data Splitting
The dataset was divided into training (80%) and testing (20%) subsets to enable model evaluation on unseen data.

3.3 Model Development
Linear Regression was implemented as a baseline model.
Ridge Regression was trained with cross-validation to identify the optimal regularization parameter α (alpha) that minimizes prediction error.

3.4 Model Evaluation
Performance was assessed using the following metrics:
Mean Squared Error (MSE) — quantifies the average squared difference between actual and predicted values.
R² Score — represents the proportion of variance in the target variable explained by the model.
Both metrics were computed for training and testing data to evaluate model fit and generalization.

4. Results and Analysis
Model	Train MSE	Test MSE	Train R²	Test R²
Linear Regression	0.2305	0.2305	0.7400	0.7696
Ridge Regression (α = 0.278)	0.2290	0.2290	0.7400	0.7712

Both models achieved similar performance on the training data (R² ≈ 0.74).
The Ridge Regression model produced a marginally lower test MSE (0.2290 vs. 0.2305) and a slightly higher test R² (0.7712 vs. 0.7696).
These results indicate that Ridge Regression provided minor improvements in generalization, consistent with its ability to reduce overfitting through regularization.
The difference was minimal due to the dataset’s well-behaved nature and low multicollinearity among predictors.

5. Technologies Used
Programming Language: Python
Libraries:
Pandas
NumPy
Scikit-learn
Matplotlib / Seaborn

6. Conclusion
This study demonstrates the effectiveness of both Linear and Ridge Regression models in predicting health insurance costs.
While their performances were comparable, Ridge Regression exhibited a slight improvement in predictive accuracy and generalization.
Such regularization techniques become more advantageous when applied to complex or noisy datasets, where they help prevent overfitting and enhance model stability.
