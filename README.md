# Final-Project-Statistical-Modelling-with-Python

## Project/Goals
(fill in your description and goals here)
The goal of this project is to accomplish statistical modeling through the use of the Python programming language.
This will involve querying APIs, and build regression models.
## Process
### Step 1
The first step was simple in theory, use the CityBike API to get the bike-share points for a given town.

After some trial and error with finding a city that returned json, I was able to then cut it down into a usable DataFrame.

### Step 2
Using the geo-coordinates of the individual bike points, I query the FourSquare and Yelp APIs for a radius of 1000m around the bike points to find points of interest (POIs), such as restaurants and such, around the bike points

To save on processing time and on my limited number of allowed queries, I tested this on a smaller sample of the bike points.

Yelp ended up providing better information over FourSquare.

### Step 3
Using the ID of the bike points, I joined the bike point dataframe on the Yelp dataframe, and was then able to aggregate the columns in order to test for a pattern. 

I used a scatter plot to test the average distance a POI is from the bike point to the average number of reviews that POI has on Yelp.

### Step 4
Once again joining the bike and Yelp dataframes, I attempted to build a simple linear regression between the dataframes using the number of free bikes per point against the average number of reviews in the nearby POIs.

The resulting model had an R-squared of 0.255, meaning it could be dangerous to draw strong conclusions. However, the P-value was 0 and the coefficient was positive, suggesting that there may be a relationship between the variables.


## Results
(fill in what you found about the comparative quality of API coverage in your chosen area and the results of your model.)

As mentioned before, the Yelp API proved to have better coverage than FourSquared. Its responses returned data on areas FourSquare lacked, like number of reviews and ratings, and offered further elaboration on areas that FourSquare did provide, such as what type of restaurant a POI is.

## Challenges 
(discuss challenges you faced in the project)
The largest problem is one that was not caused by the project itself, it was my own struggles to start and stay on topic. 

Once I overcame this, the next struggle was CityBikes API's lacking documentation. It took longer than necessary to figure out how it worked.

Once that was sorted, the last two hurdles were as follows:
*  The limited number of allowed queries from Yelp and FourSquare, requiring great care to not overspend.
* The general difficulty of linear regression as a subject.

## Future Goals
(what would you do if you had more time?)

Given more time, and the assumption that I wouldn't squander it, I believe I would like to improve my regression model in order to find a larger R-squared. 
