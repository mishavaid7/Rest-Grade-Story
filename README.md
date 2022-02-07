# **An exploration of the DOH's Restaurant Inspection Dataset for New York City.**
The goal of this project is to analyze the [restaurant inspection data provided by the DOH](https://data.cityofnewyork.us/Health/DOHMH-New-York-City-Restaurant-Inspection-Results/43nn-pn8j)

Every restaurant window in New York City has a health inspection grade that they are required to display in their establishment. I’ve always wondered how these inspections work, especially since every restaurant I’ve ever been to has somehow had an ‘A’ grade. Surely, not all eateries in the city are that clean

Nobody quite understands the grading breakdown so I looked at the raw data and [documentation](https://www.opendatanetwork.com/dataset/data.cityofnewyork.us/43nn-pn8j) that the Department of Health provides us with.

# *Look at 'Grades-Rest-DOH.ipynb' for my code.*

I started by removing the spaces in the column names and converting 'GRADE_DATE' and 'RECORD_DATE' to datetime. 

It looks like one row represents one inspection, not one rating, so I made a KEY that could be used to get an average rating for restaurants with multiple inspections. I joint based on 'DBA', 'BUILDING', "STREET", "ZIPCODE". 

We can now see that there are around 180,000 entries but only 25,000 unique restaurants in the dataset.

