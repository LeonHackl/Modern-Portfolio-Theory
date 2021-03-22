# Modern Portfolio Theory

## Introduction
Modern Portfolio Theory (MPT) is a theory on how risk-averse investors can construct portfolios to maximize expected return 
based on a given level of market risk. Harry Markowitz pioneered this theory in his paper "Portfolio Selection" which was 
published in the Journal of Finance in 1952. He was later awarded a Nobel Prize for his work on MPT. In this project, we want to
use Markowitz' MPT for identification of optimal portfolios consisting of various crypto assets like Bitcoin, Ethereum or Cardano.
The individual portfolios are all computed using classic Mean-Variance-Optimization (MVO).

## Overview
For now, only Bitcoin (BTC), Ethereum (ETH), Cardano (ADA), Chainlink (LINK) and the Binance Smart-Chain Token (BNB) are included 
in this analysis. The main reason for not taking in more coins/tokens being that there is not yet enough data available as we want at 
least 3+ years of data for our calculations. More tokens like Polkadot or Ocean will be added in the future. 

We start off by comparing the distribution of the chosen assets with the standard normal distribution before computing the annual mean return
vector and the variance-covariance-matrix necessary for the MVO. After visualization of the efficient frontier and the comparison of 
minimum volatility and maximum sharpe-ratio portfolios, the Capital-Asset-Pricing-Model (CAPM) is used to find a better estimation for 
the expected returns (for more details, see the jupyter notebook). Furthermore, we try using an exponentially-weighted covariance matrix
to improve upon our results.

All computations regarding the MVO are done using the `PyPortfolioOpt` package.

## To-Do
- Implementation of Black-Litterman Allocation
