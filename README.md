# UdacityDS

Following a CRISP-DM process, this analysis supports the research on the pricing of new Airbnb listings. It is the first project in Udacity Data Science Nano Degree.

# Prerequisites
Python ver 3.x.

# Business Understanding
This analysis is designed to understand how can Airbnb help a new homeowner in Boston to decide the price of a new listing. Specifically, To understand what elements of a listing affects the owners' decision of pricing by answering the following 3 questions:
1. Is there a seasonality of the price of the listings in Boston?
2. How do the average prices in a different neighborhood in Boston differentiate?
3. What are the top 10 features of a listing that will affect its pricing?

# Data Understanding
The data is from the Boston Airbnb Open Data sets in Kaggle. [https://www.kaggle.com/airbnb/boston] There are 3 datasets:<br />
Calendar provides the availability and price of the listings by calendar date.<br />
Listings provide all the details for the listings.<br />
Reviews provide the detailed reviews for each listings. <br />

# Prepare Data
For the first question, the Calendar dataset is used for understand the seasonalities. The price was converted from currency format to float format. The date is converted to Month and DoW after filtered out the na values.<br />

For the second question, the Listings dataset is merged to Calendar dataset to understand the impact of neighbourhood on pricing. <br />

For the last question, modify the variables in the merged dataset from Question 2 to limit the categorical features to fewer levels. Dropped the Na values. Dropped the object variables that can't be turned into the dummy variables. 

# Data Modeling
With the cleaned dataset, trained a Random Forest Regression model with price as the target variable. This model is to understand the importance of the features to understand the thrid question. 

# Evaluate the Results

Q1

September and October are the peaks of the price while from December to March is the slow season in Boston. Friday and Saturday have the highest price while Monday to Wednesday has the lowest. Interesting to see the relatively high price on Mondays and Sundays in April, which is the probable result of the famous Boston Marathon that held on April Monday in 2016. Another interesting fact is the highest price in September is on Thursday.

Q2

Although listings vary in size and quality, the average price in the different neighborhoods would provide a benchmark for the new hosts who are trying to decide the price of their listings. Leather District is the highest in Boston with an average price of $344.7 and Hyde Park having the lowest average price of $68.8

Q3
1. The top rental feature for a new host to consider when deciding the pricing is if the room type of rental is Entire home/apt.
2. Price more with more bathrooms available.
3. Better to price the extra people fee under 50.
4. Setting the minimum nights more than 4 nights might be too much commitment for tenants
5. For the listings in the Beacon Hill area, the hosts can take advantage of this famous neighborhood when considering pricing. 
6. The hosts who have more than one listing will price differently than the hosts who have only one listing.
7. The more review a listing has, the more impact it will have on the pricing.
8. The number of guests included will also impact the listing's pricing.
9. The hosts who respond will bring more to the tenants, thus can price more.
10. Price more with more bathrooms available.


# Featured Deliverables
https://medium.com/@tamine4185/boston-airbnb-listing-pricing-analysis-udacity-project-926121ce3aaf
