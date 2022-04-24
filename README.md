# weather-polybar-plugin
Weather plugin for the polybar panel

![preview](https://raw.githubusercontent.com/GuidoFe/weather-polybar-plugin/main/preview.png)

## Description
This Polybar plugin uses OpenWeather API to get and display information about the current weather, including the type of event (clear, moderate rain, fog etc.), temperature (Celsious, Fahrenheit or Kelvin) and an alert for strong winds. The icons change accordingly with the local sunrise and sunset times. 

The colors are easily customizable via constants defined at the beginning of the script.

You will need to provide your personal (and free) api key that you can obtain at https://openweathermap.org/api

## Installation

1. Copy and paste your API key in a simple text file. The default location is $HOME/.owm-key
2. Put the script where you want, and 
3. Make the script executable via `chmod +x /path/to/your/script`
4. Add this to your Polybar config file:
```
[module/weather]
type = custom/script
exec = /PATH/TO/YOUR/SCRIPT.sh
tail = false
interval = 960
```
5. Add the plugin to your polybar panel

## Configuration

Take a look at the beginning of the script for all the settings.

You must use a NerdFont https://www.nerdfonts.com

Change CITYNAME and COUNTRYCODE with your desired location.

Set WEATHER_FONT_CODE to the polybar font you want to use to display the weather type and wind icon, and set the TEMP_FONT_CODE to the font for the thermometer icon (it was too big with the first font)

You can change the text language by setting the LANG variable. You can find the available languages and their codes at https://openweathermap.org/current#list

