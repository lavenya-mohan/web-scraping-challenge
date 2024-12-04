# Mars Exploration Data Analysis

This project involves scraping and analyzing data related to Mars exploration. The tasks include extracting news about Mars missions and analyzing weather data collected from the Red Planet. The project is divided into two parts:

---

## Part 1: Scrape Titles and Preview Text from Mars News

### Objective
Scrape the latest Mars-related news articles from the Mars News website and organize the information into a structured format.

### Steps
1. **Automated Browsing**:
   - Use Splinter to navigate to the [Mars News Site](https://static.bc-edx.com/data/web/mars_news/index.html).
2. **Data Extraction**:
   - Use BeautifulSoup to parse the webpage HTML and extract titles and preview texts of articles.
3. **Data Organization**:
   - Store each article's title and preview text in a Python dictionary and compile them into a list.
4. **Results**:
   - A collection of dictionaries containing the title and preview of each news article.
   - Optionally, store the scraped data in a file (to ease sharing the data with others). To do so, exported the scraped data to a JSON file and is saved as `mars_news.json`

### Output Example
```json
[
    {
        "title": "NASA's MAVEN Observes Martian Light Show Caused by Major Solar Storm",
        "preview": "For the first time in its eight years orbiting Mars, NASA’s MAVEN mission witnessed two different types of ultraviolet aurorae simultaneously..."
    },
    {
        "title": "NASA Prepares to Say 'Farewell' to InSight Spacecraft",
        "preview": "A closer look at what goes into wrapping up the mission as the spacecraft’s power supply continues to dwindle."
    }
]
```

## Part 2: Scrape and Analyze Mars Weather Data

### Objective
Analyze Mars weather data collected from the Curiosity rover to understand temperature and pressure patterns and estimate the length of a Martian year.

### Steps
1. **Automated Browsing**:
   - Use Splinter to navigate to the [Mars Weather Site](https://static.bc-edx.com/data/web/mars_facts/temperature.html).
2. **Data Extraction**:
   - Scrape the HTML table containing weather data using BeautifulSoup.
   - Parse the data into a Pandas DataFrame.
3. **Data Cleaning**:
   - Convert columns to appropriate data types (e.g., `datetime`, `float`, `int`).
4. **Analysis**:
   - Determine seasonal trends in minimum temperature and atmospheric pressure.
   - Estimate the length of a Martian year in Earth days.

### Key Findings
- **Minimum Temperature**: The coldest month is Month 3, and the warmest is Month 8, showing significant seasonal variations.
- **Atmospheric Pressure**: The lowest pressure occurs in Month 6, and the highest in Month 9, indicating the impact of Mars' thin atmosphere on seasons.
- **Martian Year**: A Martian year is approximately 687 Earth days, as derived from temperature cycles.

### Outputs
- **Plots**: Bar charts for average minimum temperature and atmospheric pressure by month, and a line plot of temperature trends over time.
- **CSV Export**: The cleaned and analyzed data is saved as `mars_weather_data.csv`.
