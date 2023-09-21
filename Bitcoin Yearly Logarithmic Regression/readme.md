# Bitcoin Yearly Logarithmic Regression

## Model Overview
This is my Bitcoin logarithmic regression model(s) using Bitcoin's yearly low, high and open prices, which could be used to predict future yearly lows(blue), highs(red) and open(black) prices. **Please note that this model is for informational purposes only and does not constitute financial advice. Remember, All models are wrong, some are useful.**

I also performed a three-point fit to 2013/2017/2021 bull run highs (peaks): dotted red line. This provides a general idea of what the 2025 peak might be.
[2025 is an assumption based on the 4 year Bitcoin cycle, which fundamentally aligns with Bitcoin halvings that occur approximately every 4 years] [Halvings have an autocorrelation to the peaks with ~1 year lag]

- **Bitcoin Yearly Low Model:** $y = e^{0.7501 + 3.6093 ln(x - 2011)}$
- **Bitcoin Yearly High Model:** $y = e^{1.0838 + 3.6939 ln(x - 2011)}$
- **Bitcoin Yearly Open Model:** $y = e^{3.3384 + 3.0808 ln(x - 2011)}$
- **Bitcoin Cycle Peak Model:** $y = e^{5.3967 + 2.5004 ln(x - 2011)}$

where x = Year, y = price in USD

## Model Construction

### Data Source and Logarithmic Transformation
I used Tradingview's BTCUSD yearly index. I applied a natural log transform since it is a multiplicative series. This linearizes the data, making it more suitable for the model. Then, I applied the logarithmic transform, which had the highest R-squared score and correlation metrics, making it the best fit among the tested models.

### Visualization
I ploted it on on Desmos.com by inversing the natural log transform I did e^x.
For the plot, I shifted the model's origin point over 2011, corresponding to the years of the data, making the model easier to visualize.

### Model Validity
I tested the model up until 2040, and it appears to start breaking down. When comparing the peak model to the high model, residuals are decreasing, as are the residuals between the open model and the high model. However, when comparing the low model to the open model, residuals are increasing. Therefore, it will likely be necessary to refit the model as more data points become available.

