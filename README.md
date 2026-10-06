⚡ BijliSaarthi – A Personalized Household Electricity Saving Assistant

Overview
BijliSaarthi is a data-driven household electricity management application designed to help users understand and manage their electricity consumption.
The project uses Machine Learning and Deep Learning techniques to predict next-hour household electricity consumption and converts the prediction into useful information such as estimated billing, budget comparison, and electricity-saving suggestions.

🎯 Objectives
- Predict the next-hour household electricity consumption.
- Identify daily and weekly electricity usage patterns.
- Compare different forecasting models.
- Estimate billing-period electricity usage and indicative electricity bills.
- Help users understand whether their estimated bill is within their budget.
- Provide practical electricity-saving suggestions.
  
🤖 Models Used
1. Persistence Model
A simple baseline that assumes:
Next-hour consumption ≈ current consumption

2. Multiple Linear Regression (MLR)
MLR uses features such as:
- Current consumption
- 24-hour lag
- 168-hour lag
- Cyclical time features
3. LSTM
Long Short-Term Memory (LSTM) is used to learn sequential patterns from a 24-hour consumption sequence and predict the next hour.
4. Hybrid Model
The project combines MLR and LSTM predictions:
Hybrid Prediction = 0.62 × MLR Prediction + 0.38 × LSTM Prediction

The weights were selected using validation data.
📊 Model Evaluation
The models are evaluated using:
- MAE – Mean Absolute Error
- MSE – Mean Squared Error
- RMSE – Root Mean Squared Error
- R² – Coefficient of Determination
Reported results:
Model	MAE	MSE	RMSE	R²
Persistence	0.136321	0.083738	0.289376	0.575166
MLR	0.138836	0.068374	0.261484	0.653115
LSTM	0.155680	0.081905	0.286191	0.687931
Hybrid	0.175677	0.094917	0.308086	0.638345


Important: No single model performs best on every metric. MLR has the lowest MSE and RMSE, while LSTM has the highest R².
🏠 Application
The project includes a Streamlit-based application where users can provide recent electricity/billing information.
The application can:
1. Accept electricity meter/bill information.
2. Use OCR-assisted bill information extraction where applicable.
3. Allow users to confirm extracted values.
4. Estimate electricity consumption.
5. Estimate an indicative bill.
6. Compare the estimate with the user's budget.
7. Provide electricity-saving suggestions.
Note: Billing and savings values are estimates and should not be treated as official electricity bills.

🛠️ Technologies Used
- Python
- Pandas
- NumPy
- Scikit-learn
- TensorFlow / Keras
- Streamlit
- PIL / Pillow
- OCR
- Data visualization libraries
🔬 Research Contribution
The main contribution of BijliSaarthi is not only forecasting electricity consumption, but connecting forecasting with billing, budgeting, and practical electricity-saving guidance in one consumer-oriented workflow.
⚠️ Limitations
- Predictions depend on the quality and availability of electricity consumption data.
- OCR extraction may require user confirmation.
- Billing calculations are indicative estimates.
- The hybrid model does not outperform every individual model on every metric.
- Household behaviour and unexpected usage changes can affect predictions.
🚀 Future Scope
Future improvements can include:
- More household-level data.
- Appliance-level consumption analysis.
- Real-time smart-meter integration.
- More advanced forecasting models.
- Transformer-based time-series models.
- More personalized recommendations.
- Improved bill and tariff handling.

👩‍💻 Author
Sanchita Navnath Pohkar
TY B.Sc. Data Science & Analytics
R. A. Podar College of Commerce & Economics, Mumbai
