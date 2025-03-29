This project aims to predict the closing price of the NIFTY 50 index using historical market data and machine learning techniques. The primary goal is to forecast future closing prices based on historical trends, which could be useful for market analysis and decision-making.

Features
Data Extraction:
Retrieves historical market data (e.g., open, high, low, close, volume) from Yahoo Finance using libraries such as yfinance.

Data Preprocessing:
Utilizes pandas for data cleaning and manipulation. Key steps include:

Filtering for relevant features (e.g., closing prices).

Handling missing values and aligning data.

Scaling features with scikit-learn’s MinMaxScaler to normalize the input data for model training.

Modeling:
Implements a time-series forecasting model using LSTM neural networks, which are well-suited for capturing temporal dependencies in sequential data. The model is built using Keras (with TensorFlow as the backend).

Evaluation & Visualization:
Evaluates the predictive performance of the model using appropriate metrics and visualizes the results with matplotlib. Visualizations include plots of historical data, predicted prices versus actual prices, and performance metrics over time.

Methodology
Data Collection:
Historical data for the NIFTY 50 index is downloaded and stored in a structured format. The project fetches data starting from a specified date (e.g., 2012-01-01) up to the current date.

Feature Engineering:
In addition to raw closing prices, the project calculates derived features such as:

Close ratios over various time windows.

Trends and edit counts (if applicable) that may capture market volatility or sentiment shifts.

Model Training:
The dataset is split into training and testing subsets (typically 80/20 split). The training data is scaled, and an LSTM network is trained to learn the temporal patterns in the data.

Prediction & Backtesting:
The model forecasts future closing prices on the test set. A backtesting framework is implemented to simulate trading decisions based on the model’s predictions and evaluate the model’s practical performance.

Visualization & Analysis:
Results are plotted to compare predicted and actual values. The project includes interactive visualizations that help users understand the performance of the predictive model and market trends.
