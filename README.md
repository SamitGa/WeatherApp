Cyber Range Weather App
========================

Description
------------

This app tells the **_temperature_** of a place based on the zip code of the location. The REST API takes the zip code as a **_query param_** and then displays the **_temperature_** as well as the **_scale_** in which temperature is displayed. It works with two scales, *celcius* and *fahrenheit*. The default scale is *fahrenheit*. In the next few articles, I will explain the various use cases of this application.

Getting the temperature when no scale is mentioned
---------------------------------------------------

In this case, the URL looks something like this : **_http://localhost:8080/locations/24060_** where the location is Blacksburg. By default it returns the temperature in Fahrenheit. I have attached a screenshot below that shows the same.

![alt text][logo]

[logo]: https://github.com/SamitGa/WhetherApp/blob/master/Images/without_scale.PNG "Application returning temperature in Fahrenheit by default"

Getting the temperature when Celsius scale is mentioned
--------------------------------------------------------

In this case the URL like this : **_http://localhost:8080/locations/24060?scale=celsius_** where the location is Blacksburg. I have attached a screenshot below that shows the same.

![alt text][logo]

[logo]: https://github.com/SamitGa/WhetherApp/blob/master/Images/celcius.PNG "Application returning temperature in celsius when that is 
mentioned"

Getting the temperature when Fahrenheit scale is mentioned
-----------------------------------------------------------

In this case the URL like this : **_http://localhost:8080/locations/24060?scale=celsius_** where the location is Blacksburg. I have attached a screenshot below that shows the same.

![alt text][logo]

[logo]: https://github.com/SamitGa/WhetherApp/blob/master/Images/fahrenheit.PNG "Application returning temperature in fahrenheit when that is mentioned"

Getting the temperature when the scale is wrong
-----------------------------------------------

In this case the URL like this : **_http://localhost:8080/locations/24060?scale=fahrenheitopia_** where the location is Blacksburg. Please notice that in this case, the scale is **_fahrenheitopia_** instead of **_fahrenheit_**. The application does not return an error but simply gives the temperature in Fahrenheit, which is the default scale. I have attached a screenshot below that shows the same.

![alt text][logo]

[logo]: https://github.com/SamitGa/WhetherApp/blob/master/Images/wrong_scale.PNG "Application returning temperature in fahrenheit when the scale is mentioned wrong"

An incorrect zip code is mentioned
----------------------------------

In this case the URL like this : **_http://localhost:8080/locations/24060000?scale=celsius_**. The zip code in the URL is invalid, hence the appplication returns an error that says **_Invalid Request_** I have attached a screenshot below that shows the same.

![alt text][logo]

[logo]: https://github.com/SamitGa/WhetherApp/blob/master/Images/wrong_zip.PNG "Application returning an error in case of wrong zip code"
