# AIF Strategy: Combining PSP with counter-cyclical portfolio

***NOTE: CODE AVAILABLE UPON REQUEST***

## Introduction 
The idea of the strategy comes from the merger of the standard framework of Asset/Liability Management, i.e. combining a performance-seeking portfolio (PSP) with a liability-hedging portfolio (LHP), with the so-called ***Black-swan strategies***, whose goal is to generate large profits during market crashes.

---

### The Framework

1. Select the performance-seeking portfolio
2. Identify the counter-cyclical portfolio (CCP) respective to the PSP and define the asset allocation

---

## Data

* In this oversimplified application I use as PSP the Regularization strategy posted here.
* The data is collected for the period January 2005-Decmber 2020, while the backtesting period is January 2008-December 2020. 
* For the identification of the CCP, the key feature is the negative correlation, especially during market crashes.
As you can see below, the CCP identified shows a strong negative overall correlation of -0.54%, which becomes even better if we compute the dynamic correlation time series (rolling window of 36 months):

![rolling corr](https://user-images.githubusercontent.com/78954578/130289381-533eead0-dce4-4603-8b84-793549acc62e.png)

* In this case, the asset allocation is a simple naive 80-20. Nothing excludes to use more sophisticated allocations, from risk parity to dynamic asset allocation.

## Results

### Summary statistics:

![summary stats](https://user-images.githubusercontent.com/78954578/130289616-e1ca64f6-8423-4061-a0c2-eeea789580d4.png)

* 
* 
* 

![hist rets](https://user-images.githubusercontent.com/78954578/130289740-20385f9f-b29d-485a-bb05-bd8fd1905e71.png)

### Ex-post P&Ls comparison:

![P L](https://user-images.githubusercontent.com/78954578/130289858-3fd9b662-6ccf-49d7-a88d-c808ace020f5.png)

* Starting from a 1000$ capital, .

### Yearly performance:

![barplot](https://user-images.githubusercontent.com/78954578/130290191-08f9550c-1e18-40ef-9b81-93045cfc9b63.png)

* A desirable characteristic of an active fund is the "beat the market" ability: ideally, a manager asks for a higher management fee than a passive strategy to perform better than the market. In this case, if we define a new metric, the Hit Ratio, as the percentage number of periods a portfolio beats the benchmark, the strategy achieves a descrete performance of 61,5% (8 out of 13 years).


## Conclusions

* The strategy is able to deliver a greater Sharpe ratio, expected returns and an astonishing annualized alpha of 21.3% over the period 2008-2020
* 
