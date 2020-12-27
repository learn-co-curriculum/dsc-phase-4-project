# Project Four: Zillow Home Value Analysis

[Presentation Folder](https://drive.google.com/drive/folders/1tdyW9p7PeGVQl0mVuZsnQAp-svj1YHFj?usp=sharing)

[Blog Post](https://solerjaklyn.medium.com/zillow-home-value-analysis-d1afece85fcc)

[Connect with me on LinkedIn](https://www.linkedin.com/in/jaklyn-soler-6a298965/)


### Data Used

The data used was provided by Zillow, census.gov, and towncharts.com


### Building a Strategy

The assumptions that I made for this were that that investment company had plenty of capital to work with, that they were looking for a long term strategy rather than short term (perhaps even the ability to use outside funding by REIT), and that they wanted to make significant profits. I decided that their best strategy would be buying foreclosed or probate properties, rehabilitating them and renting them to tenants.

Tenant rent is calculated by being .8% to 1.1% of the total property value. By having a more competitive rental price, property owners can be more selective in their tenant evaluation since it will attract more interested renters. In light of this strategy, I selected the monthly rental amount of .9%. This means that in a 12 month period, the tenant would pay 10.8% of the property value. Not accounting for property maintenance and vacancy, every property would pay for its initial amount in about nine years and four months. The alternative strategy, rehabilitating and selling, or ‘flipping’, would result in a one-time smaller payoff, which would be less desirable than renting to tenants. Additionally, I wanted the zipcodes in close proximity to reduce the costs associated with managing multiple properties in different areas.

### Narrowing the Dataset

I cut out all of the data before 2012 as it was heavily affected by the housing crisis. Next, it was time to narrow down areas geographically. The strategy proposed would be affected by the number of foreclosure and probate properties, the ratio of rental properties that were available for rent there, and the number of people living there.
I decided that New York would be the best state due to the large number of baby boomers living there and information from census.gov confirmed this by showing that the northeast had the lowest rental vacancy rate.

### United States Rental Vacancy Rate

From there I narrowed the zipcodes by choosing property values that were between $500,000 and $700,000. I decided that this would be a good strategy so that the investment company can diversify by having several properties rather than one large property. If uncertain times were to fall on a tenant or there was property destruction, this would allow for the investment company’s monthly revenue from tenants to not be as affected.

### Modeling + Results

I had 13 zipcodes to model. I used a moving window function to remove trend and a rolling mean equation to remove seasonality as needed. Then I modeled with SARIMAX and forecasted a confidence interval. The average ROI by percentage was taken so each zip code could be compared. This took a while! Finally, the zip codes with the highest return were determined!

### Best Zipcode

The zipcode with the highest ROI was 11427 which had a forecasted return of 1438%.

![](NOTEBOOKS/data/forecast)

### Future Work

I used a range of 0 to 3 on the p, d, and q parameters for SARIMAX modeling. This range could be expanded to find better models. For the real estate investment company, they would need to constantly monitor and update their information so that they could continue to make sound real estate investments. Additionally, zip codes in other areas may be feasible to invest in for this company so other locations could be analyzed as well. Additionally the roi formula was flawed by using numbers above and below zero so converting to all positive numbers would have been a better approach. 