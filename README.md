Estimating Flight Ticket Price Using Linear Regression

In this project, I leveraged data provided by the Bureau of Transportation Statistics to predict the price of airline tickets for flights leaving O'Hare and Midway (the two primary airports in Chicago).

## The Data

The data I used is a modified form of data provided [here](https://www.transtats.bts.gov/Fields.asp?Table_ID=272). The data was cleaned up somewhat before I received it (though not completely!) and subset to flights leaving from MDW and ORD. The available fields are:

- InitID: Unique Identifier for Ticket
- FarePerMile: The amount paid per mile of flight
- Coupons: How many tickets were purchased in the order
- Origin: The departure airport of the flight
- RoundTrip: Was the ticket a round trip ticket or not?
- OnLine: Was the departing flight on the same operating carrier that it was booked on or not?
- RPCarrier: Reporting carrier of the flight (crosswalk table can be found [here](https://www.transtats.bts.gov/Oneway.asp?Field_Desc=Reporting%20Carrier&Field_Type=Char&Sel_Cat=REPORTING_CARRIER&Lookup_Table=L_CARRIERS&Sel_Var=PASSENGERS&Sel_Stat=Sum&Data_Type=CAT&Percent_Flag=0&Display_Flag=0))
- Passengers: Number of passengers on the flight
- ItinFare: Itinerary fare per passenger
- BulkFare: Was the ticket part of a bulk order of tickets?
- Distance: How many miles was the flight?
- DistanceGroup: Pre-binned version of Distance (crosswalk table can be found [here](https://www.transtats.bts.gov/Oneway.asp?Field_Desc=Distance%20Group%2C%20in%20500%20Mile%20Intervals&Field_Type=Num&Sel_Cat=DISTANCE_GROUP&Lookup_Table=L_DISTANCE_GROUP_500&Sel_Var=PASSENGERS&Sel_Stat=Sum&Data_Type=CAT&Percent_Flag=0&Display_Flag=0))

The data can be found at [here](./airline.csv) and, if necessary, a 10% subsample can be found [here](./airline_10.csv).

## Work

In the Jupyter Notebook labeled Project_3.ipynb, one can find the steps that I took to clean and model the data provided by the Bureau of Transportation Statistics. A number of linear regression models were made and they all aim to predict the fare of a ticket (`ItinFare`). 
