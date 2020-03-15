# Median_Home_Price
Visualizations to describe the median home prices by metro area in the US. 

## The Data

Home prices have been a hot-button issue in terms of the greater health of the US economy for several decades.  Following median home prices, home builds, home purchases, home loan interest rates, is talked about regularly by all sorts of market analysts.  

Rises prices of construction, in labor an materials, are chasing more and more people out of participating in this market.  With the wealth of data available we can do our own analysis and see where the most affordable US metropolitan areas are, should one be interested in lowering costs.  The project here was created to participate on [Kaggle](https://www.kaggle.com/paultimothymooney/zillow-house-price-data).

__Acknowledgements__
The data was downloaded from [Zillow Research](https://www.zillow.com/research/data/). Dataset license described at [Zillow](https://www.zillow.com/research/data/).

## The Approach

So when working with a relatively simple ask, like looking at trends in Home Prices, the approach to cleaning and reviewing the data is the major decision of the project. In this case, the data was relatively clean, but there were a number of null values that needed to be dealt with. In the case of NANs in the MSA column, I made a bold decision. I removed those lines from my dataframe completely resulting in a loss of 22.6% of the data. This was a conscious decision I made with my background knowledge of real estate. There exists in the US a large amount of unincorporated land. This includes everything from small plots in central Florida that are between farms to large swaths in the mid-west that are either part of parks or generally empty fields. Thought the data loss was large, I was comfortable given the ask, home prices in MSAs as these NANs likely weren't part of one. One thought for future work would be to add these back in to see what affect they have on the prices.

I decided to work on the averages of the median prices, when aggregating everything together. It's a little confusing to talk about the mean median home prices, however I still think it's the right choice. My first two visuals show the 10 most expensive MSAs, on average, over the last 10 years. The first is a simple plot showing each MSA, the second is weighted by SizeRank changing the size of the plot point.

![Most Expensive MSAs](https://github.com/MissAle17/Median_Home_Price/blob/master/images/most%20exp.png)

![Weighted Most Expensive MSAs](https://github.com/MissAle17/Median_Home_Price/blob/master/images/most%20exp%20w.png)

This dataset is not that surprising. The states that each of these MSAs are located in make sense.
⋅⋅* 5 in CA
⋅⋅* 3 in HI
⋅⋅* 1 in MA (Martha's vineyard)
⋅⋅* 1 in FL (Jupiter island)

I was surprised that this does not include New York City, but the home prices in the whole MSA are included. The NYC MSA also includes Newark, where home prices are considerably less than Manhattan.

As a former New Yorker, I wanted to see a little more about what the changes of the various MSAs looked like over time.  I added a dist plot for some of the MSAs in New York as well, including NYC.  I wanted to see if the dispersion in home price was different across such an economically diverse state.  

![NYS over time](https://github.com/MissAle17/Median_Home_Price/blob/master/images/NYS%20prices.png)


![NYS Displot](https://github.com/MissAle17/Median_Home_Price/blob/master/images/NYS%20dist.png)

Apparently, New York city is really expensive.  In both plots you can see that the prices of homes in NYC are much higher than some of the other larger MSAs in New York State.  

What about another state?  Are larger citites more spread out than the more secondary msa's in the state?

By way of contrast, I took my current state of residence, CO, and performed the same analysis.

![CO over time](https://github.com/MissAle17/Median_Home_Price/blob/master/images/CO%20prices.png)


![CO Displot](https://github.com/MissAle17/Median_Home_Price/blob/master/images/CO%20dist.png)


CO is very different in NY in this case. It does look like the Denver MSA is a more spread out than the other MSA's in CO, however, New York City is likely an outlier, since it is one of the biggest cities (and therefore metropolitan areas) in the world.

Dissecting the information in these plots, one must remember what you are looking at. These plots are average home prices by metropolitan area over time. So with the distplots, we're looking at the dispersion of the mean for each MSA by month over roughly ten years.

What about state by state averages side by side? The beginning of the data set is very near to the financial crisis, but included in the time frame is the 'recovery'. Roughly five years after the crisis the real estate markets recovered and in some places boomed.

![States over time](https://github.com/MissAle17/Median_Home_Price/blob/master/images/states%20prices.png)

Take careful note of the y axes - they've been calibrated to be the same. The top plot includes CA (That includes the San Jose MSA which is not only one of the highest median home prices but also one of the fastest growing). You can see the jump in CA toward the end of 2012. The same time frame saw a jump in median home prices in many states, this is roughly 5 years after the Financial Crisis and accepted as the period of recover.

## If I Had More Time..

I would take income data as well and contrast the Area Median Income (AMI) with the Average Median Home Price to determine the true 'expensiveness' of a metro politan area. Unfortunately the AMI data is difficult to find when you are not an institution subscribing to expensive dta sources. To move forward, either city by city income data or per capita (instead of household) data could be used to approximate AMI. Additionally, I could reassess the data and include the NANs in the state by state analysis as they are part of the state though not necessarily part of an MSA


## Process Summary

__1__ Import necessary libraries; Pandas, Numpy, Matplot, and Searborn

__2__ Load in the data from csv file into Pandas

__3__ Clean the data and explore basic statistics

__4__ Address NAN values

__5__ Calculating averages for median prices

__6__ Collapse data into 10 year Averages by MSA

__7__ Create the first plot of the series by graphing the most expensive MSAs

__8__ Create the second plot by weighting the most expensive MSAs by the size rank

__9__ Return to full, cleaned dataset in order to create subset for viewing NY over time

__10__ Plotting the median home price by MSA over time for NY

__11__ Plotting the distplot of home prices in NY for the 3 most expensive MSAs in NY

__12__ Repeating the NY process with another state, CO

__13__ Return again to full, cleaned sataset to plot the average prices by state over time

__14__ Explaining next steps

__15__ Process summary


