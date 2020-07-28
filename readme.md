# King County Housing Price Trends

objective: Provide West Seattle Realty (WSR) with value-added assets to share with their clientele. As a small, local agency, a trend analysis and market predictions tailored to their brand will help distinguish their services from larger national realty services.

approach: Explore the provided dataset, find valuable trends and create a regression model for pricing predictions based on property features.

client presentation: <a href="https://docs.google.com/presentation/d/1VheIM7FTypBAxmL6JM3dZ3q2_4CzjzBK84fcWReRD8M/edit?usp=sharing" target="_blank">Google Slides: King County Housing Price Trends for Potential Buyers</a>

## Dataset

closing property prices for King County sold between May 2014 and May 2015

Includes detailed information including: 
* Sale price
* Sale date
* Property condition and features
* Property location and neighboring property features 

(complete variable list available in the notebook <a href="housing_data.ipynb">housing_data.ipynb</a>)



## Targeted Audience

West Seattle Realty’s Targeted Segment: potential buyers. Specifically, WSR will use trends and insights to create a Buyer's Need-to-Know document for those who are interested in: 
* Expected price based on property features


## EDA

### Is this a good market for flipping homes?

Since less than 1% of the properties have multiple sale dates and renovations in the last 20 years is below 2%, flipping houses in this market is likely difficult. However, if a property does have a logged renovation year, there is an average 34.74% sales price lift

![/resources/reno_pricediff.png](/resources/reno_pricediff.png)

### How does the time of year impact sale prices?

The average quarterly sale price hovers year round at around $446K. There is no significant price change in any specific quarter. It's interesting to note that from the provided dataset, houses sold in Q2 saw a 5.76% sales price lift.

![/resources/salequarter_pricediff.png](/resources/salequarter_pricediff.png)

### How do waterfront locations and quality of the view affect sale prices?

Yes, the trend here shows that waterfront properties on average are selling at 211% higher than properties without a waterfront record in the dataset. The category of view, from ranking 0-4 with zero as nonexistent and 4 being the best view, is directly correlated with prices: higher view rank = higher selling price.

#### Waterfront

![/resources/waterfront_pricediff.png](/resources/waterfront_pricediff.png)

#### Does it have a view?

![/resources/view_pricediff.png](/resources/view_pricediff.png)

## Features

### Assigned grade level

### Bathroom/Bedroom ratio

### Neighborhoods

### Decade of original build

## Final Regression Model

r-squared:  0.7778

mean absolute error (MAE):  105313.8415

mean squared error (MSE):  27295186841.4224

root mean square error (RMSE):  165212.5505

![/resources/finalmodel.png](/resources/finalmodel.png)

### Impact of specific coefficients on price


```python
# looking at a home in Bellevue
x_new = 1
bellevuem = 1.409e+05
c = -1.36e+05
Bellevue_predicted = (bellevuem*x_new)+c
Bellevue_predicted
```




    4900.0



Expect an average additional premium of $4900.00 for properties in Bellevue


```python
# looking at houses built on the waterfront
x_new = 1
wm = 5.607e+05
c = -1.36e+05
w_predicted = (wm*x_new)+c
w_predicted
```




    424700.0



Expect an average price increase of $424,700.00 for properties on the waterfront

## Recommendations

Present buyers with pricing expectations featuring selections of:
* Grade of Property regarding building construction and design
    * Low (gr 1-3)
    * Average (gr 4-7)
* Bathroom/Bedroom ratio 
    * 1:1 has an average of $515K
    * For negotiations, consider the price dip with a 2:1 ratio
* Neighborhoods
    * West Seattle Realty listings that are similar to average for the King County Market
        * Seattle and Kirkland
    * Expect to spend 66% more on properties in the Bellevue neighborhood


## Scale Recommendations (Future Work)

Focus on locality features. Gather more data to develop neighborhood profiles such as:
* Who lives here? Are they the property owners?
* What community amenities are available? (parks, local businesses, entertainment)

Build year-over-year case studies showing neighborhood trends and predictions

