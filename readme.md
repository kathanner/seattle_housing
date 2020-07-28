# King County Housing Price Trends

objective: Provide West Seattle Realty (WSR) with value-added assets to share with their clientele. As a small, local agency, a trend analysis and market predictions tailored to their brand will help distinguish their services from larger national realty services.

approach: Explore the provided dataset, find valuable trends and create a regression model for pricing predictions based on property features.

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

### How does the time of year impact sale prices?

### How do waterfront locations and quality of the view affect sale prices?

#### Waterfront

#### Does it have a view?

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

### Impact of specific coefficients on price

## Recommendations

Present buyers with pricing expectations featuring selections of:
* Grade of Property regarding building construction and design
    * Low (gr 1-3)
    * Average (gr 4-7)
* Bathroom/Bedroom ratio 
    * 1:1 has an average of \\$515K
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

