# Project Overview
This project focuses on forecasting energy consumption on an hourly basis using the XGBoost algorithm. Accurate energy consumption forecasting is crucial for effective energy management, reducing costs, and ensuring a balanced supply-demand scenario.

# Dataset
PJM Hourly Energy Consumption Data PJM Interconnection LLC (PJM) is a regional transmission organization (RTO) in the United States. It is part of the Eastern Interconnection grid operating an electric transmission system serving all or parts of Delaware, Illinois, Indiana, Kentucky, Maryland, Michigan, New Jersey, North Carolina, Ohio, Pennsylvania, Tennessee, Virginia, West Virginia, and the District of Columbia. Data Source : https://www.kaggle.com/datasets/robikscube/hourly-energy-consumption

# Model
This project employs the XGBoost model for forecasting. Key steps include: <br>
- Data preprocessing: Handling Outliers, feature engineering.
- Training: Training the XGBoost model with Cross validation using TimeSeriesSplit to ensure having a robust model. <br>
  ![image](https://github.com/mahdihammi/Energy_Consumption_Forecasting_Using_XGBoost/assets/89527502/57434cb1-e3cd-4b00-99f6-c51939ff15e9) <br>
   - Score across folds 3742.5833 <br>
     Fold scores:[3760.8277187583353, 3420.313091887879, 3478.018038580526, 4052.5712055405547, 4001.186553933809]

- Evaluation: For this project, RMSE was chosen as the primary evaluation metric for the following reasons: <br>
    - Interpretability: RMSE is measured in the same units as the target variable (energy consumption in kWh), making it easier to interpret and understand the magnitude of the prediction errors. <br>
    - Penalizing Large Errors: RMSE gives higher weight to larger errors due to the squaring of the error terms. This is particularly important for energy consumption forecasting, where larger errors could have more significant implications for energy management and planning. <br>
![image](https://github.com/mahdihammi/Energy_Consumption_Forecasting_Using_XGBoost/assets/89527502/11ce706c-7f1a-498b-833a-ef9bbb00b5e9)


# Forecast on Future Dates
![image](https://github.com/mahdihammi/Energy_Consumption_Forecasting_Using_XGBoost/assets/89527502/737ff13a-5e53-4283-8d10-eedef3888765)
