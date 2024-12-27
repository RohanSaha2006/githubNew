Brief Report: Model Implementations and Performance
1. Random Forest Model
   Description: A Random Forest classifier was used with specific hyperparameters including the number of trees, maximum 
   depth, minimum samples split, and minimum samples per leaf node.

Class Weights: Applied.

Key Hyperparameters:

n_estimators: 870

max_depth: 42

min_samples_split: 5

min_samples_leaf: 2

class_weight: {0: 1, 1: 3.5, 2: 1}

F1 Score: 80.147

2. Random Forest Model with Class Weights
Description: Same as the first model but with the addition of class weights to handle class imbalance.

Class Weights: Applied.

F1 Score: 79.645

3. Gradient Boosting Model without Class Weights
Description: A Gradient Boosting classifier was used with specified hyperparameters including the number of boosting stages, learning rate, and maximum depth of the individual estimators.

Class Weights: Not applied.

Key Hyperparameters:

n_estimators: 200

learning_rate: 0.1

max_depth: 3

F1 Score: 80.239

4. Gradient Boosting Model with Class Weights
Description: The same Gradient Boosting model as above, but with manually handled class weights by adjusting sample weights.

Class Weights: Applied manually.

F1 Score: 80.61

5. Random Forest with Hyperparameter Tuning
Description: A Random Forest model was tuned using grid search to find the best hyperparameters.

Class Weights: Applied.

Key Hyperparameters Found (example values):

n_estimators: 500

max_depth: 40

min_samples_split: 5

min_samples_leaf: 2

bootstrap: True

F1 Score: 80.039

6. Stacking Model (Gradient Boosting and Random Forest)
Description: A Stacking classifier combining Gradient Boosting and Random Forest models, with another Random Forest as the final estimator.

Class Weights: Not applied.

Key Components:

Base Estimators:

Gradient Boosting: n_estimators=200, learning_rate=0.1, max_depth=3

Random Forest: n_estimators=870, max_depth=42, min_samples_split=5, min_samples_leaf=2

Final Estimator: Random Forest with n_estimators=100

F1 Score: 79.946

Summary
The different models varied in their approach to handling class weights, hyperparameter tuning, and the use of ensemble methods. Among the models, the Gradient Boosting with manually adjusted class weights achieved the highest F1 score of 80.61, while the Stacking model without class weights achieved the lowest score of 79.946.

Each approach has its own strengths and may perform differently depending on the specific characteristics of the dataset and the problem at hand. Continuous experimentation and tuning can further optimize these models for even better performance.


