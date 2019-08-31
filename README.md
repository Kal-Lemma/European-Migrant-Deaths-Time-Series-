# European Migrant Deaths: Time Series
There is a serious humanitarian problem that needs to be voiced and clearly shown to have any chance at an impactful solution to the issue. With the billions already being poured at the national and EU levels into border control efforts, it is within the Public’s right to know the ‘intended’ and ‘unintended’ outcomes of such policy.
* These outcomes rely ‘extremely’ on accurate information in order for society’s and policymakers’ engagement on the issue is to be properly motivated, honest, and factual! The lack of consistent accounting for Migrant deaths in the Mediteranean has contributed to the legitimization and neutralization of the humanitarian issue at hand.
* Not having ‘proper’ death accounting also diminishes chance of aiding those who may be particularly vulnerable groups, and without death confirmations, relatives and family members “are not only denied closure but may also be unable to inherit or remarry
## The Two Major Sources of data for border deaths
* Both sourced from the news media, in which then volunteering activists who verify, categorize, and input the reports death into the database.
* Problem with Data; News Media
Undercounting deaths due to how the media tends to report whatever catches attention, bigger story, bodies go unreported. Also may stop reporting deaths if it is always occurring in certain locations.
Possible overcounting by the misidentification of ‘migrant’ bodies.
## My DataSet for Time-Series
* The Amsterdam-based activist group UNITED for Intercultural Action has, since the early 1990s, been collecting information about the deaths of Europe’s refugee-seekers. The organization's volunteers “update the data annually, spending six months at a time verifying reports, categorizing deaths and entering them into the database”, according to The Guardian's story about the endeavor and its findings: “When the project began, they received physical clippings from a network of groups around Europe. Now, the data is collected from email submissions and Google Alerts in a number of languages.”
## Exploratory Data Analysis
* Only 10% of all irregular Migrants enter Europe by sea, though nearly 80% drowned in our recorded data.
![Screen Shot 2019-07-30 at 2.17.43 PM](https://github.com/klemma14/European-Migrant-Deaths-Time-Series-/blob/master/Visuals/Screen%20Shot%202019-07-30%20at%202.17.43%20PM.png)
Low counts during the 90s can be related to the lack of many of the many visa obligations and government policies that began to be highly enforced later in the decade.
For the past two decades, Europe’s response to irregular migration by sea has taken many various forms (intended).
![Screen Shot 2019-08-31 at 2.02.37 PM](https://github.com/klemma14/European-Migrant-Deaths-Time-Series-/blob/master/Visuals/Screen%20Shot%202019-08-31%20at%202.02.37%20PM.png)
* Increased enforcement, migrants resort to more  dangerous routes to avoid detection, which lead to increased deaths (unintended).
## Trend over Time
![Screen Shot 2019-07-30 at 3.36.40 PM](https://github.com/klemma14/European-Migrant-Deaths-Time-Series-/blob/master/Visuals/Screen%20Shot%202019-07-30%20at%203.36.40%20PM.png)
## Time Series Prep and Modeling
* Using Partial and AutoCorrelation Function (PACF,ACF) which is checking different past timelines related to the present, to see which past day could be the best predictor of today.
* Using SARIMA model to multiple different transformed series, in which Subtracted Rolling Mean series performed best for my predictions. This Model works by Combining both AutoRegressive and Moving-Average models, with Integrated detrending, while accounting for Seasonality due to our non-stationary Time Series.
* Finally, fitting my model with Gridsearch’s best found parameter choices for both the Non-Seasonal (p,d,q), and Seasonal (P,D,Q) components.
## Results
![Screen Shot 2019-07-30 at 4.13.26 PM](https://github.com/klemma14/European-Migrant-Deaths-Time-Series-/blob/master/Visuals/Screen%20Shot%202019-07-30%20at%204.13.26%20PM.png)
### Future Predictions 2018, 2019, 2020
![Screen Shot 2019-07-31 at 4.22.49 PM](https://github.com/klemma14/European-Migrant-Deaths-Time-Series-/blob/master/Visuals/Screen%20Shot%202019-07-31%20at%204.22.49%20PM.png)
