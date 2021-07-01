<h1>Housing Data for King County <h1>    

<h5>John Carter Simmons, Mallory Wilson, Charlie Fountain<h5>

<h3>Overview<h3>      

In order for us to accurately inform King County home buyers how their potential home renovations would affect the price of their home, we had to go through the process of making multiple models. These models will show how price is affected by different home features and how much the price is affected by these features. In order for us to make a good prediction model, we had to go through the data and clean it in multiple ways. Then we had to figure out which features had the largest effect on price. After discovering this, we found more data and applied it to our model with made it even better. After finding more data, cleaning the data, making multiple models and graphs, we have a better idea on how much different features can affect the price of a home. These results will be shown in multiple graphs.

<h3>Business Problem<h3>  

A Seattle real estate firm has asked us to create a model that allows clients to make a prediction for their home's sale price. This model will make it easier for clients to approximate the price of their home. Clients will now know a ballpark estimate of their homes sale price based off of the features of the home. This allows the real estate firm to focus on finding their client a new home instead of evaluating the previous home. Using this model, the real estate firm can quickly generate a price of any clients home that they are trying to sell.  

<h3> Data <h3>

We used two data sets for our model kc_house_data.csv and King County GIS Census data. The first data set includes information about house features. The King County GIS Census data includes information on Census tract. This is similar to a zipcode but only more specfic. After cleaning these datasets, they allowed us to evalute variables that effect sale price of a home.   

<h3> Methods <h3>

In this project we used linear regression to create models that would predict the price of a home. This took the majority of the time because we created many different models in order to find the one that predicts the most accurately. In order to find the most accurate model, we had to clean the data (getting rid of NaNs and ?'s), then scale the data using StandardScaler, log the data to make it more accurate, and find and clean new data. Some models crash and burned and others prevailed. Before we could do this, we used a variety of PANDAS methods to clean and filter our data. 

<h3> Results <h3>

Our early models used all original data from the kd_housing_data.csv. We included sqft_living, sqft_lot, sqft_living15, sqft_lot15, sqft_above, grade, condition, bathrooms, bedrooms, yr_built, lat, long, condition, grade. This gave us an Training RMSE of 205095.986and for Testing RMSE: 211169.6608. This number is very high so we brainstormed ways to lower it. We developed some strategies including cleaning data, gitting rid of outliers, and finding which features had highest coefficients when compared to price. Most importantly we imported more data from a census website. This allowed us to create these new columns empty_lot_space = sqft_living-sqft_lot, Compared_to_neighbors = sqft_living/sqft_living15, and Median Household Income from King County GIS. All of cleaned and new data created our best model. The new models Training RMSE was 137130.563 and our Testing RMSE was 137400.419. This was a large increase from our first model.
 





We created a model that can predict the price of a home based off the features given. This helps house sellers accuratly depict how much money they can get for their house.

Here are some visualizations that were created during the process of creating our models. Each visual will be explained in a line before the visual. 

This is a heatmap of all the features and our target in a heatmap. The bigger the square the higher correlation 2 variables have with each other.

![Screen%20Shot%202021-07-01%20at%202.48.39%20PM.png](attachment:Screen%20Shot%202021-07-01%20at%202.48.39%20PM.png)

Our next histogram shows our target variable (price) before we dealt with the outliers. As you can see this was very top heavy and would have skewwed our model if we did not normalize the distrbution. 

![Screen%20Shot%202021-07-01%20at%2011.25.52%20AM.png](attachment:Screen%20Shot%202021-07-01%20at%2011.25.52%20AM.png)

We generalized our target variable so it would have a normal distribution. 

![Screen%20Shot%202021-07-01%20at%202.59.49%20PM.png](attachment:Screen%20Shot%202021-07-01%20at%202.59.49%20PM.png)

This graph shows how census tract median household income aligns with home price quantiles. As you can see the higher the income in the area, the more expensive the house will be. 

![Screen%20Shot%202021-07-01%20at%203.05.43%20PM.png](attachment:Screen%20Shot%202021-07-01%20at%203.05.43%20PM.png)

This is a scatter plot that shows price and Sqft living. As you can see the bigger the house the higher the price. 

![Screen%20Shot%202021-07-01%20at%203.05.53%20PM.png](attachment:Screen%20Shot%202021-07-01%20at%203.05.53%20PM.png)

Here we have a map of King County. The darker blue dots show the cheaper houses and the dark red dots show the most expensive houses. The varying shades of green show the median household income in that designated area. 

![Screen%20Shot%202021-07-01%20at%203.48.05%20PM.png](attachment:Screen%20Shot%202021-07-01%20at%203.48.05%20PM.png)

<h3> Conclusions <h3>

In conclusion, we found a couple attributes of a house that have large impact on the  selling price of a home. In particular, the features, Grade, Empty Lot Space, Square Foot Living, Square Foot Lot, and Median Household Income have a large effect on a homes selling price when these features are compared to neighboring houses. For example, if the house the owners  want to  sell has a square foot living that is larger than the neighboring houses, that house would sell for more. 

If we were able to take this project furthur, we would look into making something that would allow individuals who are hoping to sell their home to plug all of their home's information into a website that would spit out the time they should sell their home and at what price. 

## For More Information 

Please review our full analysis in our Jupyter Notebook or our Presentation. For any additional questions, pkease contact Mallory Wilson at mallorye1103@gmail.com, Charlie Fountain at charliefountain122@gmail.com, and John Carter Simmons at johncsimmons99@gmail.com

## Repository Structure


```
project-folder
    |
    README.md
    data-folder
    images-folder
    notebooks-folder
          |
          report.ipynb
          exploratory-folder
                  |
                  johncarter
                  mallory 
                  Charlie 
```