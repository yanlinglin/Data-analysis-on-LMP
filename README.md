# Data analysis on LMP
 A general data analysis on LMP
 
## The motivation for the project
Since the liberalization of the U.S. market, most U.S. electric markets adopt the locational marginal price (LMP) to set prices for energy purchases and sales. The power market is usually divided into the day-ahead (DA) market and real-time (RT) market. The resolution of the DA market is one hour. In the DA market before the operation day, Generation companies (GENCOs) and large consumers bid in the DA market and receive the LMP when ISO clears the market by running an economic dispatch problem. Then in the operation day, ISO will clear the RT market again and calculate the RT LMP. The cleared DA and RT LMP are used in the settlement phase, where consumers pay the LMP and GENCOs receive LMP.

True to its name, LMP is location-dependent. It is also influenced by demand, renewable energy generation, transmission congestion, prices of fuel, generator outage, etc. LMP is not only the energy price for transactions but also a critical index for the decision-making of the market participants. Therefore, accurate electricity forecasting is a key issue for both market participants and market operators in the wholesale electricity market. This report takes a look at the general trend of LMP and its correlation with other time-series data, such as load, temperature, and fuel mix. This works can serve as a data preprocessing for performing LMP forecasting using machine learning methods in the future.

## Libraries used:

Pandas, Matplotlib, seaborn, datetime.

## The files in the repository 
The main code is stored in "LMP_analysis.ipynb". The data folder contains all the data used.

## A summary of the results of the analysis
We investigate the general trends of LMP; show the correlation of LMP with other time-series data, e.g. load, temperature, fuel mix; show that LMP exhibits autocorrelation. 

