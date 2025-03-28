This project addresses the challenge from SNCF-Transilien—the suburban train operator of Île-de-France—to forecast the daily number of ticket validations at 448 train stations. Accurate predictions will help anticipate growing passenger volumes and optimize service planning.

Overview
SNCF-Transilien processes over 2.3 million validations per day, with a steady annual growth of about 6% (2015–2019). The goal of this project is to predict the number of daily validations (variable y) per station for the period January 1, 2023, to June 30, 2023. The forecasting problem leverages historical data (from January 1, 2015 to December 31, 2022) and exogenous variables.

Data Description
Training Data (train.csv):

Contains 1,237,971 rows and 6 columns.

Daily validations for 448 stations between January 1, 2015, and December 31, 2022.

Test Data (test.csv):

Contains 78,652 rows and 6 columns.

Daily validations for the same stations from January 1, 2023, to June 30, 2023.

Variables:

date: Date of validation (YYYY-MM-DD).

station: Anonymized station identifier (3-character code).

job: Binary indicator (1 if it’s a regular workday; 0 otherwise).

ferie: Binary indicator (1 if it’s a public holiday; 0 otherwise).

vacances: Binary indicator (1 if it’s a school vacation day; 0 otherwise).

y: Number of validations on that day at that station.

Objective
Develop a forecasting model to predict daily validations at each station for January–June 2023. This project explores various time series forecasting methods, incorporating exogenous variables, and compares them to a baseline model that projects 2022 data to 2023 with day-of-week alignment.

Methodology
Data Analysis & Preprocessing:

Perform exploratory data analysis (EDA) to identify trends, seasonality, and anomalies.

Clean the data and handle missing values.

Engineer features using exogenous variables (job, holiday, vacation).

Modeling Approaches:

Baseline Model: Replicate the 2022 validation data for 2023 by aligning days of the week.

Forecasting Models: Experiment with traditional time series methods and machine learning models (e.g., regression, tree-based methods, and deep learning approaches) tailored for time series forecasting.

Evaluation:

Use metrics such as Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and R² score to assess model performance.

Compare the models’ forecasts against the baseline.

Analysis & Improvement:

Visualize historical trends and forecast performance.

Analyze error distributions and discuss potential improvements (e.g., parameter tuning, incorporating additional features, ensemble methods).
