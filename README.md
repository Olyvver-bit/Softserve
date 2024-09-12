# Softserve


The purpose of SoftServe is to provide a recommendation on whether or not to go out for soft serve based on the user’s desired IP address—whether it's their own, a friend's, or a family member's. If the temperature outside is above 78°F, the program will recommend getting soft serve.

SoftServe utilizes the IP-API (https://ip-api.com/docs/api:json) to retrieve the latitude and longitude of a given IP address by sending a request and working with JSON data. This particular API was chosen because it is public, simple to use, and provides accurate latitude and longitude information for any valid IP address without requiring an API key.

Once the location data is obtained, SoftServe uses the National Weather Forecast API (https://www.weather.gov/documentation/services-web-api) to get accurate weather data. This API, backed by government satellite data, was selected for its reliability and the fact that it doesn't require an API key. The program retrieves forecast data, specifically focusing on the temperature for the next hour, within a 2.5-square-kilometer area around the provided latitude and longitude. This forecast-based approach accounts for the time it might take the user to get their ice cream, ensuring that the weather conditions won't change drastically before they enjoy their treat.

To use SoftServe, the user is prompted to enter an IP address. The program also provides a link to easily find the user's current IP address, which they can then copy and paste. The program will return a forecast for the next two hour, along with a recommendation on whether or not to get soft serve based on the temperature.

Note: This program works exclusively for public IP addresses located in the US.

