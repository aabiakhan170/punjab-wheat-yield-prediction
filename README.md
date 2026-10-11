# Predicting Punjab Wheat Yield from District History and Weather

District-level wheat yield analysis for 36 districts of Punjab, Pakistan (harvest years 2008-2020).

**Question:** does seasonal weather help predict wheat yield, beyond each district's usual yield and a time trend?

**Answer:** mostly no. District averages plus a time trend capture most of the predictable yield (error 231 kg/ha vs 261 for the district average alone). Weather, mainly warm March-April nights, lowers the error by only about 4%, and the gain is not stable across years.

## What I did
- Cleaned official wheat production and area data (opendata.com.pk) and flagged data errors (Kasur and Lahore 2010)
- Added monthly weather from NASA POWER for the wheat season (November-April)
- Validated by holding out one whole year at a time, which is more honest than a random split
- Compared a district average, a year trend, Ridge regression and a random forest
- Built 90% prediction intervals (conformal prediction) that reached 90% coverage overall

## Files
`wheat_yield_analysis.ipynb`: the full analysis with outputs. Run all cells to reproduce it; the data downloads automatically.

## Credits
Yield data: Pakistan Bureau of Statistics via opendata.com.pk. Weather data: NASA POWER Project (power.larc.nasa.gov).

## Author
* **Name:** Aabia Khan
* **Academic Track:** B.Sc. Mathematics Student
