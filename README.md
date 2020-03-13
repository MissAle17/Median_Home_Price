# Median_Home_Price
Visualizations to describe the median home prices by metro area in the US. 

## The Data

Home prices have been a hot-button issue in terms of the greater health of the US economy for several decades.  Following median home prices, home builds, home purchases, home loan interest rates, is talked about reguarly by all sorts of market analysts.  

Rises prices of construction, in labor an materials, are chasing more and more people out of participating in this market.  With the wealth of data available we can do our own analysis and see where the most affordable US metropolitan areas are, should one be interested in lowering costs.  The project here was created to participate on [Kaggle](https://www.kaggle.com/paultimothymooney/zillow-house-price-data).

__Acknowledgements__
The data was downloaded from [Zillow Research](https://www.zillow.com/research/data/). Dataset license described at [Zillow](https://www.zillow.com/research/data/).

## The Approach

So when working with a relatively simple ask, like looking at trends in Home Prices, the approach to cleaning and reviewing the data is the major decision of the project.  In this case, the data was realatively clean, but there were a number of null values that needed to be dealt with.  In the case of NANs in the MSA column, I made a bold decision.  I removed those lines from my dataframe completely resulting in a loss of 22.6% of the data.  This was a conscious decision I made with my background knowledge of real estate.  There exists in the US a large amount of unincorporated land.  This includes everything from small plots in central Florida that are between farms to large swaths in the mid-west that are either part of parks or generally empty fields.  Thought the data loss was large, I was confortable given the ask, home prices in MSAs as these NANs likely weren't part of one.  One thought for future work would be to add these back in to see what affect they have on the prices.

I decded to work on the averages of the median prices, when aggregating everything togeter.  It's a little confusing to talk about the mean meadian home prices, however I still think it's the right choice. My first two visuals show the 10 most expensive MSAs, on average, over the last 10 years.  The first is a simple plot showing each MSA, the second is weighted by SizeRank changing the size of the plot point.
![Most Expensive MSAs](https://github.com/MissAle17/Median_Home_Price/tree/master/images/most%20exp.png "Most Expensive MSAs")
![Weighted Most Expensive MSAs](https://github.com/MissAle17/Median_Home_Price/tree/master/images/most%20exp%20w.png "Weighted Most Expensive MSAs")


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


