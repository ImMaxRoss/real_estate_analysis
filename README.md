![mini_house_in_boardroom](./images/mini_house_boardroom.jpeg)

# Real Estate Consulting for King County

#### Authors: Charlie, Gideon, Max

## Overview

Our project analyzes the marketplace for real estate in the city of Seattle.   Seattle Flips real estate company needs to know that their houses are to be sold with maximum profit.   Our project will result in findings relevant for knowledge of the Seattle marketplace, breaking down individual components that helps and relates to a house being sold.


## Business Problem

Seattle Flips is currently trying to find out how to sell their houses.  They are confused with the data that they currently have, making economic sense of it.   Our job is to create the best plan of action to sell these houses for maximum profit.


## Data 
    
Our data is taken from the King County Database, titled csv: data/kc_house_data.csv

URL for King County Coordinate info https://www5.kingcounty.gov/sdc/FGDCDocs/ZIPCODE_fgdc.htm


## Methods

We will first test our initial model, the simple base model.   Then we will test it against our multiple assumptions.  Then we will try additional models for better, more accurate results.   With target being a final model we will create.


## Modeling
 
Our first initial model: ![img](https://i.postimg.cc/JntjvhVg/1.png)

This is our initial model... the simple base model.   Reports an R squared of .380, so a better model is needed.


#### Our assumption testing results:

1. Passes Homoskedasticity
2. Does Not Pass Normality Assumption (We cannot assume our model is normally distributed)
3. Passes Linear Assumption
4. Passes Durbin-Watson Independence Test
5. Does Not Pass Kurtosis Test
6. Passes Final Multicollinearity Test


Our final model ![img](https://i.postimg.cc/HkqQRmss/download.png)

Our final model is SQFT Living vs Price.   The reason we chose SQFT Living is because it is the feature most likely correlated with price - it impacts price the most.


## Results


#### Base Model:
- Adjusted R-squared: 0.380
- F-statistic: 1.789e+04
- Prob (F-statistic): 0.00
- Df Model: 1
- Condition Number: 4.01e+05
- Multicollinearity: Might have strong multicollinearity problems

#### Final Model:
- Adjusted R-squared: 0.626
- F-statistic: 548.7
- Prob (F-statistic): 0.00
- Df Model: 89
- Condition Number: 4.01e+05
- Multicollinearity: Passes multicollinearity.   VIF score under 1.5


Final Model is better as it has a higher adjusted R-squared value (0.625 vs. 0.380), indicating that it explains more variation in housing prices. 

![img](https://i.postimg.cc/K4X0NMVx/2.png)

Our final results indicating Price vs SQFT Living

![img](https://i.postimg.cc/sgzrfQ2k/3.png)

Our final result indicating SQFT Living of Renovated/Unrenovated Homes vs Price

![img](https://i.postimg.cc/T3fzMz7G/4.png)

Price of renovated homes vs price of unrenovated homes


## Conclusions

Our final model features housing prices vs SQFT Living.   However, it takes into account Housing price vs SQFT Living for specific individual homes like waterfront homes/non waterfront homes and SQFT Living vs Housing price for renovated/unrenovated homes.

We see lots of potential for profit with unrenovated homes.   There are many more unrenovated homes than renovated homes in the market - thus we can choose many of these unrenovated homes, renovate them, increas their value, and earn profit.   

We satisify our initial business problem of being unsure what our plan of action is.   We now know our plan of action.   Choosing among 29,000 unrenovated homes (according to our data), we can increase their value by renovating them thus satisfying our intinial desire of maximizing profit.

## For More Information
See the full analysis in the [Jupyter Notebook](./King_County_analysis.ipynb) or review this [presentation](./King_County_Analysis.pdf).

For additional info, contact Charlie at [protigen34](https://github.com/protigen34), Gideon Miles at [Giddybird](https://github.com/Giddybird), or Max Ross at [ImMaxRoss](https://github.com/ImMaxRoss)


## Repository Structure

```
├── data
├── images
├── README.md
├── King_County_Analysis.ipynb
├── King_County_Analysis.pdf
```
