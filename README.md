# Trus.mq5 ReadMe File

## Description

This code is an example of a trading indicator called Trus. Trus is designed to identify trend insights in the currency market and make trading decisions based on certain conditions. It uses Bollinger Bands, trend intensity calculations, and analysis of economic and political news to determine when to buy or sell.

## How it Works

The Trus indicator works as follows:

1. Initialization: The indicator initializes by setting the necessary parameters such as the period for smoothing calculations, the deviation for Bollinger Bands, and the impact factor of economic and political news.

2. Indicator Buffers: Two indicator buffers are created for storing the trend information. The first buffer (ExtMapBuffer1) is used for a bullish trend, and the second buffer (ExtMapBuffer2) is used for a bearish trend.

3. Trade Class Initialization: The CTrade class is initialized to perform trading operations.

4. Main Loop: The main loop iterates over the historical data, starting from the period specified. Inside the loop, the following actions are performed:

   - Bollinger Bands Calculation: The upper and lower Bollinger Bands are calculated using the iBands() function.
   
   - Trend Intensity Calculation: The trend intensity is calculated by taking the absolute difference between the closing prices of the current and previous periods, divided by the period length.
   
   - News Analysis: The economic and political news at the current time is analyzed using the AnalyzeNews() function. The impact factor is taken into account to determine if there is an anomaly.
   
   - Trend Identification: Based on the Bollinger Bands, trend intensity, and news analysis, the indicator determines the trend direction. If the closing price is above the upper band and there is no anomaly, a bullish trend is identified. If the closing price is below the lower band and there is no anomaly, a bearish trend is identified. The corresponding values are stored in the indicator buffers.
   
   - Trend Prediction: The trend intensity is compared to certain thresholds (0.5 for buy and 0.3 for sell) to predict the duration and intensity of the trend. If the trend intensity is above 0.5, a buy order is placed. If the trend intensity is below 0.3, a sell order is placed.

5. Event Handling: The OnTick() function is called on each tick event. However, no specific actions are performed in this example.

6. News Analysis: The AnalyzeNews() function is called to analyze economic and political news. In this example, the function always returns false, indicating that no anomaly is found.

## Product Description

Trus is a powerful trading indicator that unveils trend insights in the currency market. It combines the analysis of Bollinger Bands, trend intensity, and economic/political news to identify profitable trading opportunities.

Key Features:
- Bollinger Bands: Trus utilizes Bollinger Bands to determine the upper and lower price levels for trend identification.
- Trend Intensity Calculation: The indicator calculates the intensity of the trend based on historical price data, allowing for better trend prediction.
- Economic and Political News Analysis: Trus analyzes economic and political news to identify anomalies that may affect the market conditions.
- Buy and Sell Orders: The indicator automatically places buy and sell orders based on the predicted trend duration and intensity.

Please note that ForexRobotEasy is not the official developer of this product. We only provide sample code that demonstrates how this indicator can work based on the product description. For detailed reviews and trading results of this product, please visit [Forex Robot Easy](https://forexroboteasy.com/forex-robot-review/trus-forex-software-unveiling-trend-insights-in-currency-market/). To find the official developer of this product, please refer to MQL5.
