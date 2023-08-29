# Weather API

This is a simple Python script that demonstrates how to use the OpenWeatherMap API to get the weather for a given city.

## Step 1: Import the necessary libraries

The first step is to import the necessary libraries. In this case, we need the `requests` library to make HTTP requests to the OpenWeatherMap API.

```python
import requests
```

## Step 2: Define the base URL and API key

Next, we need to define the base URL for the OpenWeatherMap API and our API key. The base URL is `http://api.openweathermap.org/data/2.5/weather?`. Our API key can be found on the OpenWeatherMap website.

```python
base_url = "http://api.openweathermap.org/data/2.5/weather?"

api_key = "YOUR_API_KEY_HERE"
```

## Step 3: Get the city name from the user

Next, we need to get the city name from the user. We can do this using the `input()` function.

```python
city_name = input("Enter city name: ")
```

## Step 4: Construct the complete URL

Now that we have the city name, we can construct the complete URL for the OpenWeatherMap API. We do this by concatenating the base URL, the API key, and the city name.

```python
complete_url = base_url + "appid=" + api_key + "&q=" + city_name
```

## Step 5: Make the request to the OpenWeatherMap API

Now that we have the complete URL, we can make the request to the OpenWeatherMap API using the `requests` library.

```python
response = requests.get(complete_url)
```

## Step 6: Check the status code

The `requests` library returns a `Response` object. The `status_code` attribute of this object contains the status code of the response. We can use this status code to check if the request was successful.

```python
if response.status_code == 200:
    print("Request was successful")
else:
    print("Request failed")
```

## Step 7: Parse the JSON response

If the request was successful, the `Response` object will contain a JSON response.
