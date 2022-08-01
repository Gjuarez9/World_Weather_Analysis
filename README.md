# **WeatherPy Project**

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

Then I created input statements that would allow users to select their own preffered weather parameters in order to find a city that met their needs.

```
# 2. Prompt the user to enter minimum and maximum temperature criteria 
min_temp = float(input("What is your desired minimum temperature for your trip? "))
max_temp = float(input("What is your desired maximum temperature for your trip? "))

```

I was then able to find the location's of said hotels and join it with the corresponding cities in order for our end users to have that information available to them in addition to the previouse weather and temperature data I added.

After doing so this is what our map looked like, displaying all our input cities and hotel names.

![WeatherPy_vacation_map](https://user-images.githubusercontent.com/107452167/182255234-379f7548-de07-43fa-b7ab-fcb661ada944.png)

#### Step 3
Lastly using the input statements I was able to create a user case in which the desired temperatures was between 64° & 88° degrees Fahrenheit. This narrrowed the search down & upon furter exploration i found a possible trip near the San Francisco Bay Area.

I chose the cities of Pacific Grove, South Lake Tahoe, San Jose, and Half Moon Bay for our case. Then using gmaps I created a trip route layer that would allow us to visualize the potential route of the trip and it looked like this.

![WeatherPy_travel_map](https://user-images.githubusercontent.com/107452167/182256470-b14be240-d5dd-4a2f-a9ff-19666b37c5a9.png)


## Results
Using gmaps and understanding how to create for loops as well as properly using my Google API key, I was able to create a working map that showed worldwide cities and their respective weather conditions. I was also able to use that information and further expand on it by adding a Hotel field that would allow an end user to locate hotels in the city of their choice. Lastly I was able to create a trip route in order for someone to have the ability to explore many different cities and use all of the afforementioned details to plan accordingly.


