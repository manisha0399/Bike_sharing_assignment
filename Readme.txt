=========================================
Dataset characteristics
=========================================	
day.csv have the following fields:
	
	- instant: record index
	- dteday : date
	- season : season (1:spring, 2:summer, 3:fall, 4:winter)
	- yr : year (0: 2018, 1:2019)
	- mnth : month ( 1 to 12)
	- holiday : weather day is a holiday or not (extracted from http://dchr.dc.gov/page/holiday-schedule)
	- weekday : day of the week
	- workingday : if day is neither weekend nor holiday is 1, otherwise is 0.
	+ weathersit : 
		- 1: Clear, Few clouds, Partly cloudy, Partly cloudy
		- 2: Mist + Cloudy, Mist + Broken clouds, Mist + Few clouds, Mist
		- 3: Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds
		- 4: Heavy Rain + Ice Pallets + Thunderstorm + Mist, Snow + Fog
	- temp : temperature in Celsius
	- atemp: feeling temperature in Celsius
	- hum: humidity
	- windspeed: wind speed
	- casual: count of casual users
	- registered: count of registered users
	- cnt: count of total rental bikes including both casual and registered
	
=========================================
Comparison of the Train model and Test model:
Train - R^2 : 0.8185
Test - R^2: 0.8159
We can observe that the temperature variable has the largest coefficient, implying that as the temperature rises, so does the number of bike rentals.
There are also some variables with negative coefficients, as we can see. A negative coefficient indicates that the dependent variable tends to drop as the independent variable increases.
Spring, misty clouds, and light snow are all negative coefficient variables. The coefficient value indicates how much the dependent variable changes when the independent variable is changed by one unit while the other variables in the model remain constant.


=========================================
#Prominent determinants that can be used to forecast demand for shared bikes:
#holiday
#temp
#hum
#windspeed
#Season
#months(January, July, September, November, December)
#Year
#Sunday
#weathersit( Light Snow, Mist + Cloud)