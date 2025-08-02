# Used Car Price Prediction

## 📖 Overview

This project aims to predict the selling price of used cars based on various features like the car's age, kilometers driven, fuel type, and more. The goal is to build a regression model that accurately estimates a car's value.

We explored and evaluated two different regression models for this task:
* Linear Regression
* Lasso Regression

The project demonstrates a complete machine learning pipeline, from data preprocessing and feature engineering to model training and evaluation.

## 📊 Dataset

The dataset used for this project contains information about used cars listed for sale. The data includes the following features:

| Feature | Description |
| :--- | :--- |
| **Car_Name** | The name of the car model. |
| **Year** | The year the car was manufactured. |
| **Selling_Price** | The price the car was sold for (in lakhs). **(Target Variable)** |
| **Present_Price** | The current showroom price of the car (in lakhs). |
| **Kms_Driven** | The total kilometers driven by the car. |
| **Fuel_Type** | The type of fuel the car uses (e.g., Petrol, Diesel, CNG). |
| **Seller_Type** | The type of seller (e.g., Dealer, Individual). |
| **Transmission** | The transmission type of the car (e.g., Manual, Automatic). |
| **Owner** | The number of previous owners the car has had. |

## ⚙️ Methodology

The project followed these key steps:

1.  **Data Loading & Initial Exploration:** The dataset was loaded into a pandas DataFrame. We performed an initial analysis to understand the data's structure, identify missing values, and examine basic statistics.

2.  **Data Preprocessing & Feature Engineering:**
    * Handled categorical features (`Fuel_Type`, `Seller_Type`, `Transmission`) by converting them into numerical format using one-hot encoding. This step is crucial for the regression models to process the data.

3.  **Model Training:**
    * The dataset was split into training and testing sets (typically an 90/10 split).
    * Two different regression models were trained on the preprocessed training data:
        * **Linear Regression:** A standard baseline model.
        * **Lasso Regression:** A regularized linear model that is effective in feature selection and can help prevent overfitting.

4.  **Model Evaluation:**
    * The trained models were used to make predictions on the unseen test set.
    * The performance of each model was evaluated using the R-squared (R²) score, which measures the proportion of the variance in the dependent variable that is predictable from the independent variables.

## 📈 Results

The performance of the two models on the test data is as follows:

| Model | Accuracy (R² Score) |
| :--- | :--- |
| **Linear Regression** | 83% |
| **Lasso Regression** | **84%** |

### Conclusion

Both models performed well, but the **Lasso Regression** model achieved a slightly higher accuracy of 84%. This suggests that the regularization technique used by Lasso was beneficial for this dataset, possibly by reducing the impact of less important features.

## 🤝 Contributing

Contributions are welcome! If you have suggestions for improving this project, please feel free to create an issue or submit a pull request.
