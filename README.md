# Predicting Electricity Peak Consumption

This repository contains a project focused on forecasting electricity peak consumption, essential for optimizing energy use and management.

The project includes data preprocessing, analysis, and modeling to accurately predict electricity peaks.

## Table of Contents
+ Overview
+ Data
+ Dependencies
+ Usage
+ EDA
+ Results

---

## Overview
This project aims to analyze historical electricity consumption data to predict peak usage, benefiting both energy providers and consumers by enabling more efficient resource allocation and demand management.

## Data
**Resource Optimization AI Dataset**
- **Hour**: The current hour of data recording
- **15m, 30m, 45m, 60m (15m intervals)**: Electricity peak consumption values in 15-minute intervals
- **Average**: Average peak consumption over 15-minute intervals
- **Produced amount**: Quantity of goods produced within a given timeframe
- **Temperature, Humidity, Rainfall**: Weather data affecting consumption
- **Unit Price**: Electricity cost per unit, varies by season
- **Date fields**: Includes weekday (`day`), day (`d`), and month (`m`)
- **Number of people**: Number of personnel present
- **Personnel expense**: Associated labor costs
- **Target Variable**: Maximum consumption value within each 15-minute interval by hour

*Note*: The dataset (`data.csv`) is available on [KAMP AI](https://www.kamp-ai.kr). Ensure that column names align with the preprocessing steps outlined in the project notebook.

## Dependencies
The following libraries are required to run this project:

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`

You can install these dependencies via pip:

    pip install pandas numpy matplotlib seaborn

## Usage
To run the project:

1. Clone the repository:

       git clone https://github.com/daunnn/Predict_Electricity_Peak_Consumption

2. Navigate to the project directory:

       cd Predict_Electricity_Peak_Consumption

3. Open and run `Project.ipynb` in Jupyter:

       jupyter notebook Project.ipynb

## Exploratory Data Analysis (EDA)
- **Heatmap of Data**
  
    <img src=https://github.com/user-attachments/assets/8fb681e1-e80e-4aba-9fa6-f9aa70dd7fe1 width="500"/>
    
- **Target Variable Analysis**
  - Peak Consumption Boxplot for Each Month
  <img src=https://github.com/user-attachments/assets/5452fdf1-50a2-43d5-8f8d-2c46382db138 width="500"/>
    
  - Peak Consumption Boxplot for Each Hour
  <img src=https://github.com/user-attachments/assets/bc41a9f8-ba82-4a30-a4b5-86a95fc2b1bc width="500"/>
    
  - Target Variable Distribution
  <img src=https://github.com/user-attachments/assets/3ed902c9-0565-459e-9b89-d43dfb5a014d width="600"/>

## Results

### Predictive Model
We evaluated the following predictive models to compare performance:
- **Linear Regression**
- **Random Forest**
- **Recurrent Neural Network (RNN)** with 200 epochs

### Performance Measures
Model performance was evaluated using:
- **MAPE (Mean Absolute Percentage Error)**
- **MAE (Mean Absolute Error)**
- **MSE (Mean Squared Error)**
- **R-squared (Coefficient of Determination)**

### Cross-Validation
Each model’s accuracy was further validated through **5-fold cross-validation**.

**Model Performance Comparison**

| Model                | MAE ↓ | MSE ↓    | R-Squared ↑ | MAPE ↓ |
|----------------------|-------|----------|-------------|--------|
| Linear Regression    | 33.97 | 1823.02  | 0.52        | 73.70  |
| Random Forest        | 16.85 | 773.32   | 0.79        | 36.31  |
| RNN (epoch: 200)     | 31.71 | 2046.22  | 0.45        | 63.48  |

**Key Takeaways**
- Using predictive models, particularly Random Forest, significantly reduces prediction errors and better captures peak usage trends.
- Effective forecasting can help mitigate peak power occurrences, lowering electricity costs and improving resource efficiency.
- Continuous monitoring and model refinement will support sustainable power optimization in manufacturing processes. 

For visualizations and in-depth analysis, including comparisons across different models and prediction metrics, please see the `Project.ipynb` notebook.
