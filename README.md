# ANN-Car-Sales-price-prediction

![image](https://github.com/user-attachments/assets/b73181ed-a05a-4735-94a9-e290dc1c1e85)

Script Analysis
# 1. Data Loading and Initial Inspection
**Dataset Reading:**
Reads the CSV file using pd.read_csv.
Encodes the file with ISO-8859-1 (useful for special characters).
**Dataset Inspection:**
Displays the first few rows (data.head()).
Provides metadata (data.info()) and descriptive statistics (data.describe()).

# 2. Data Preprocessing
Dropping Unnecessary Columns:

Columns like customer name, customer e-mail, and country are checked for existence before being dropped.
**Feature and Target Selection:**

Features (x) are selected as columns 0 to 3 (gender, age, annual salary, credit card debt).
The target variable (y) is the car purchase amount (column 5).
**Scaling:**

Both x and y are scaled using StandardScaler for normalization.
 # 3. Splitting the Dataset
Training and Testing Split:
Data is split into training and testing sets using an 80:20 ratio with a fixed random state for reproducibility.
# 4. Building the ANN
Architecture:

Two hidden layers with 10 neurons each, using ReLU activation.
Output layer has 1 neuron with linear activation (suitable for regression).
**Early Stopping:**

Configured to monitor validation loss and stop training early if no improvement is seen for 2 consecutive epochs.
# 5. Training the ANN
Optimizer: Adam optimizer with a learning rate of 0.01.
Loss Function: Mean Squared Error (MSE).
Metrics: Mean Absolute Error (MAE).
Training Parameters: Batch size of 50 and 70 epochs.
# 6. Evaluation
**Visualizations:**

Plots training and validation MAE over epochs.
Plots training and validation loss over epochs.
**Prediction:**

Makes predictions on the test set (y_pred).
**Performance Metric:**

Computes the R² score using r2_score, which measures the proportion of variance explained by the model.
Output Explanation
score: The R² score is a critical metric here. Multiplying it by 100 gives the percentage of variance in the target variable explained by the model.
For example, if score = 0.85, then score * 100 = 85%, meaning the model explains 85% of the variance in car purchase amounts.
Improvements & Suggestions
**Data Preprocessing:**

Verify data types (e.g., categorical variables like Gender) and handle them properly.
Include a check for missing or outlier values.
**Model Architecture:**

Increase the number of neurons or layers if the model is underfitting.
Add dropout layers to prevent overfitting (currently commented out).
**Hyperparameter Tuning:**

Experiment with learning rates, batch sizes, and activation functions.
Perform grid search or random search for optimal hyperparameters.
**Evaluation Metrics:**

Include additional metrics like Mean Absolute Percentage Error (MAPE) or Root Mean Squared Error (RMSE) for more interpretability.
Plot predicted vs. actual values for better visualization of model performance.
**Feature Engineering:**

Derive new features such as Debt-to-Income Ratio or interaction terms between features.
Consider using PCA or feature selection if the dataset grows.
**Interpretability:**

Use libraries like SHAP to understand feature importance and the model's decision-making process.
**Model Deployment:**

Save the trained model using model.save() and deploy it in a web interface for user predictions.
