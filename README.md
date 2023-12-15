# Urban Air Pollution Prediction Tool

This tool utilizes machine learning algorithms to predict global PM2.5 levels leveraging accessible satellite data (Sentinel 5P) and weather data (Global Forecast System - GFS). The predictions aim to provide reliable information to the World Health Organization for policy initiatives aimed at mitigating PM2.5 exposure worldwide.

## Overview

The project focuses on predicting PM2.5 levels globally, which is essential for understanding and addressing urban air pollution. The tool utilizes various machine learning models, such as Random Forest, Gradient Boosting, Extra Trees, K-Nearest Neighbors, and Linear Regression, to predict PM2.5 levels based on satellite and weather data.

## Methodology
The code in this repository leverages machine learning regressors from scikit-learn library for predicting PM2.5 levels:

### Model Stacking

The stacking technique is employed to combine multiple regression models for enhanced prediction accuracy. The following stacking approaches were explored:

- StackingRegressor: A stacking ensemble method is employed using various base regressors and a final estimator.
- RandomForestRegressor, LinearRegression, KNeighborsRegressor, GradientBoostingRegressor, ExtraTreesRegressor, and Ridge: These regressors are used as base models within the stacking ensemble.

### Stacking Regressor 1

- **Models Used**: Linear Regression, K-Nearest Neighbors, Gradient Boosting, Extra Trees
- **Final Estimator**: Linear Regression
- **Evaluation Metrics**:
  - Mean Squared Error (MSE)
  - Root Mean Squared Error (RMSE)
  - R-squared (R²)
  - Adjusted R-squared


### Stacking Regressor 2

- **Models Used**: Linear Regression, Extra Trees
- **Final Estimator**: Linear Regression
- **Evaluation Metrics**:
  - MSE
  - RMSE
  - R²
  - Adjusted R²


### Stacking Regressor 3

- **Models Used**: Linear Regression, K-Nearest Neighbors, Gradient Boosting, Extra Trees
- **Final Estimator**: RandomForest
- **Evaluation Metrics**:
  - MSE
  - RMSE
  - R²
  - Adjusted R²


### Stacking with Ridge Regression

- **Models Used**: Random Forest, K-Nearest Neighbors, Gradient Boosting, Extra Trees
- **Final Estimator**: Ridge Regression
- **Evaluation Metrics**:
  - MSE
  - RMSE
  - R²
  - Adjusted R²


## Usage

1. **Input Data:** Ensure input data includes Sentinel 5P satellite data, GFS weather data, and relevant features for prediction.
2. **Python Environment:** Install necessary Python packages (`scikit-learn`, `numpy`, `pandas`, etc.).
3. **Model Training:** Use the provided code to train and evaluate the stacking regressors.
4. **Prediction:** Utilize the trained models to make predictions for global PM2.5 levels.

### Prerequisites

- Python 3.x
- Required Python packages (list them)
- Access to Sentinel 5P satellite data and Global Forecast System (GFS) for weather data

# Installation and Dependencies

## Prerequisites

- Python 3.x (recommended)
- Anaconda or virtual environment manager (optional but recommended)

## Setup Steps

1. **Clone Repository:** Clone or download the repository containing the PM2.5 prediction tool.

2. **Create Virtual Environment (Optional):**
    ```bash
    # Create a virtual environment (optional but recommended)
    conda create --name pm25_env python=3.8   # Replace `pm25_env` with your preferred environment name
    conda activate pm25_env                   # Activate the virtual environment
    ```
   
3. **Install Required Packages:** 
    ```bash
    # Navigate to the project directory
    cd path/to/your/project/directory

    # Install required packages using pip
    pip install -r requirements.txt
    ```
    Replace `requirements.txt` with the actual filename if different.

4. **Run the Code:** Execute the provided Python scripts or Jupyter notebooks to train and evaluate the PM2.5 prediction models.

## Dependencies

- `scikit-learn`: Machine learning library for Python.
- `numpy`: Library for numerical computations in Python.
- `pandas`: Data manipulation and analysis library.
- Other necessary dependencies specified in the requirements file.



## Conclusion

The project demonstrates the potential of machine learning models to predict global PM2.5 levels using accessible satellite and weather data. The insights gained can aid policymakers in implementing effective strategies to mitigate air pollution.


## References

- `scikit-learn` documentation: [Scikit-Learn](https://scikit-learn.org/)
- Sentinel 5P Satellite Data: [Sentinel 5P](https://sentinels.copernicus.eu/web/sentinel/missions/sentinel-5p)
- Global Forecast System (GFS): [GFS](https://www.weather.gov/gis/nwp)

## License

This project is licensed under the [MIT License](LICENSE).

