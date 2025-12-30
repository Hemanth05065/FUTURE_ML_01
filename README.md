# Sales Forecasting using Prophet

## Project Overview

This project utilizes Facebook's Prophet library to perform time-series forecasting on sales data. The primary goal is to predict future sales and export the forecast in a format suitable for visualization and analysis in Power BI. The project is contained within a Jupyter Notebook (`m.ipynb`) that handles everything from data preparation to model evaluation and output generation.

## Dataset

The dataset used for this project is `WA_Fn-UseC_-Telco-Customer-Churn.csv`, which is expected to be located at `C:\Users\Hemanth\Downloads\WA_Fn-UseC_-Telco-Customer-Churn.csv`. This file should contain historical sales data with at least two columns: one for the date and another for the sales figures.

**Note:** The `WA_Fn-UseC_-Telco-Customer-Churn.csv` file is not included in this repository.

## Files in this Repository

- **`m.ipynb`**: This is the main Jupyter Notebook for the project. It includes all the Python code for data loading, preprocessing, model training with Prophet, generating forecasts, and evaluating the model's performance.
- **`prophet_forecast_output.csv`**: This CSV file is the output of the `m.ipynb` notebook. It contains the forecasted sales data, including the predicted value (`yhat`) and the uncertainty intervals (`yhat_lower`, `yhat_upper`).
- **`README.md`**: This file, providing an overview and instructions for the project.

## How to Use

1.  **Prerequisites**: Ensure you have Python and the necessary libraries installed. You can install the required libraries by running the first cell in the `m.ipynb` notebook.
    ```
    !pip install numpy pandas matplotlib seaborn scikit-learn prophet
    ```
2.  **Data**: Place the `WA_Fn-UseC_-Telco-Customer-Churn.csv` dataset in the `C:\Users\Hemanth\Downloads\` directory.
3.  **Run the Notebook**: Open and run the `m.ipynb` Jupyter Notebook. The notebook will:
    - Load and preprocess the data.
    - Train a Prophet model.
    - Generate a 30-day forecast.
    - Evaluate the forecast using MAE, RMSE, and MAPE metrics.
    - Save the forecast to `prophet_forecast_output.csv`.

## Notebook: `m.ipynb`

The `m.ipynb` notebook is structured as follows:

1.  **Installation and Imports**: Installs and imports all the necessary libraries.
2.  **Data Loading and Preparation**: Loads the `WA_Fn-UseC_-Telco-Customer-Churn.csv` dataset, renames the columns to `ds` and `y` as required by Prophet, and converts the date column to the correct format.
3.  **Train/Test Split**: Splits the data into training and testing sets to evaluate the model's performance.
4.  **Modeling**: Initializes and trains a Prophet model with yearly and weekly seasonality.
5.  **Forecasting**: Creates a future dataframe and generates predictions.
6.  **Evaluation**: Calculates and prints the Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and Mean Absolute Percentage Error (MAPE).
7.  **Visualization**: Plots the forecast and its components.
8.  **Export for Power BI**: Saves the forecast data to `prophet_forecast_output.csv`.

## For Future Interns/Contributors

**THIS PROJECT IS FUTURE INTERNS ASK 1**

Welcome to the Sales Forecasting project! This project serves as a great introduction to time-series analysis and forecasting using the Prophet library.

**Potential areas for future work and contribution:**

1.  **Hyperparameter Tuning:** Experiment with Prophet's hyperparameters to improve model performance.
2.  **Adding Regressors:** Incorporate additional regressors (e.g., holidays, promotional events) into the model.
3.  **Advanced Visualization:** Create more detailed and interactive visualizations of the forecast data, possibly using a dashboarding tool like Power BI, Streamlit, or Dash.
4.  **Error Analysis:** Perform a deeper analysis of the model's errors to understand where it performs well and where it struggles.
5.  **Alternative Models:** Compare Prophet's performance with other time-series forecasting models like ARIMA, SARIMA, or LSTMs.
