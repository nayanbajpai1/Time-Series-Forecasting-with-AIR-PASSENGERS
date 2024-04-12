## AIR-PASSENGERS (Time Series Forescasting)
![air passenger image](https://github.com/nayanbajpai1/Time-Series-Forecasting-with-AIR-PASSENGERS/assets/166288028/14bffb40-db01-485f-9ef9-d6a19be6bace)
## Objective : 
Given historical air passenger data, the objective of this study is to develop accurate forecasting models utilizing ARIMA (AutoRegressive Integrated Moving Average) and SARIMAX (Seasonal AutoRegressive Integrated Moving Average with Exogenous Variables) methodologies. The aim is to predict future passenger counts, thereby aiding in resource allocation, capacity planning, and operational decision-making within the aviation industry. By leveraging advanced time series analysis techniques, this research seeks to provide reliable insights into the anticipated trends and fluctuations in air travel demand.

## STEPS :
- Imported the necessary libraries.
- Loaded the dataset .
((which contains 144 rows and 2 columns, where 'month' is of object datatype and 'passengers' contains integers.))
- Converted the 'month' column to datetime format.
- Set 'month' as the index.
- Checked the pattern and distribution of the data.

![air1](https://github.com/nayanbajpai1/Time-Series-Forecasting-with-AIR-PASSENGERS/assets/166288028/fa2dce29-2db6-4484-b077-2aaede7219c6)

- Understood more about the data trend and seasonality through seasonal decomposition.

![air 2](https://github.com/nayanbajpai1/Time-Series-Forecasting-with-AIR-PASSENGERS/assets/166288028/e6471a47-0839-41d4-9b73-bd563d40d0e9)

- Conducted the Dickey-Fuller test (adfuller) to check if the data is stationary or non-stationary.
[Null hypothesis (H0): Data is non-stationary.
Alternative hypothesis (H1): Data is stationary.]
#### Concluded that the p-value is 0.99, indicating that the data is non-stationary.
### Made the data stationary.
- Applied rolling mean and standard deviation.
- Plotted the data.
  
![air3](https://github.com/nayanbajpai1/Time-Series-Forecasting-with-AIR-PASSENGERS/assets/166288028/3697e2ca-5120-471f-a228-5159a39a7908)

- Conducted a log transformation.
- Plotted the data again after the log transformation.

![air4](https://github.com/nayanbajpai1/Time-Series-Forecasting-with-AIR-PASSENGERS/assets/166288028/f3e4ea8b-4cf9-4efb-8f7c-508320c9fa0d)

- Adfuller test again to check data is stationary
#### p_value is greater that 0.05 hence again the data is non_stationary
- Performed differencing on the dataset.
- Plotted the differenced data.

![image](https://github.com/nayanbajpai1/Time-Series-Forecasting-with-AIR-PASSENGERS/assets/166288028/f4e67690-df3b-4693-a1f4-a72355e8aa8d)


- Compared the original plot with the differenced plot.

![image](https://github.com/nayanbajpai1/Time-Series-Forecasting-with-AIR-PASSENGERS/assets/166288028/91a25a49-1187-48bf-ba88-af0bb3b9f9de)

- Conducted the Dickey-Fuller test again.
#### Concluded that the p-value is 0.04, rejecting the null hypothesis and indicating that the data is now stationary.
## Successfully made the data stationary.
## Proceeded to model building:
- Utilized ARIMA.
- Utilized ACF and PACF plots to select the optimal values of p, d, q.

![image](https://github.com/nayanbajpai1/Time-Series-Forecasting-with-AIR-PASSENGERS/assets/166288028/144f39ba-4933-4dab-bbd7-578650662ca5)
![image](https://github.com/nayanbajpai1/Time-Series-Forecasting-with-AIR-PASSENGERS/assets/166288028/35223240-b6e6-4462-89bd-4be6ffaf5323)


- Divided the data into training and testing sets.
- Imported ARIMA.
- Build a model
- Plotted the model.

![image](https://github.com/nayanbajpai1/Time-Series-Forecasting-with-AIR-PASSENGERS/assets/166288028/8109a889-3fee-4c2a-a110-177d57f76b43)

#### Found that the model was not performing well.
- Utilized the second method, tuning with itertools.
- Checked RMSE with each order through a loop and identified the combination (7, 0, 7) with the least RMSE.
- Built a model with the selected parameters (7, 0, 7).
- Built the model and plotted it.

![image](https://github.com/nayanbajpai1/Time-Series-Forecasting-with-AIR-PASSENGERS/assets/166288028/ef41214b-e39f-4cf9-80fa-3b43a82a5fba)

- Forecasted for the next 5 years.
- Plotted the forecast.

![image](https://github.com/nayanbajpai1/Time-Series-Forecasting-with-AIR-PASSENGERS/assets/166288028/9b9c8a83-133f-495d-8661-d94311656429)

## Proceeded to build a SARIMA model.
- Built the SARIMA model and plotted it.

![image](https://github.com/nayanbajpai1/Time-Series-Forecasting-with-AIR-PASSENGERS/assets/166288028/52716fcc-9593-4b11-bb5a-838837c58889)

- Forecasted for the next five years using SARIMA.
- Plotted the SARIMA forecast.

![image](https://github.com/nayanbajpai1/Time-Series-Forecasting-with-AIR-PASSENGERS/assets/166288028/217c077b-2674-454f-9df3-aa3ebde17ad0)

### Confirmed the best model.
### End 

## This project successfully demonstrates the process of building time series forecasting models using ARIMA and SARIMA methodologies, providing valuable insights into predicting future air passenger counts. The detailed steps outlined here serve as a guide for future analysis in similar contexts."
