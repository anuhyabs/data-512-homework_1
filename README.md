## Professionalism & Reproducibility

### Goal of the Project

The goal of this project is to construct, analyze, and publish a dataset of monthly article traffic for a select set of pages on Dinosaurs from English Wikipedia from January 1, 2015 through September 30, 2022. The purpose of this is to develop and follow best practices for open scientific research.

### Source Data
The source data comes from **Wikimedia Foundation REST API** which offers a cacheable and straightforward access to Wikimedia's content and data. 

Link to the Wikimedia Foundation REST API terms of use: https://www.mediawiki.org/wiki/REST_API#Terms_and_conditions

### API Documentation
Links to relevant API Documentation:
- https://en.wikipedia.org/api/rest_v1/
- https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews
- https://wikimedia.org/api/rest_v1/#!/Pageviews_data/get_metrics_pageviews_aggregate_project_access_agent_granularity_start_end

### Project Structure

```bash
data-512-homework_1
├── data
│   ├── dinosaur_genera.cleaned.SEPT.2022.csv
│   ├── dino_monthly_desktop_201501-202209.json
│   ├── dino_monthly_mobile_201501-202209.json
│   └── dino_monthly_cumulative_201501-202209.json
├── results
│   ├── maximum_minimum_average.png
│   ├── top_ten_peaks.png
│   └── fewest_months.png
├── source
│   ├── data_acquisition.ipynb
│   └── data analysis.ipynb
├── LICENSE
└── README.md
 ```

### File Descriptions

**data**:
- *dinosaur_genera.cleaned.SEPT.2022.csv* : A CSV file conatining the list of Dinosaur pages from Wikipedia.
- *dino_monthly_desktop_201501-202209.json* : This file is obtained from the data_acquisition notebook and contains data on the monthly desktop page traffic.
- *dino_monthly_mobile_201501-202209.json* : This file is obtained from the data_acquisition notebook and contains data on the monthly mobile app and web traffic.
- *dino_monthly_cumulative_201501-202209.json* : This file is obtained from the data_acquisition notebook and contains data on the monthly cumulative (sum of all movile and all desktop) page traffic.

**results**:
- *maximum_minimum_average.png* : Time series result for the articles that have the highest average page requests and the lowest average page requests for desktop access and mobile access.
- *top_ten_peaks.png* : Time series result for the top 10 article pages by largest (peak) page views over the entire time by access type.
- *fewest_months.png* :  Time series result to show pages that have the fewest months of available data.

**source**:
- *data_acquisition.ipynb* : In this notebook, the data is obtained using the pageviews API.  The counts of pageviews are collected for a set of Dinosaur pages from Wikipedia.
- *data analysis.ipynb* : In this notebook, basic data visual analysis is performed to graph the Dinosaur subset as a timeseries for Desktop and Mobile access type.

