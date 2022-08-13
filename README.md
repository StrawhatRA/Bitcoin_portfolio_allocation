# **Bitcoin_portfolio_allocation**



## **Question: What is the ideal cryptocurrency portfolio allocation?**
<br>

[Link to Presentation Slide](https://docs.google.com/presentation/d/1NstwO41gBiJYkp_dUDChRg1CIiXgvBwwUQjsIbcKBOk/edit#slide=id.g10d75b15c0d_0_753)

<br>

## Summary
In this project, we analyzed the use of Bitcoin as a proxy for cryptocurrency asset class and how it performed within a portfolio strategy compared to a portfolio which included only equity, bond and other traditional asset classes. <br>

We also used efficient frontier to find the most efficient portfolio with Bitcoin as part of the mix. Our goal was to develop, forecast, and compare several 5-year portfolios that offer the greatest returns per unit of risk. We determined that the most efficient portfolio allocation is stocks (59%), bonds (18%), gold (10%), and crypto (14%). In forecasting this distribution, our ideal portfolio weighting has characteristic risk of σ = 1.51 and a forecasted total return of 212%.

<br>

## Introduction
Let’s face it. The current investment landscape has changed dramatically for younger investors across Canada. We have lived through an era of ultra low interest yields for over a decade that, despite having contributed to the momentum of the economy, still comes at a cost (mostly to general affordability, housing, and complicating our investment portfolio strategies). Meanwhile, we’ve seen the rise of alternative asset classes (cryptocurrency, private equity, hedge funds). We believe these changes offer an opportunity for young investors to potentially build savings in hopes of entering the housing market. 

We aim to explore the potential risks, returns, and general impact of including cryptocurrency assets as part of an investment portfolio. We will do this by modeling 4 standard portfolio weightings, as well as run a model that provides the ideal portfolio distributions.


To illustrate this, we’ve introduced Average Joe.

<br>

<p align="center" width="100%">
    <img width="100%" src="https://github.com/JakeKJShin/Project_1_Team_2/blob/ray_draft/readme%20Images/Average_Joe.PNG"> 
</p>

<br>

## **Approach**
In order to build our model portfolios, we must first understand the characteristics of our asset classes. Our fundamental asset categories are stocks, bonds, gold, and bitcoin, and so we created a representative basket of 11 ETFs (as well as the historical price of BTC). To determine the properties and relationships of these assets, our team ran several correlation analysis, summarized below.

<p align="center" width="100%">
    <img width="100%" src="https://github.com/JakeKJShin/Project_1_Team_2/blob/ray_draft/readme%20Images/heat_map2.png"> 
</p>

We can see here that Bitcoin best correlates to XLF, the energy sector ETF, with a value of X

<br>
The daily standard deviation of bitcoin is an obvious outlier with a value of X. We believe the increased volatility of bitcoin and the Dow Jones Transportation index is due to the major impacts of the initial crash of Covid-19 and its impact on the logistics industry. The below graph displays the standard deviation of  
<p align="center" width="100%">
    <img width="75%" src="https://github.com/JakeKJShin/Project_1_Team_2/blob/ray_draft/readme%20Images/std_dev.png"> 
</p>


<br>

## **Portfolio Analysis**

Based on popularized recommended allocations in modern portfolios (similar to the 60/40 structure typically advised by Investment Managers), we’ve chosen four portfolios and assigned crypto allocations as 0%, 5%, 10%, and 20%. The generic portfolio breakdowns are as follows:

<p align="center" width="100%">
    <img width="50%" src="https://github.com/JakeKJShin/Project_1_Team_2/blob/ray_draft/readme%20Images/pf_a.png"> 
</p>
<p align="center" width="100%">
    <img width="50%" src="https://github.com/JakeKJShin/Project_1_Team_2/blob/ray_draft/readme%20Images/pf_b.png"> 
</p>
<p align="center" width="100%">
    <img width="50%" src="https://github.com/JakeKJShin/Project_1_Team_2/blob/ray_draft/readme%20Images/pf_c.png"> 
</p>
<p align="center" width="100%">
    <img width="50%" src="https://github.com/JakeKJShin/Project_1_Team_2/blob/ray_draft/readme%20Images/pf_d.png"> 
</p>


<br>
<br>

Running each of these portfolios through a 5-year Monte Carlo analysis, we arrive at the following possible return ranges.
<p align="center" width="100%">
    <img width="75%" src="https://github.com/JakeKJShin/Project_1_Team_2/blob/ray_draft/readme%20Images/cum_return.png"> 
</p>
<p align="center" width="100%">
    <img width="75%" src="https://github.com/JakeKJShin/Project_1_Team_2/blob/ray_draft/readme%20Images/return_ranges.png"> 
</p>

However, what if our Average Joe wanted to allocate funds according to his own specific tolerance for risk? Or, alternatively, what is the most efficient weighting of a portfolio containing crypto regarding optimal risk and return metrics?

<br>

## **Enter: The Efficient Frontier!** 

The efficient frontier consists of investment portfolios that offer the highest expected return for a specific level of risk. Returns depend on the investment weighting of each portfolio, where it’s standard deviation is synonymous with risk (and a lower covariance between securities results in lower risk). By optimizing and plotting these portfolios, we arrive at the Efficient Frontier which plots the ideal portfolio weightings that achieves the best returns per unit or risk. Optimal portfolios that comprise the efficient frontier usually exhibit a higher degree of diversification.

By randomly generating 1000 portfolio weights, we can plot their most efficient returns per unit of risk for each portfolio.

<p align="center" width="100%">
    <img width="100%" src="https://github.com/JakeKJShin/Project_1_Team_2/blob/ray_draft/readme%20Images/ef.png"> 
</p>
We note the characteristics of two significant portfolios:

Lowest Volatility Portfolio Distribution = [{‘Volatility’ : 0.135}, {‘Sharpe’ : 0.277}, {‘Returns’ : 0.031}, {‘Stocks’ : 0.52}, {‘Bonds’ : 0.23}, {‘Gold’ : 0.19}, {‘Crypto’ : 0.05}]

Highest Sharpe Portfolio Distribution =  [{‘Volatility’ : 0.2}, {‘Sharpe’ : 1.05}, {‘Returns’ : 0.21}, {‘Stocks’ : 0.59}, {‘Bonds’ : 0.18}, {‘Gold’ : 0.10}, {‘Crypto’ : 0.14}]

<p align="center" width="100%">
    <img width="60%" src="https://github.com/JakeKJShin/Project_1_Team_2/blob/ray_draft/readme%20Images/lowest_volatility_portfolio.png"> 
</p>
<p align="center" width="100%">
    <img width="60%" src="https://github.com/JakeKJShin/Project_1_Team_2/blob/ray_draft/readme%20Images/high_sharpe_portfolio.png"> 
</p>

If we were to then apply each of these key portfolio distributions to our Monte Carlo analysis, we can arrive at the forecasted mean returns range.

<p align="center" width="100%">
    <img width="90%" src="https://github.com/JakeKJShin/Project_1_Team_2/blob/ray_draft/readme%20Images/all_portfolios_cum_return.png"> 
</p>


## **Conclusion**
The most efficient portfolio allocation for Average Joe represents a crypto allocation of 14%, with an anticipated mean return of 212% over 5 years, bringing his initial investment of $10,000 to $31,300. Sadly, still not enough for a down payment in Toronto! As a rule of thumb for all other investors, your typical portfolio allocation for cryptocurrency should be somewhere between 1%-15%, depending on your risk tolerance.

It should also be noted that crypto doesn’t correlate with typical assets, and therefore adds diversification to his savings portfolio. 

Although these potential returns could tempt investors to allocate more money to crypto, investors should always remember that past performance is no guarantee of future results. These results may be skewed to be toward Bitcoins growth and evolution into a mainstream asset; that is, these historical prices capture bitcoin’s earliest price movements from its initial stages of early adoption to being widely accepted as the planet's dominant crypto currency.
