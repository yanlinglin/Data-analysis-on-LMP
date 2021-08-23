# Data analysis on LMP
 A general data analysis on LMP
 
## The motivation for the project
Since the liberalization of the U.S. market, most U.S. electric markets adopt the locational marginal price (LMP) to set prices for energy purchases and sales. The power market is usually divided into the day-ahead (DA) market and real-time (RT) market. The resolution of the DA market is one hour. In the DA market before the operation day, Generation companies (GENCOs) and large consumers bid in the DA market and receive the LMP when ISO clears the market by running an economic dispatch problem. Then in the operation day, ISO will clear the RT market again and calculate the RT LMP. The cleared DA and RT LMP are used in the settlement phase, where consumers pay the LMP and GENCOs receive LMP.

True to its name, LMP is location-dependent. It is also influenced by demand, renewable energy generation, transmission congestion, prices of fuel, generator outage, etc. LMP is not only the energy price for transactions but also a critical index for the decision-making of the market participants. Therefore, accurate electricity forecasting is a key issue for both market participants and market operators in the wholesale electricity market. This report takes a look at the general trend of LMP and its correlation with other time-series data, such as load, temperature, and fuel mix. This works can serve as a data preprocessing for performing LMP forecasting using machine learning methods in the future.

##
In this report, we analyze data from PJM of three years (7/1/2018 00:00 to 5/31/2021 23:59). The data is available to the public. The collected data include:

Target:  
- DA LMP: https://dataminer2.pjm.com/feed/rt_da_monthly_lmps, node: 1(PJM RTO)  

We select the following accomapying data sets to assist our understanding of LMP:  
- DA_load: https://dataminer2.pjm.com/feed/hrl_load_metered, Region: RTO
- DA_wind: https://dataminer2.pjm.com/feed/wind_gen , area: RTO
- DA_temperature: https://dataminer2.pjm.com/feed/da_tempset 
- fuel_type: https://dataminer2.pjm.com/feed/gen_by_fuel
- outage: https://dataminer2.pjm.com/feed/gen_outages_by_type, region: PJM RTO

## Libraries used:

Pandas, Matplotlib, seaborn, datetime.

## Data source
In this report, we analyze data from PJM of three years (7/1/2018 00:00 to 5/31/2021 23:59). The collected data include:

Target:  
- DA LMP: https://dataminer2.pjm.com/feed/rt_da_monthly_lmps, node: 1(PJM RTO)  

We select the following accomapying data sets to assist our understanding of LMP:  
- DA_load: https://dataminer2.pjm.com/feed/hrl_load_metered, Region: RTO
- DA_wind: https://dataminer2.pjm.com/feed/wind_gen , area: RTO
- DA_temperature: https://dataminer2.pjm.com/feed/da_tempset 
- fuel_type: https://dataminer2.pjm.com/feed/gen_by_fuel
- outage: https://dataminer2.pjm.com/feed/gen_outages_by_type, region: PJM RTO

## The files in the repository 
The main code is stored in "LMP_analysis.ipynb". The data folder contains all the data used.

## A summary of the results of the analysis
We investigate the general trends of LMP; show the correlation of LMP with other time-series data, e.g. load, temperature, fuel mix; show that LMP exhibits autocorrelation. 


