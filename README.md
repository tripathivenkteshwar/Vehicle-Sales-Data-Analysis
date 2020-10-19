# Vehicle-Sales-Data-Analysis
* *Vehicle sales data analysis from the RTA of the state of Telangana.*
* *It will help the automobile companies to under stand the Telangana market and it will give the insight of product performance*

## Resources Used 
**Python Version:** 3.7  
**Packages:** pandas, numpy, matplotlib, glob

## Play with Data
After loading the data, I needed to merge the data but some data file need to have same column name so that it should merge properly. I made the following changes and created the following variables:

*	Removed column slno
*	fuel columns have some categories with shorthand which need to be fixed 
*	Handling missing values of fuel column
     * Missing value in fuel column, filled as per vehicleClass column values 
     * if frequency of specific fuel type is considerably very high then that value is used in filling particular vehicleClass nan value 
     * if ferquency count is nearly same then random filling is done 
*	Handling missing values of OfficeCd column
     * 1.) group the rto and category
     * 2.) take the top 3 most frequent OfficeCd of peticular group
     * 3.) randomly fill that value in perticular group
* Alert Bamm:
     * Some colour value have NIL value (I am not talking about NAN or Null or missing values) but the value of colour is filled as NIL rather some colour value eg RED, Black etc.
     * So replacing Colour NIL value with most frequent colour of perticular vehicle class
*	Now Handling missing values of colour column
     * Filled nan value with most frequent colour of perticular vehicle class
*	Parsed rating out of company text 
*	Made a new column for manufacturing month and manufacturing year by Parsing makeYear


## EDA
I looked at the distributions of the data and the value counts for the various categorical variables.

![alt text](https://github.com/tripathivenkteshwar/Vehicle-Sales-Data-Analysis/blob/main/img/Capture.JPG)
![alt text](https://github.com/tripathivenkteshwar/Vehicle-Sales-Data-Analysis/blob/main/img/disVehicleClass.JPG)
![alt text](https://github.com/tripathivenkteshwar/Vehicle-Sales-Data-Analysis/blob/main/img/distriManufac.JPG)
![alt text](https://github.com/tripathivenkteshwar/Vehicle-Sales-Data-Analysis/blob/main/img/distriSeat.JPG)
![alt text](https://github.com/tripathivenkteshwar/Vehicle-Sales-Data-Analysis/blob/main/img/distributionAge.JPG)
