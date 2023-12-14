# Oscillator Predictor MT5

This code is a sample implementation of the Oscillator Predictor indicator for MetaTrader 5 platform. It predicts future price movements based on the current oscillator value.

## Global Variables

- `overboughtLevel`: The threshold value for the oscillator to be considered overbought. Default value is 80.0.
- `oversoldLevel`: The threshold value for the oscillator to be considered oversold. Default value is 20.0.
- `predictionPeriod`: The number of periods to predict into the future. Default value is 1.

## OnInit function

In the `OnInit` function, the initial values for global variables are set. The default values for `overboughtLevel`, `oversoldLevel`, and `predictionPeriod` are assigned.

## OnCalculate function

The `OnCalculate` function is called on each new tick or bar to calculate the prediction bands. It takes the necessary data as input parameters, such as time, open, high, low, close prices, tick volume, volume, and spread.

The function iterates over the bars from `prev_calculated` to `rates_total` and calculates the oscillator value by subtracting the previous close from the current close. Based on the oscillator value, the prediction bands are calculated as follows:
- If the oscillator value is greater than the overbought level, the prediction band is set to the current close plus the difference between the current close and the previous close, multiplied by the prediction period.
- If the oscillator value is less than the oversold level, the prediction band is set to the current close minus the difference between the previous close and the current close, multiplied by the prediction period.
- Otherwise, the prediction band is set to EMPTY_VALUE.

## OnDeinit function

The `OnDeinit` function is called when the indicator is removed or the chart is closed. It can be used to clean up any resources used by the indicator.

## Other necessary functions

This code only includes the calculation of the prediction bands. Other necessary functions for entering and exiting trades are not included in this code. These functions need to be implemented separately according to the trading strategy.

Please note that Forex Robot Easy is not the official developer of this product. This code is provided as a sample implementation that can work as described in the product. To find the official developer of this product, please refer to the MQL5 website.

For detailed reviews and trading results of this product, please visit [Forex Robot Easy - Oscillator Predictor MT5](https://forexroboteasy.com/forex-robot-review/review-oscillator-predictor-mt5-a-unique-forex-software-for-professional-traders/).
