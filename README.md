# Bike-sharing-assignment
### Problem statement
A bike-sharing system is a service in which bikes are made available for shared use to individuals on a short term basis for a price or free. Many bike share systems allow people to borrow a bike from a "dock" which is usually computer-controlled wherein the user enters the payment information, and the system unlocks it. This bike can then be returned to another dock belonging to the same system.

A US bike-sharing provider BoomBikes has recently suffered considerable dips in their revenues due to the ongoing Corona pandemic. The company is finding it very difficult to sustain in the current market scenario. So, it has decided to come up with a mindful business plan to be able to accelerate its revenue as soon as the ongoing lockdown comes to an end, and the economy restores to a healthy state.

In such an attempt, BoomBikes aspires to understand the demand for shared bikes among the people after this ongoing quarantine situation ends across the nation due to Covid-19. They have planned this to prepare themselves to cater to the people's needs once the situation gets better all around and stand out from other service providers and make huge profits.

They have contracted a consulting company to understand the factors on which the demand for these shared bikes depends. Specifically, they want to understand the factors affecting the demand for these shared bikes in the American market. The company wants to know:

Which variables are significant in predicting the demand for shared bikes.
How well those variables describe the bike demands
Based on various meteorological surveys and people's styles, the service provider firm has gathered a large dataset on daily bike demands across the American market based on some factors.
### Business Goal
We are required to model the demand for shared bikes with the available independent variables. It will be used by the management to understand how exactly the demands vary with different features. They can accordingly manipulate the business strategy to meet the demand levels and meet the customer's expectations. Further, the model will be a good way for management to understand the demand dynamics of a new market.
### Dataset Information
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
###  Basic Information
- General information
  - Dataset is very much clean and there is no missing values.
  - Dataset is having 16 columns and 730 rows.
  - It has integer, float and object datatype.
- Pre-processing
  - Below columns are dropped
  - instant
  - dteday
  - atemp
  - casual & registered
  - All the columns are renamed for better understanding.
### Finding Categorical Variables
  - Season
  - Year
  - Month
  - Holiday
  - Weekday
  - Workingday
  - Weather
### Creating dummy variables for required categorical variables
  - Season
  - Weekday
  - Month
  - Weather
### Spilting the data
  - Training set = 70
  - Test set = 30
### Exploratory Data Analysis
  - Visualising Numeric Variables
  - Visualising Categorical Variables
  - Correlation Matrix
### Model Building
Several Model building attempts were made and finally came up with good model with all features having very low VIF (less than 5) and very low P-Value(less than 0.05)
  - **Count = 0.123(const)+ 0.233(Year)+ 0.549(Temperature)+ 0.088(Season_2)+ 0.129(Season_4)+ 0.101(Month_9)+ 0.020(Weekday_6)- 0.095(Holiday)- 0.155(Windspeed)- 0.079(Weather_2)- 0.283(Weather_3)**
#### Final Report
- **Train R^2 :0.831**
- **Train Adjusted R^2 :0.828**
- **Test R^2 :0.795**
- **Test Adjusted R^2 :0.785**
- **This seems to be a really good model that can very well 'Generalize' various datasets.**
