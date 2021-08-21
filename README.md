# AIF Strategy: Combining PSP with counter-cyclical portfolio

***NOTE: CODE AVAILABLE UPON REQUEST***

## Introduction 
The idea of the strategy comes from the merger of the standard framework of Asset/Liability Management, i.e. combining a performance-seeking portfolio (PSP) with a liability-hedging portfolio (LHP), with the so-called **Black-swan strategies** whose goal is to generate large profits during market crashes.

---

### The Framework

1. Select the performance-seeking portfolio
2. Identify the counter-cyclical portfolio (CCP) respective to the PSP
3. Define the asset allocation policy

---

## Data

* In this oversimplified application I use as PSP the Regularization strategy posted <b>[here](https://github.com/dpiloni/UCITS-Strategy-Regularization-Methods-in-US-Equity-Market)</b>.
* The data is collected for the period January 2005-Decmber 2020, while the backtesting period is January 2008-December 2020. 
* For the identification of the CCP, the key feature is the negative correlation, especially during market crashes.
The selected CCP shows a strong negative overall correlation of -0.54%, which becomes even better if we compute the dynamic correlation time series (rolling window of 36 months), as can be seen below:

![rolling corr](https://user-images.githubusercontent.com/78954578/130289381-533eead0-dce4-4603-8b84-793549acc62e.png)

* In this case, the asset allocation is a simple naive 80-20. Nothing excludes to use more sophisticated allocations, from risk parity to dynamic asset allocation.

## Results

### Summary statistics:

![summary stats](https://user-images.githubusercontent.com/78954578/130289616-e1ca64f6-8423-4061-a0c2-eeea789580d4.png)

* The strategy is able to achieve a higher perfrormance than the PSP and the market, both in terms of risk-adjusted one (Sharpe ratio) and extra-performance, **with an annualized alpha of 21.3%**
* Benefits come also in form of *left tail risk reduction*: lower maximum drawdown, VaR and CVaR than the PSP and the market
* By visualizing historical returns' *pdf*, it's possible to appreciate the combination of high variance, positive skewness and excess of kurtosis:

![hist rets](https://user-images.githubusercontent.com/78954578/130289740-20385f9f-b29d-485a-bb05-bd8fd1905e71.png)

### Ex-post P&Ls comparison:

![P L](https://user-images.githubusercontent.com/78954578/130289858-3fd9b662-6ccf-49d7-a88d-c808ace020f5.png)

* Starting from a 1.000$ capital, the cumulative profits of the strategy over 13 years (2008-2020) would have reached more than 21.600$, not so far from doubling PSP's final wealth of 12.800$.

### Yearly performance:

![barplot](https://user-images.githubusercontent.com/78954578/130290191-08f9550c-1e18-40ef-9b81-93045cfc9b63.png)

* From the barplot we can appreciate how the framework works as expected: the strategy "sacrifices" a portion of total return during bullish phases, and is able to hedge better during bad times.
* By defining the **Hit Ratio** as the fraction of periods in which a portfolio beated the benchmark, the strategy is able to achieve a perfect score of 100%.
* Over 13 years considered, only during the subprime crisis the strategy highlights a negative return, still better than the PSP and the stock market.


## Conclusions

* The strategy is able to deliver a greater Sharpe ratio and expected returns than the market and the PSP, with an astonishing annualized alpha of 21.3% over the period 2008-2020.
* This is just an example of a broader portfolio management framework which could be applied in asset management industry: alternatives from the PSP selection to asset allocation policy are almost infinite.
