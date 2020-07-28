# The Battle of the Neighbourhoods

## Introduction

The US is known for its wide range of food choices from the traditional hamburger to its divine barbeque. An amusing way of getting to know a city, food tours are quickly becoming a favourite among travellers in a so-called trend of "food vacations". In particular, one such delicacy within American culture, pizza, is enjoyed among all food tourists prevalent within all major cities.

For all those tourists who have always wanted to go on a pizza adventure in the US and dont know where to look, I propose a new solution by exploring pizza joint locations in major US cities.

## Data

Using the Foursquare API, I will collect data about locations of Pizza stores in 5 major US cities which are: New York, NY, San Francisco, CA, Jersey City, NJ, Boston, MA and Chicago, IL.
This will be used to show the number of pizza suppliers and its density relative to the city.

## Methodology

My main target here was to asses which city would have the highest Pizza store density. I used the Four Square API through the venues channel and used the near query to extract venues in the cities, using the CategoryID to set it only Pizza suppliers. 

Moreover, I repeated this request for the 5 studied cities and extracted their top 100 venues. I produced a dataframe containing data regarding the name and coordinates of the location and plotted them on the map for visual inspection.

Next, to get an indicator of the density of Pizza Places, I calculated the center coordinate of the venues to get the mean longitude and latitude values with respect to all the Pizza stores. Then I calculated the mean of the Euclidean distance from each venue to the mean coordinates.

## Results

From inspection, each city provides multiple pizza joints often more than Foursquare would like to supply us. The following here are the pictures of the geoplot generated with folium:



#### New York :

![image.png](attachment:image.png)

#### Chicago :

![image.png](attachment:image.png)

#### San Francisco :

![image.png](attachment:image.png)

#### Jersey City : 

![image.png](attachment:image.png)

#### Boston : 

![image.png](attachment:image.png)

Upon inspection, we can see that New York, Jersey City and San Francisco are the most "Pizza dense" cities. In the next phase we calculate the mean coordinate and the mean distance to mean coordinate(MDMC). We represent the mean coordinate with a big green circle and distances with green lines.

#### New York :

MDMC: 0.021556

![image.png](attachment:image.png)

#### Chicago :

MDMC: 0.052805

![image.png](attachment:image.png)

#### San Francisco :


MDMC: 0.028633

![image.png](attachment:image.png)

#### Jersey City :

MDMC: 0.029950

![image.png](attachment:image.png)

#### Boston :

MDMC: 0.035126

![image.png](attachment:image.png)

Therefore our results indicate :

1. New York
2. San Francisco
3. Jersey City
4. Boston
5. Chicago

## Discussion

One thing I noticed in the figures is that there is a Pizza Store a large distance away from Jersey City that is probably giving it a higher MDMC. Taking this as an anomaly and lowering the number of Pizza Stores from 100 to 99, the new MDMC would be: 0.0219953, lower than San Francisco. 

Although this is not a clear indicator of whether you should go to these cities for a pizza tour, it does give a clear insight to the cluster of pizza stores situated around the centre of the city, allowing routes to be tracked and planned.

## Conclusion

Based on the results, there is no doubt that New York is the best place to try pizzas, due to its sheer density of pizza places. Being so close to Jersey City also allows the opportunity to travel between cities and experience more pizza delights. Overall, we recommend to the consumer that a hotel is booked near the mean coordinate if planning to travel to the US especially if travelling to New York.


```python

```
