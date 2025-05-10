# used-car-price-prediction-with-neural-network
A machine learning project to predict used car prices using a neural network model (MLPRegressor). The project involves preprocessing data, feature encoding, and dimensionality reduction (PCA) to improve model performance.
# Used Car Price Prediction with Neural Network

## Description
A machine learning project to predict used car prices using a neural network model (MLPRegressor). The project involves preprocessing data, feature encoding, and dimensionality reduction (PCA) to improve model performance.

## Table of Contents
- [Introduction](#introduction)
- [Dataset](#dataset)
- [Data Preprocessing](#data-preprocessing)
- [Model](#model)
- [Results](#results)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Introduction
This project aims to predict the price of used cars based on various features such as kilometers driven, car age, brand, engine size, and more. We use a neural network model (MLPRegressor) to train and predict car prices. The dataset is preprocessed to handle missing values, scale numerical features, and encode categorical variables.

## Dataset
The dataset used in this project contains information about various used cars, including:
- Car name (brand, model, and variant)
- Year of manufacture
- Kilometers driven
- Engine size
- Number of seats
- Fuel type, transmission, and ownership details

For this project, the dataset is loaded from a CSV file: `car_price.csv`. You can modify the path to the dataset as needed.

## Data Preprocessing
The preprocessing steps performed on the dataset include:
1. **Price Conversion**: The car prices are converted from 'Lakh' or 'Crore' format to numerical values in rupees.
2. **Feature Extraction**: Relevant features like the car's brand, model, and variant are extracted from the car name.
3. **Missing Value Imputation**: Missing values are handled by imputing the most frequent value in each column.
4. **Categorical Encoding**: Ordinal and One-Hot Encoding are used to convert categorical variables (e.g., ownership, fuel type) into numerical format.
5. **Scaling**: Numerical features are standardized using `StandardScaler` to improve model performance.
6. **Dimensionality Reduction**: Principal Component Analysis (PCA) is applied to reduce the number of features while retaining 95% of the variance.

## Model
The model used to predict car prices is a Multi-Layer Perceptron (MLP) Regressor, which is a type of artificial neural network. The model consists of two hidden layers with 32 and 16 neurons, respectively, and uses the ReLU activation function. The model is trained using cross-validation to evaluate its performance.

### Model Hyperparameters:
- Hidden layers: (32, 16)
- Activation function: ReLU
- Max iterations: 500
- Random state: 42

## Results
After training the model, the performance is evaluated using cross-validation with 5 folds. The evaluation metrics include:
- **Mean Absolute Error (MAE)**
- **R² Score**
- **Mean Squared Error (MSE)**

### Example output:
- **Mean MAE**: 0.0367
- **Mean R²**: 0.9972
- **Mean MSE**: 0.0027

These results demonstrate the high accuracy and low error of the model.

