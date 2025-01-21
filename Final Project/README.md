# Stock Price Prediction and Trading Signal Generation  

This project integrates machine learning, financial data analysis, and sentiment analysis to predict stock prices and generate profitable trading signals. It uses Tesla stock data (2020–2024), macroeconomic indicators, and Elon Musk's tweets for sentiment-based strategies.

## Features  

### Data Sources  
- **Stock Data:** Tesla and competitors (BMW, NIO, BYD) via `yfinance`.  
- **Macroeconomic Indicators:** Fama-French factors, ADS Index, and FRED economic data.  
- **Sentiment Analysis:** Elon Musk’s tweets processed using sentiment scoring.

### Workflow  
1. **Sentiment Analysis**  
   - Extract Elon Musk's tweets using a preprocessed sentiment CSV (`sentiment_scores.csv`).  
   - Integrate these scores into feature engineering.  

2. **Feature Engineering**  
   - Technical indicators: SMA, EMA, RSI, MACD, Bollinger Bands, and ATR.  
   - Macroeconomic factors: GDP, unemployment, bond yields, oil prices, and more.  
   - Add sentiment-based features for modeling.

3. **Predictive Modeling**  
   - Train models: Ridge, LASSO, Random Forest, Gradient Boosting, XGBoost, LSTM, and Kalman filters.  
   - Evaluate models with RMSE and R² metrics.  

4. **Trading Signal Generation**  
   - Backtest trading strategies using signals from SMA Crossover, Momentum, Bollinger Bands, and sentiment-based approaches.  

5. **Performance Evaluation**  
   - Analyze cumulative returns and identify the best-performing models and strategies.  

## Results  
- Ridge regression and tree-based models achieved high predictive accuracy (R² > 0.98).  
- Sentiment-based strategies improved trading signal accuracy.  
- Backtesting demonstrated significant cumulative returns.  

## Files in This Repository  

1. **`Final_Project.ipynb`**  
   - Main notebook for the project.  
   - Includes data extraction, feature engineering, modeling, and backtesting.  

2. **`FF_Research_Data_5_Factors_daily.csv`**  
   - Fama-French 5-factor model dataset.  

3. **`ADS_Index_Most_Current_Vintage.xlsx`**  
   - ADS Index for macroeconomic activity tracking.  

4. **`sentiment_scores.csv`**  
   - Preprocessed sentiment analysis data for Elon Musk's tweets.  

5. **`lithium_index_data.csv`**  
   - Lithium market data used in feature engineering.  

## Usage  

### Prerequisites  
- Install Python 3.8+ and required libraries:  
  ```bash
  pip install -r requirements.txt
  ```  
- **Note:** If a `requirements.txt` file is missing, manually install the libraries mentioned in the imports section of `Final_Project.ipynb`.  

### Steps to Run  

1. **Data Preprocessing**  
   - Ensure all datasets (`FF_Research_Data_5_Factors_daily.csv`, `ADS_Index_Most_Current_Vintage.xlsx`, etc.) are in the project directory.  

2. **Sentiment Analysis**  
   - Use `sentiment_scores.csv` as input for Elon Musk's sentiment data.  
   - If you need to recreate this, process tweets using Python libraries like `TextBlob` or `VADER`.  

3. **Feature Engineering and Modeling**  
   - Run `Final_Project.ipynb` to execute all steps, from data extraction and feature engineering to modeling and backtesting.  

4. **Backtesting Trading Strategies**  
   - Use the trading signal generation logic in the notebook to evaluate performance.  

### Libraries Required  
- `pandas`, `numpy`, `matplotlib`, `seaborn`  
- `yfinance`, `scipy`, `sklearn`, `xgboost`, `tensorflow`  
- `fredapi` (for FRED data extraction)  

## Future Enhancements  
- Add a script for dynamic data updates and sentiment analysis.  
- Automate model selection and hyperparameter tuning.  
- Expand the scope to other stocks and economic indicators.  
