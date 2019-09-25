# Housing-information-in-Victoria-Australia
housing information in Victoria, Australia


# Task 1: Data Integration

COLUMN DESCRIPTION
ID A unique id for the property

Address The property address

Suburb (20/100) The property suburb. The suburb must only be calculated using

Vic_suburb_boundary.zip. Default value: “not available”

Price The property price

Type The type of property

Date Date of sold

Rooms Number of bedrooms

Bathroom Number of bathrooms

Car The number of parking space of the property

LandSize The area of the property

Age The age of the property at the time of selling

Latitude The Latitude of the property

Longitude The Longitude of the property

train_station_id
The closest train station to the property that has a direct trip to the
Southern Cross Railway Station. A direct trip is a trip that there
are no connections (transfers) in the trip from the origin to the
destination. Default value: 0

distance_to_train_station 
The direct distance from the closest train station to the property
that has a direct trip to the Southern Cross Railway Station.
Default value: 0

travel_min_to_CBD
The average travel time (minutes) from the closest train station
(regional/metropolitan) that has a direct trip to the “Southern
Cross Railway Station” on weekdays (i.e. Monday-Friday)
departing between 7 to 9:30 am. For example, if there are 3
direct trips departing from the closest train station to the Southern
Cross Railway Station on weekdays between 7-9:30 am and each
takes 6, 7, and 8 minutes respectively, then the value of this
column for the property should be (6+7+8)/3.). Default value: 0

over_priced?  A boolean feature indicating whether or not the price of the
property is higher than the median price of the similar properties
(with respect to bedrooms, bathrooms, parking_space, and
property_type attributes) in the same suburb on the year of
selling. Default value: -1

crime_A_average
The average of type A crime for three years prior to selling in the
same suburb as the property. For example, if a property is sold in
2016, then you should calculate the average of the crime type A
for 2013, 2014 and 2015. Default value: -1

crime_B_average
The average of type B crime for three years prior to selling in the
same suburb as the property. For example, if a property is sold in
2016, then you should calculate the average of the crime type B
crime for 2013, 2014 and 2015. Default value: -1

crime_C_average
The average of type C crime for three years prior to selling in the
same suburb as the property. For example, if a property is sold in
2016, then you should calculate the average of the crime type C
for 2013, 2014 and 2015. Default value: -1


# Task 2: data reshaping

study the effect of different normalization/transformation methods (i.e.
standardization, min-max normalization, log, power, and root transformation) on Rooms ,
crime_C_average, travel_min_to_CBD , and property_age attributes. You need to observe and
explain their effect assuming that we want to build a linear model on price using these
attributes as the predictors of the linear model and recommend which one(s) do you think would
work better on this data. When building the linear model, the same normalization/transformation
method can be applied to each of these attributes.
