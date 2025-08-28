# Solar-Power-Output-Prediction-using-Machine-Learning
"Built a Solar Power Forecasting model using weather data (temperature, irradiance, humidity, wind). Tested ML models (Linear Regression, Random Forest, Neural Networks, ARIMA). Achieved >99.99% accuracy (R² ~0.9999) with Random Forest, outperforming baseline and classical time series methods."

("I worked on a solar power prediction project. Using weather data like temperature, solar irradiance, humidity, and wind speed, I tested different prediction models. I compared simple approaches like persistence, statistical models like ARIMA, and machine learning models like Random Forest and Neural Networks. Random Forest performed the best with almost perfect accuracy. This shows my ability to handle data, build predictive models, and select the best one by comparing performance.")

Input Data
Synthetic dataset (365 days, full year with seasons + monsoon)
Features included:
1.Temperature (°C)
2.Solar Irradiance (W/m²)
3.Humidity (%)
4.Wind Speed (m/s)
5.Seasonal variations (summer, monsoon, winter)

Target: Solar Power Output (kW)
Models Tested

Persistence (Baseline) → predicts tomorrow = today.
Linear Regression (LR) → simple linear relation between inputs and output.
Random Forest (RF) → ensemble of decision trees.
Multi-Layer Perceptron (MLP / Neural Net) → deep learning style predictor.
ARIMA → time series forecasting model.
| Model            | MAE ↓ (kW) | RMSE ↓ (kW) |         R² ↑ | Notes                                      |
| ---------------- | ---------: | ----------: | -----------: | ------------------------------------------ |
| Persistence      |       8.33 |        13.2 |         0.84 | Good seasonal baseline                     |
| LinearRegression |       0.42 |        0.57 |       0.9997 | Excellent, almost perfect fit              |
| RandomForest     |  **0.016** |    **0.04** | **0.999998** | ⭐ Best performer, captures non-linearities |
| MLP (Neural Net) |       12.3 |        14.3 |         0.81 | Overfit / unstable                         |
| ARIMA            |       28.9 |        33.7 |       -0.004 | ❌ Poor, not suited here                    |

Interpretation

Best Model → 1.Random Forest (RF)
             Lowest errors, highest R² → almost perfect prediction.
              Works well because solar output is non-linear (temperature too high → panel overheats,    clouds reduce output suddenly).
2.Linear Regression also did well (data was generated with some linear assumptions).
3.MLP (neural net) struggled → probably needs more data & tuning.
4.ARIMA → not suitable since solar power is not purely time-based (depends on weather, season, environment).
5.Persistence → good baseline but not accurate.


Key Learnings:-

Solar panels are sensitive to weather:
Too high temperature (>35°C) → efficiency drops.
Cloudy/rainy → sudden dip in irradiance.
Seasonal shifts → need long dataset (365 days).
Machine Learning (especially Random Forests) can predict solar output much better than simple models.
Adding more real-world features (dust on panels, shading, tilt angle) could improve accuracy further.
