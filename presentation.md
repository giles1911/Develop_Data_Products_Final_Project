<style type="text/css">

.reveal pre code {
  display: black; padding: 0.3em;
  font-size: 1em;
  
</style>


Diamond price prediction
========================================================
author: S.Giles
date: 23 | October |   2018
autosize: true
transition: rotate
transition-speed: slow

Overview
========================================================
The world diamond market is represented by diamond mining and trade in rough diamonds. The bulk of the world diamond mining is concentrated in nine countries, with their share in the global production in physical terms as high as 99%. The world’s largest producers of natural diamonds are Russia, the Democratic Republic of Congo (DRC) and Botswana, all together accounting over 60% of the global diamond production. [**here**] (https://github.com/giles1911/Develop_Data_Products_Final_Project)

The Shiny application it is building linear regression model using the famous data set `diamonds` and is predicting the market price based on quality and specifications.The application allows the user to pre-define:
- Carat
- Clarity
- Cut
- Color

Now we will create a plot and try to predict the price of diamonds in the market.

Data Analysis and General Information
========================================================

ussia ranks first in the world’s diamond production. ALROSA Group accounts for 93% of the total diamond production in the Russian Federation in physical terms, and it is the leader of the global diamond mining industry. Major mining companies are engaged in mining in the main diamond-producing countries, the exception being Zimbabwe and the DRC, where diamond deposits are developed by small companies and prospectors. The graph below represents the geography of the companies’ activities including exploration.
This data set contains the information about 54000 diamonds with 10 specifications:



```
     carat               cut        color        clarity     
 Min.   :0.2000   Fair     : 1610   D: 6775   SI1    :13065  
 1st Qu.:0.4000   Good     : 4906   E: 9797   VS2    :12258  
 Median :0.7000   Very Good:12082   F: 9542   SI2    : 9194  
 Mean   :0.7979   Premium  :13791   G:11292   VS1    : 8171  
 3rd Qu.:1.0400   Ideal    :21551   H: 8304   VVS2   : 5066  
 Max.   :5.0100                     I: 5422   VVS1   : 3655  
                                    J: 2808   (Other): 2531  
     depth           table           price             x         
 Min.   :43.00   Min.   :43.00   Min.   :  326   Min.   : 0.000  
 1st Qu.:61.00   1st Qu.:56.00   1st Qu.:  950   1st Qu.: 4.710  
 Median :61.80   Median :57.00   Median : 2401   Median : 5.700  
 Mean   :61.75   Mean   :57.46   Mean   : 3933   Mean   : 5.731  
 3rd Qu.:62.50   3rd Qu.:59.00   3rd Qu.: 5324   3rd Qu.: 6.540  
 Max.   :79.00   Max.   :95.00   Max.   :18823   Max.   :10.740  
                                                                 
       y                z         
 Min.   : 0.000   Min.   : 0.000  
 1st Qu.: 4.720   1st Qu.: 2.910  
 Median : 5.710   Median : 3.530  
 Mean   : 5.735   Mean   : 3.539  
 3rd Qu.: 6.540   3rd Qu.: 4.040  
 Max.   :58.900   Max.   :31.800  
                                  
```

Shiny files
========================================================

The application is build using Shiny package and the source code is in 2 files:
- `ui.R`
- `server.R`

Both files can be found here: [GitHub repo](https://github.com/giles1911/Develop_Data_Products_Final_Project)

Documentation
========================================================

The application is drawing plot of diamonds in the `diamonds` data set distributed by their size (carat) and price ($). The regression line is shown on the plot as well. 

By selecting specific features of the diamond (carat, cut, clarity, color) the user is able to sub select the data set and the regression is recalculated based only on the diamonds in the data set that share the same features. If no features are selected the regression model is using all diamonds in the data set.

Below the graph shows the price of Diamonds based on quality.
