# Options Calculator 

Options calculator with Black-Scholes model and binomial model

## Project Statement:
As other financial products, an option should be completely understood what it is, why the price is changed overnight, and which information should be understood before trading one option. 

Options are contracts that give investors the right to buy or sell an asset at a strike price at or before the maturity day. With options, it is possible to profit whether the stock goes up, down or sideways in the future. Moreover, options can be used to cut the losses and protect the gains. However, if an investor does not completely understand option trading, this lack of knowledge may cause a huge loss. 

## 1. Black-Scholes Model

In order to know more information about a stock option, this options calculator with Black-Scholes Model, the first widely used model for option pricing, can provide the call/put option price, d1, d2, and Greek letters. It can assist investors in establishing an option trading strategy. 


Certain assumptions must be made due to this calculator is modeled by Black-Scholes model. 
* It works on European options that can only be exercised at expiration.
* No dividends are paid out during the option’s life.
* Stock markets are efficient. The movement of the markets cannot be predicted, and there is continuous trading
* There are no transaction and commissions costs in buying the option.
* The risk-free rate and volatility of the underlying are known and constant.
* The returns on the underlying are normally distributed.

#### Input variables:
* Underlying price (per share)
* Strike price of the option (per share)
* Time to maturity (years)
* Continuously compounding risk-free interest rate (%)
* Volatility (%)

#### Output Variables:
* d1: N(d2), the cumulative density function of normal distribution, is the risk-adjusted probability that the option will be exercised.
* d2: N(d1), the cumulative density function of normal distribution, is the probability of receiving the stock at expiration of the option.

* The Greek letters, including delta, gamma, vega, rho, and theta, represent the sensitivities of the option price to a single –unit change in the value of either a state variable or a parameter. 
  - The delta of an option is defined as the rate of change of the option price respected to the rate of the change of underlying asset price. 
  -	The gamma is defined as the rate of change of delta respected to the rate of change of underlying asset price.
  -	The vega of an option is defined as the rate of change of the option price respected to the volatility of the underlying asset. 
  -	The rho of an option is defined as the rate of the option price respected to the interest rate. 
  -	The theta of an option is defined as the rate of change of the option price respected to the passage of time.

## 2. Binomial Model
Binomial model is arguably the simplest techniques used for option pricing. In this calculator, the options price will be calculated by two binomial-tree methods,Cox-Ross-Rubinstein and Jarrow-Rudd (the equal-probability model). 

Each of the approaches has its advantages and disadvantages for pricing different types of options. However, they all involve a similar tree-step process.

* There are only two possible prices for the underlying asset on the next day.
* The two possible prices are the up-price and down-price
* No dividends are paid out during the option’s life.
* The risk-free rate is constant throughout the life of the option
* There are no transaction and commissions costs in buying the option.
* Investors are risk neutral

#### ** All trees are built from four parameters (u, d, p and q). 
- The parameters u and d are how much the underlying will go up or down in each discrete time. 
- The parameters p and q are the probabilities for the price to go up and down respectively. Moreover, assume p+q=1.


#### ** Note that the model assumes that the price of the equity underlying the option follows a random walk.


## Python Resources:

* Pandas: Pandas is a Python package for data analysis. In particular, it offers data structures and operations for manipulating numerical tables and time series. 

* Numpy: Numpy is a fundamental package to support for multi-dimensional arrays and matrices. It is not only used for scientific computing, but also for multi-dimensional container of generic data.

* Math: Math provides access to the mathematical functions, such as pi, log, exp, sqrt, and other mathematical functions.  

* Statistics: Statistics provides access to the statistics functions, such as norm_pdf, norm_cdf, mean, stdev, and other statistics functions.

* matplotlib.pyplot

* datetime
