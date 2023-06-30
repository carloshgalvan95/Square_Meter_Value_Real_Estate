# Price per Square Meters of Real Estate Properties
---
The most important factor that influences the price per square meter of a property.

## Dataset
---
![dataset](https://github.com/carloshgalvan95/Square_Meter_Value_Real_Estate/blob/main/resources/correlation_matrix.png)

After evaluating the variables scraped from our website data source we identify a few important ones:

- Number of Bedrooms
- Amenities
- Location

Nevertheless, this could be due to the nature of the numbers and the data not being standardized and it's something we will be able to evaluate way better further down the road when we have a predictive model.

## Number of Bedrooms
---
![bedrooms](https://github.com/carloshgalvan95/Square_Meter_Value_Real_Estate/blob/main/resources/violin_chart.png)

we see that we get an unusual correlation with this feature, the reason being there's probably a drop-down point on the marginal value a square meter of land can be conveyed in regards to the price per square meter.


## Amenities
---
![amenities](https://github.com/carloshgalvan95/Square_Meter_Value_Real_Estate/blob/main/resources/violin_chart2.png)

In regards to this feature, we see that the tendency drops down in the middle, to then raise when we get to a higher number of amenities. This could also be due to the method we used to replace the NaN values of our dataset which can be evaluated further down the road as one of our possible improvements.

## Parking Spaces
---
![parking](https://github.com/carloshgalvan95/Square_Meter_Value_Real_Estate/blob/main/resources/violin_chart3.png)

As expected, having three parking spaces available is something not common, and we see the corresponding jump in price associated.

## Days on site
---
![days](https://github.com/carloshgalvan95/Square_Meter_Value_Real_Estate/blob/main/resources/correlation_days_sqrmtr.png)

We see a correlation between the days on-site feature and the price per square meter. Properties with higher days on site will most likely be less desirable and the more days it has on the platform, the most likely it is to correspond to lower prices.

## Gentrification Factor
---
One of the most predominant topics of discussion, whenever Real Estate and Property Value comes up, is gentrification. In order to boost the predictive capabilities of our possible model and be able to identify tendencies. Let's introduce two features with the possibility to broaden them down the road…

The approach for this will be to determine a radius for each franchise and determine how many Starbucks and Airbnbs there are within that distance of each property to see if they play an important role as a possible indicator of the price per square meter expected.

## Number of Airbnbs nearby
---
![airbnbCorrelation](https://github.com/carloshgalvan95/Square_Meter_Value_Real_Estate/blob/main/resources/correlation_airbnb_sqrmtr.png)

When Analyzing two of our other important variables we see that the number of Airbnbs nearby the property does correlates to higher property prices. This could be due to two main reasons:

- The properties with more Airbnbs nearby will tend to be in denser population areas.
- Airbnbs tend to be located on touristic sites, where the property value increases.

## Making Predictions
---
![model](https://github.com/carloshgalvan95/Square_Meter_Value_Real_Estate/blob/main/resources/mlmodel.png)

For our predictive model, we will start with the general rule of, the simpler, the better, trying to use a linear regression model which would aid with costs, time, and resources. Assuming that it's probably not going to be enough, we will then proceed to try a Random Forest Regressor and a Gradient Boosted Regressor.

To be able to visualize the importance that each feature represents in our model, after determining which is our best-performing model, we are going to get each feature's importance and visualize it to gather conclusions.

## Tell me where you live, and I will tell you how much you pay…
---
![features](https://github.com/carloshgalvan95/Square_Meter_Value_Real_Estate/blob/main/resources/features.png)

### Is it important? if so, how important?
---
From our final chart, we can see that the most important features to determine the price per square meter of a property are:

- Vendor: We should take this with a grain of salt given that this is not an inherent variable of the property itself. Nevertheless is safe to assume that the vendor will play a significant role in the average value of the property. This will also help us determine tendencies and how every vendor plays with the market price.
  
- Neighbourhood: I will consider this to be our main feature to consider, the location of the property will play the most important role to determine the price per square meter of the property due to multiple factors, some of them previously mentioned, like how touristic the area is or how densely populated it is. All of them increase the desirability associated with that area.

- Street: This further confirms the hypothesis stated before, but it would be useful to evaluate the colinearity of both variables down the road to see if we can gain some predictive power in our model.
  
- Number of Bedrooms: The correlation this feature plays is interesting to analyze, the number of bedrooms will increase the square meters built dividing the price among more square meters. It would be also interesting to deepen the correlation and determine if there is any point of marginal return where the increase of bedrooms or square meters starts to diminish.
  
- Airbnb Average Price per Night: As our previous hypothesis stated, gentrification will play an important role in evaluating real estate market tendencies, and adding this feature proved useful in order to increase the predictive power of our model.

