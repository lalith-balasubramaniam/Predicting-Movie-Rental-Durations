
# Predicting Movie Rental Durations

## Project Overview
This project builds a regression model to predict the duration (in days) that customers rent DVDs, based on various rental features. The model is designed to help a DVD rental company optimize inventory management by accurately forecasting rental durations, thereby improving operational efficiency and customer satisfaction.

## Project Goals
- **Predict Rental Duration**: Create a model to forecast how long a DVD will be rented by a customer.
- **Optimize Inventory Management**: By understanding rental durations, the company can better plan inventory, reduce shortages, and prevent overstock.
- **Achieve Model Accuracy**: Target a mean squared error (MSE) of 3 or less on the test set to ensure reliable predictions.

## Dataset
- **File**: `rental_info.csv`
- **Description**: Contains information on each DVD rental, including rental and return dates, amount paid, DVD features, and movie ratings.
- **Key Features**:
  - `rental_date`, `return_date`: Rental start and end dates.
  - `amount`, `rental_rate`, `replacement_cost`: Pricing-related features.
  - `length`, `release_year`: Movie characteristics.
  - `special_features`: Indicates any special features like "Deleted Scenes" or "Behind the Scenes".
  - `NC-17`, `PG`, `PG-13`, `R`: Movie ratings represented as dummy variables.

## Instructions
### Data Preprocessing
1. **Load the Data**: Read `rental_info.csv` into a pandas DataFrame.
2. **Calculate Rental Duration**: Create a column `rental_length_days` representing the difference between `return_date` and `rental_date`.
3. **Feature Engineering**: 
   - Create dummy variables from `special_features`, specifically "Deleted Scenes" and "Behind the Scenes".
   - Remove columns that may leak information about the target variable.
4. **Define Features and Target**:
   - **Features (X)**: Relevant columns to predict rental duration.
   - **Target (y)**: `rental_length_days`.

### Model Selection and Evaluation
1. **Train-Test Split**: Split data into training and testing sets with 80% training and 20% testing.
2. **Modeling**: Use various regression models (e.g., Linear Regression, Decision Tree, Random Forest) to find the best predictor of rental duration.
3. **Evaluation**: Calculate the mean squared error (MSE) for each model and select the model with the lowest MSE (targeting an MSE ≤ 3).

### Results
- The best model achieved an MSE below 3, making it a reliable predictor for DVD rental durations.
- The model can assist the DVD rental company in optimizing inventory management by forecasting rental durations more accurately.

## Files
- `rental_duration_prediction.ipynb`: Jupyter Notebook with code for data preprocessing, model training, and evaluation.
- `README.md`: Project description and instructions.
- `requirements.txt`: List of dependencies needed to run the project.
- 'rental_info.csv' : Data Source

## Setup
1. **Install Required Libraries**:
   ```bash
   pip install -r requirements.txt
   ```
2. **Run the Notebook**: Open `rental_duration_prediction.ipynb` to see the full analysis and results.

## Conclusion
This project provides a regression model that effectively predicts DVD rental durations. By leveraging this model, the DVD rental company can improve its inventory management, resulting in a more efficient and customer-friendly operation.

