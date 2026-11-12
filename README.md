# NYC Taxi Tips: Exploratory Analysis (Learning Project)

**Question:** When and where do NYC taxi passengers tip more?

Notebook: [nyc_taxi_tip_analysis.ipynb](nyc_taxi_tip_analysis.ipynb) (with outputs)

## Data
Seaborn's public `taxis` sample: 6,433 NYC taxi trips and 14 columns (pickup and dropoff time, distance, fare, tip, payment type, taxi color, boroughs).

## Key findings (credit card trips only, n = 4,577)
- Cash tips are recorded as 0 in this data (1,812 cash trips, none with a tip), so cash trips were excluded.
- Typical tip: median 25.5% of the fare (mean 23.8%).
- Hour of day barely matters: median tip % stays about 24 to 27%. The biggest gaps are in hours with few trips (hour 2: 64, hour 3: 47), so they are probably noise.
- Taxi color and borough are tangled together: green taxis tip much less overall (10.3% vs 26.3%), but most green trips start outside Manhattan. Inside Manhattan the gap is small (22.3% vs 26.7%); in Brooklyn and Queens it stays large.

## Limitations
- A sample of 6,433 trips; only 74 Bronx card trips.
- Zero-tip medians in some boroughs (Brooklyn, Bronx) may be a recording issue; not verified.
- Trip distance and fare size were not controlled for.
- Descriptive only: no statistical tests.

## What I learned
- Check how the data is recorded before trusting a number (cash tips were stored as 0).
- The median describes a typical value better than the mean when values are skewed.
- Small groups give unstable medians, so always show the count next to the median.
- Two variables can be tangled together (confounding): compare inside groups.

## Tools
Python, pandas, seaborn (for the dataset), Google Colab.
