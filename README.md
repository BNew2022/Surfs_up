# Surfs_up

## Overview:

The purpose of this analysis is to analyze rainfall and temperature data provided to see if the island of Oahu is a suitable place to open up a new business that will sell surfboards and accessories, as well as ice cream.  We will look specifically at the months of December and June in this analysis.

## Results:

There are 3 key differences in the weather data between June and December:
  - The average temperature for June is significantly higher by 6.1 degrees (77.2 vs 71.1 degrees Fahrenheit)
  - The highest temperature for June is 5 degrees warmer than December (83 vs 78 degrees Fahrenheit)
  - The lowest temperature for December is 11 degrees cooler than June (60 vs 17 degrees Fahrenheit)

## Summary:

Based on the data provided, we can summarize that the shop is more likely to be busier during the month of June as the warmer weather is more conducive to ice cream and surf board sales.  It would be a good idea to perform additional analysis on precipitation data to give us a better overall weather picture for each month.  We could add the following to our code to pull the precipitation data for each month:

june_prcp = dt.date(2017, 6, 30) - dt.timedelta(days=29)
results = session.query(Measurement.date, Measurement.prcp).filter(Measurement.date >= june_prcp).filter(Measurement.date <= dt.date(2017,6,30)).all()

dec_prcp = dt.date(2016, 12, 31) - dt.timedelta(days=30)
results = session.query(Measurement.date, Measurement.prcp).filter(Measurement.date >= dec_prcp).filter(Measurement.date <= dt.date(2016, 12, 31)).all()
