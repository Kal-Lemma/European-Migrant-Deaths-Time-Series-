# European Migrant Deaths: Time Series
There is a serious humanitarian problem that needs to be clearly voiced and publicized to have any chance at an impactful solution. With Billions already being poured by the National and EU sectors into border control efforts, it is within the Public’s right to know the ‘intended’ and ‘unintended’ outcomes of such policy.
* These outcomes rely ‘extremely’ on accurate information in order for policymakers and social engagement on the issue to be properly motivated, honest, and factual! The lack of consistent accounting for Migrant deaths in the Mediterranean has contributed to the legitimization and neutralization of the humanitarian issue at hand.
* Not having ‘proper’ death accounting also diminishes likelihood of aiding those who may be particularly vulnerable groups; and without death confirmations, relatives and family members “are not only denied closure, but may also be unable to inherit or remarry.

## The Two Major Sources of Data for Border Deaths
* Both sourced from the news media, in which volunteering activists verify, categorize, and input the reports into the database.
* **Problem with DataSet:** News Media
Deaths are 'under-counted' due to how the media tends to report whatever catches attention: bigger story, bodies go unreported. Also may stop reporting deaths if it is always occurring in certain locations and continually being reported.
There is also possible 'over-counting' by the misidentification of ‘migrant’ bodies, much less occurrence.

## My DataSet for Time-Series
* The Amsterdam-based activist group, UNITED for Intercultural Action, has been collecting information about the deaths of Europe’s refugee-seekers since the early 1990s. The organization's volunteers “update the data annually, spending six months at a time verifying reports, categorizing deaths and entering them into the database”, according to The Guardian's story about the endeavor and its findings: “When the project began, they received physical clippings from a network of groups around Europe. Now, the data is collected from email submissions and Google Alerts in a number of languages.”

## Exploratory Data Analysis
* Only 10% of all irregular Migrants enter Europe by sea, though nearly 80% drowned in our recorded data.
![Screen Shot 2019-07-30 at 2.17.43 PM](https://github.com/klemma14/European-Migrant-Deaths-Time-Series-/blob/master/Visuals/Screen%20Shot%202019-07-30%20at%202.17.43%20PM.png)
* Low counts during the 90s can be attributed to the lack of many of the visa obligations and government policies that began to be highly enforced later that decade.
For the past two decades, Europe’s response to irregular migration by sea has taken many various forms. (Intended)

![Screen Shot 2019-08-31 at 2.02.37 PM](https://github.com/klemma14/European-Migrant-Deaths-Time-Series-/blob/master/Visuals/Screen%20Shot%202019-08-31%20at%202.02.37%20PM.png)
* When enforcement is increased, migrants resort to more dangerous routes to avoid detection, which leads to increased deaths. (Unintended)

## Trend over Time
![Screen Shot 2019-07-30 at 3.36.40 PM](https://github.com/klemma14/European-Migrant-Deaths-Time-Series-/blob/master/Visuals/Screen%20Shot%202019-07-30%20at%203.36.40%20PM.png)

## Time Series Prep and Modeling
* Tested out Partial and AutoCorrelation Functions, (PACF,ACF) which checks different past timelines relating to the present, to see which past day could be the best predictor of today.
* Utilized multiple different transformed series through SARIMA models, in which the Subtracted Rolling Mean Series performed best for my predictions. This Model works by combining both AutoRegressive and Moving-Average models, while integrating de-trending and accounting for seasonality in the non-stationary Time Series.
* Finished up by fitting my model with Gridsearch’s best found parameter choices for both the Non-Seasonal (p,d,q), and Seasonal (P,D,Q) components.
## Results
![Screen Shot 2019-07-30 at 4.13.26 PM](https://github.com/klemma14/European-Migrant-Deaths-Time-Series-/blob/master/Visuals/Screen%20Shot%202019-07-30%20at%204.13.26%20PM.png)
**Future Predictions 2018, 2019, 2020**
![Screen Shot 2019-07-31 at 4.22.49 PM](https://github.com/klemma14/European-Migrant-Deaths-Time-Series-/blob/master/Visuals/Screen%20Shot%202019-07-31%20at%204.22.49%20PM.png)
### Value in Migrant Death Data
“It is, however, imperative to have migrant death data that is as reliable as possible, for at least two reasons. First, when death occurs on such a massive scale, all actors involved, including States, NGOs and international humanitarian organizations, have a responsibility to investigate the causes of such tragedies in order to identify possible interventions. Second, missing migrants’ relatives have the right to know whether their loved ones have died in the attempt to reach the destination country, and if so where their remains are.”
[Fatal Journeys: Tracking Lives Lost during Migration](https://publications.iom.int/system/files/pdf/fataljourneys_countingtheuncounted.pdf#page=104)
