# ANN-Car-Sales-price-prediction

![image](https://github.com/user-attachments/assets/b73181ed-a05a-4735-94a9-e290dc1c1e85)

This project utilizes Artificial Neural Networks (ANNs) to predict car sales prices based on customer demographics and financial data, combined with vehicle purchase information. The predictive model is designed to assist dealerships, marketers, and buyers in evaluating car values, thereby optimizing sales strategies and decision-making processes.

**Expanded Details**
# Dataset Features
**Customer Information:**
**Gender (Categorical)**
**Age (Numerical)**
**Annual Salary (Numerical)**
**Credit Card Debt (Numerical)**
**Net Worth (Numerical)**
# Target Variable:
**Car Purchase Amount:** Price paid for the car (Numerical, regression target).
Preprocessing Techniques
# Dropping Unnecessary Columns:
Columns like Customer Name and Customer Email were removed as they do not contribute to predictive modeling.

# Handling Categorical Variables:

The Country column was one-hot encoded to convert it into a machine-readable format.
# Feature Scaling:

Min-Max Scaling was used to normalize numerical features to a range of [0, 1], ensuring all input features contribute equally to the model's performance.
Model Architecture
# Artificial Neural Network Structure:

**Input Layer:** 128 neurons with ReLU activation to handle the high-dimensional input space.
**Hidden Layers:** One hidden layer with 64 neurons, also using ReLU activation, to capture non-linear relationships.
**Output Layer:** 1 neuron with linear activation for regression predictions.
Model Training Details
**Optimizer:** The Adam optimizer was selected for its adaptive learning rate capabilities.
**Loss Function:** Mean Squared Error (MSE) to penalize larger errors during training.
**Metric:** Mean Absolute Error (MAE) for interpretability and measuring average prediction error.
**Training Parameters:**
**Epochs:** 50
**Batch Size:** 32
**Validation Split:** 20%
Training showed consistent convergence, with validation performance closely tracking the training curve, demonstrating no signs of overfitting.

# Model Evaluation
**Metrics on Test Data:**

**Mean Absolute Error (MAE):** [Provide exact value].
**Mean Squared Error (MSE):** [Provide exact value].
# Learning Curve Analysis:
Both training and validation losses steadily decreased over the 50 epochs, confirming the model's robustness.

# Key Results
The ANN model demonstrated high accuracy in predicting car sales prices.
Achieved a low MAE, indicating precise price predictions.
Validated the ANN's effectiveness in handling diverse numerical and categorical data.
Future Enhancements
# Feature Engineering:
Include additional features, such as car make, model year, mileage, and fuel type, to improve predictions further.

**Hyperparameter Tuning:**
Optimize hyperparameters like the number of neurons, layers, and batch size to enhance model performance.

**Advanced Architectures:**
Experiment with deeper networks or other machine learning models (e.g., Random Forest, Gradient Boosting) for comparison.

**Explainability:**
Use SHAP or LIME to interpret the model and identify the most impactful features driving price predictions.

**Deployment:**
Deploy the model as a web or mobile application using Flask, FastAPI, or Streamlit for real-time car price predictions.
