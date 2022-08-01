# World_Weather_Analysis

## Overview
For this project, I was tasked with the responsibility to generate and gather a list of worldwide cities in order to create an interactible map that will allow end users to select potential travel destinations based on their desired weather conditions. With a functional map available, I then had to add the information of Hotels located in the same cities found earlier in order for users to find a place to spend the night. With this tool available users then are able to create an itinerary of their desired destination(s) and also have the ability to plan a route to get there.

## Process

#### Step 1
In order to achieve the desired outcome first I generated a list of cities using NumPy's random.uniform function to create a list of 2,000 latitudes and longitudes that I would then hope to pair with the locations and names of real existing cities.

I then made an API call to the openweathermap.org cite and with the use of a for loop, then matched the coordinates I had just made to existing cities in order to gather other information such as temperature, humidity, country, windspeeds etc. In the event that no city existed or had inadequate usable data, the coordinates were dropped.

Once I had my clean dataframe I exported it onto a CSV file in order to use in the next step.

#### Step 2
Now with a functional dataframe containing all the city and weather information that I needed I had to create an interactable map in order for users to be able to navigate.

To make this happen I used the csv file I had just created, the gmaps plug in and my google API key to be able to make calls that would allow me to use google to gather hotel names located in the cities I had just formatted.

I was then able to find the location's of said hotels and attach them to their corresponding cities in order for our end users to have that information available to them now as well.
