# EPA Confidence Intervals

Confidence interval analysis of EPA air quality (AQI) data in Python, using pandas, seaborn and scipy.

## Notebook

`Activity_Explore_confidence_intervals.ipynb`

Scenario: a renewable energy company operates in California, Florida, Michigan, Ohio, Pennsylvania and Texas. A proposed federal subsidy would apply to states with an average AQI of 10 or above. The notebook:

- Summarizes mean AQI for each of the six states
- Compares AQI distributions with seaborn boxplots
- Builds a 95% confidence interval for the state with the highest mean AQI, by hand and with `scipy.stats.norm.interval()`

## Dataset

`c4_epa_air_quality.csv`: 260 carbon monoxide AQI readings from monitoring sites across 52 US states and territories, all recorded on 2018-01-01. The data is based on US Environmental Protection Agency measurements and was provided through the Google Advanced Data Analytics course on Coursera.

## Key findings

| State | Mean AQI |
| --- | --- |
| California | 12.12 |
| Michigan | 8.11 |
| Florida | 5.50 |
| Ohio | 3.33 |
| Pennsylvania | 2.90 |
| Texas | 2.70 |

- California is the only state above the threshold of 10 and has the widest spread and highest outliers.
- Its 95% confidence interval is 10.36 to 13.88 (standard error 0.90, margin of error 1.76), entirely above 10.
- Caveat: the data covers a single day and states are unevenly sampled (California has 66 rows, many states have 1 to 4), so results should be confirmed with a longer time range.

## Tools

Python, pandas, NumPy, seaborn, SciPy, Jupyter

## How to run

```bash
pip install pandas numpy seaborn scipy jupyter
jupyter notebook
```

c4_epa_air_quality.csv
