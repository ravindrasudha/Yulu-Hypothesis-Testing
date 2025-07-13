 # Yulu-Hypothesis-Testing

 # Problem Statement
Yulu is India’s leading micro-mobility platform offering eco-friendly electric cycle rentals for shortdistance
urban commutes. Recently, the company has experienced a significant dip in revenues and
wants to identify the factors that influence the demand for its electric cycles.
To address this, the following business questions need to be answered:
Which variables significantly influence the demand for electric cycles (e.g., working
day, weather, season)?
How do environmental and calendar-based factors (e.g., temperature, season, holidays)
affect the number of rentals?
Are there patterns or relationships among the predictors themselves, such as between
weather and season?

 # About Yulu

Yulu is India’s leading micro-mobility service provider, which offers unique vehicles for the daily commute. Starting off as a mission to eliminate traffic congestion in India, Yulu provides the safest commute solution through a user-friendly mobile app to enable shared, solo and sustainable commuting.

Yulu zones are located at all the appropriate locations (including metro stations, bus stands, office spaces, residential areas, corporate offices, etc) to make those first and last miles smooth, affordable, and convenient!

Yulu has recently suffered considerable dips in its revenues. They have contracted a consulting company to understand the factors on which the demand for these shared electric cycles depends. Specifically, they want to understand the factors affecting the demand for these shared electric cycles in the Indian market.


 # Column Profiling:
datetime: datetime
season: season (1: spring, 2: summer, 3: fall, 4: winter)
holiday: whether day is a holiday or not (extracted from http://dchr.dc.gov/page/holiday-schedule)
workingday: if day is neither weekend nor holiday is 1, otherwise is 0.
weather:
1: Clear, Few clouds, partly cloudy, partly cloudy
2: Mist + Cloudy, Mist + Broken clouds, Mist + Few clouds, Mist
3: Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds
4: Heavy Rain + Ice Pallets + Thunderstorm + Mist, Snow + Fog
temp: temperature in Celsius
atemp: feeling temperature in Celsius
humidity: humidity
windspeed: wind speed
casual: count of casual users
registered: count of registered users
count: count of total rental bikes including both casual and registered

 # Concept Used:
Bi-Variate Analysis
2-sample t-test: testing for difference across populations
ANNOVA
Chi-square

 # Insights:
• The T-Test for Workingday vs Count has a P-value of 0.2264. Since this is > 0.05,
we fail to reject the null hypothesis. This means there is no statistically significant
difference in the average electric cycle demand between working days and non-working days.
• The ANOVA for Season vs Count has a P-value of 0.0000. Since this is < 0.05, we reject
the null hypothesis. This means season significantly affects the average electric cycle
demand.
• The ANOVA for Weather vs Count has a P-value of 0.0000. Since this is < 0.05, we reject
the null hypothesis. This means weather significantly affects the average electric cycle
demand.
• The Chi-Square test for Season vs Weather has a P-value of 0.0000. Since this is <
0.05, we reject the null hypothesis. This means weather condition is statistically
dependent on season.
Overall Conclusion: Season and weather conditions are significant factors influencing electric
cycle demand, while the distinction between working and non-working days does not show a statistically
significant difference in average demand based on this analysis.

  # Recommendations
Based on the analysis, here are key recommendations for Yulu:
• Leverage Seasonality: Increase resources in peak seasons (Fall/Summer), consider promotions
in off-peak (Spring/Winter).
• Adapt to Weather: Use dynamic pricing based on weather, efficiently redistribute bikes
during poor conditions, and communicate with users.
• Optimize for Commute: Continue focusing on bike availability in commuter areas during
peak hours.
• Boost Non-Working Day Use: Analyze weekend patterns and target promotions for
leisure/recreational rides.
• Predict Demand: Consider building a model for more precise forecasts and resource planning
