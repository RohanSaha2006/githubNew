Comprehensive Report: Model Implementations and Performance
Day 1: Codes and Performance
1. Random Forest Model
Description: A Random Forest classifier with specific hyperparameters.

Class Weights: Applied.

Key Hyperparameters:

n_estimators: 870

max_depth: 42

min_samples_split: 5

min_samples_leaf: 2

class_weight: {0: 1, 1: 3.5, 2: 1}

F1 Score: 80.147

2. Random Forest Model with Class Weights
Description: Same as the first model but with class weights to handle class imbalance.

Class Weights: Applied.

F1 Score: 79.645

3. Gradient Boosting Model without Class Weights
Description: A Gradient Boosting classifier with specified hyperparameters.

Class Weights: Not applied.

Key Hyperparameters:

n_estimators: 200

learning_rate: 0.1

max_depth: 3

F1 Score: 80.239

4. Gradient Boosting Model with Class Weights
Description: Gradient Boosting model with manually handled class weights by adjusting sample weights.

Class Weights: Applied manually.

F1 Score: 80.61

5. Random Forest with Hyperparameter Tuning
Description: Random Forest model tuned using grid search to find the best hyperparameters.

Class Weights: Applied.

Key Hyperparameters Found (example values):

n_estimators: 500

max_depth: 40

min_samples_split: 5

min_samples_leaf: 2

bootstrap: True

F1 Score: 80.039

6. Stacking Model (Gradient Boosting and Random Forest)
Description: Stacking classifier combining Gradient Boosting and Random Forest models with another Random Forest as the final estimator.

Class Weights: Not applied.

Key Components:

Base Estimators:

Gradient Boosting: n_estimators=200, learning_rate=0.1, max_depth=3

Random Forest: n_estimators=870, max_depth=42, min_samples_split=5, min_samples_leaf=2

Final Estimator: Random Forest with n_estimators=100

F1 Score: 79.946

Day 2: Codes and Performance
7. Random Forest Model
Description: A Random Forest classifier with specific hyperparameters.

Class Weights: Not applied.

Key Hyperparameters:

n_estimators: 700

max_depth: 35

min_samples_split: 4

min_samples_leaf: 2

F1 Score: 79.783

8. Random Forest Model with Fine-Tuning
Description: Random Forest model with directly fine-tuned parameters.

Class Weights: Not applied.

Key Hyperparameters:

n_estimators: 800

max_depth: 40

min_samples_split: 4

min_samples_leaf: 2

F1 Score: 81.095

9. Improved Feature Selection and Ensemble Methods
Description: Improved feature selection using SelectFromModel, and ensemble methods including Extra Trees Classifier and Voting Classifier.

Class Weights: Not applied.

Key Models:

Random Forest: n_estimators=870, max_depth=42, min_samples_split=5, min_samples_leaf=2

Extra Trees Classifier: n_estimators=500, max_depth=35, min_samples_split=4, min_samples_leaf=2

Voting Classifier: Soft voting combining the above models.

F1 Score: 80.94

10. Random Forest Model
Description: Random Forest classifier with fine-tuned parameters achieving the highest F1 score.

Class Weights: Applied.

Key Hyperparameters:

n_estimators: 870

max_depth: 42

min_samples_split: 5

min_samples_leaf: 2

class_weight: {0: 1, 1: 3.5, 2: 1}

F1 Score: 81.394

Summary
The different models varied in their approach to handling class weights, hyperparameter tuning, feature selection, and ensemble methods. The Random Forest model with fine-tuned parameters achieved the highest F1 score of 81.394, while the Stacking model without class weights achieved the lowest score of 79.946.

Each approach has its strengths and may perform differently depending on the dataset and problem. Continuous experimentation and tuning can further optimize these models for better performance.
