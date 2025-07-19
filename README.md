# Cricket Data Analytics 🏏

The **Cricket Data Analytics** project is a comprehensive data-driven analysis of the T-20 Cricket World Cup. This project leverages **Power BI** to create an interactive dashboard that allows users to explore and analyze match statistics, player performances, and team strategies from the tournament. Additionally, the dashboard provides tools to help you select the best possible playing 11 from the pool of players participating in the World Cup.

> To interact with the dashboard, you can download the `.pbix` file from the repository and open it locally using **Power BI Desktop**.

---

## Project Overview

This project focuses on analyzing data from the T-20 Cricket World Cup using advanced analytics techniques. By combining **web scraping**, **data cleaning**, **data transformation**, and **data visualization**, this project offers insights into player performance, team dynamics, and match outcomes. The final output is an interactive Power BI dashboard that enables users to make informed decisions about team selection and strategy.

---

## Key Features of the Dashboard

1. **Match Analysis**:

   - Analyze key match statistics such as runs scored, wickets taken, strike rates, economy rates, and more.
   - Compare team performances across different matches and venues.

2. **Player Performance Metrics**:

   - Evaluate individual player performances using metrics like batting average, bowling average, strike rate, and economy rate.
   - Identify top performers in batting, bowling, and all-round categories.

3. **Team Composition**:

   - Use the dashboard to select the best playing 11 based on player performance metrics.
   - Filter players by role (batsman, bowler, all-rounder) and performance indicators.

4. **Venue Analysis**:

   - Understand how different venues impact match outcomes.
   - Analyze historical data to identify patterns in team performance at specific venues.

5. **Interactive Filters**:
   - Apply filters to focus on specific teams, players, or matches.
   - Customize your analysis by selecting date ranges, player roles, and other parameters.

---

## Project Structure

The project is organized into several directories and files, each serving a specific purpose in the data pipeline:

```
Cricket-Data-Analytics/
│
├── t20-csv-files/                # Contains raw and processed CSV files
│   ├── dim_match_summary.csv     # Match summary data (e.g., match results, venue details)
│   ├── dim_players.csv           # Player information (e.g., player names, roles)
│   ├── fact_batting_summary.csv  # Batting statistics for players
│   └── fact_bowling_summary.csv  # Bowling statistics for players
│
├── t20-json-files/               # JSON files containing raw scraped data
│   ├── t20_wc_batting_summary.json  # Raw batting data in JSON format
│   ├── t20_wc_bowling_summary.json  # Raw bowling data in JSON format
│   ├── t20_wc_match_results.json    # Raw match results data in JSON format
│   └── t20_wc_player_info.json      # Raw player information data in JSON format
│
├── T20 Analytics Dashboard.pbix  # Power BI dashboard file
│
├── t20-data-processing.py        # Python script for processing raw JSON data into CSV files
│
└── README.md                     # Project documentation
```

---

## Steps Involved in the Project

### 1. **Requirement Scoping** 📝

- Defined the scope of the project, focusing on T-20 Cricket World Cup data.
- Identified key metrics for analysis, including player performance, team performance, and match outcomes.
- Outlined the deliverables, including the creation of an interactive Power BI dashboard.

### 2. **Data Collection using Web Scraping** 🌐

- Extracted raw data from the [ESPN Cricinfo](http://www.espn.in/cricket/) website using **Bright Data**.
- Used Bright Data's web scraping infrastructure to efficiently scrape large volumes of data, including:
  - Match results
  - Player statistics (batting, bowling, fielding)
  - Team compositions
  - Venue details
- Ensured data accuracy by cross-referencing multiple sources.
- Saved the raw data in JSON format under the `t20-json-files/` directory:
  - `t20_wc_batting_summary.json`: Raw batting data.
  - `t20_wc_bowling_summary.json`: Raw bowling data.
  - `t20_wc_match_results.json`: Raw match results data.
  - `t20_wc_player_info.json`: Raw player information data.

### 3. **Data Cleaning and Preprocessing** 🧹

- Processed the raw JSON data using the Python script `t20-data-processing.py`.
- Cleaned the raw data using **Pandas** in Python.
- Handled missing values, removed duplicates, and standardized data formats.
- Created new features such as strike rates, economy rates, and player rankings.
- Converted the cleaned data into CSV files and saved them in the `t20-csv-files/` directory:
  - `dim_match_summary.csv`: Match summary data (e.g., match results, venue details).
  - `dim_players.csv`: Player information (e.g., player names, roles).
  - `fact_batting_summary.csv`: Batting statistics for players.
  - `fact_bowling_summary.csv`: Bowling statistics for players.

### 4. **Data Transformation in Power Query** 🪄

- Imported the cleaned CSV files into **Power BI**.
- Used **Power Query** to further transform and shape the data for analysis.
- Created calculated columns and applied filters to enhance data usability.
- Merged multiple datasets (e.g., player stats, match results) to create a unified data model.

### 5. **Data Modelling and Building Parameters in Power BI using DAX** ⚒️

- Built a robust data model in Power BI using **DAX (Data Analysis Expressions)**.
- Created custom measures for advanced analytics, such as:
  - Batting Average: `Total Runs / Number of Innings`
  - Bowling Average: `Total Runs Conceded / Wickets Taken`
  - Strike Rate: `(Runs Scored / Balls Faced) * 100`
- Developed parameters to allow dynamic filtering and customization of the dashboard.

### 6. **Building the Dashboard in Power BI** 📊

- Designed an intuitive and user-friendly dashboard in Power BI.
- Included various visualizations such as bar charts, line graphs, heatmaps, and tables.
- Added interactive slicers and filters to enable users to drill down into specific data points.
- Highlighted key insights through KPIs and summary cards.
- Saved the final Power BI dashboard as `T20 Analytics Dashboard.pbix`.

---

## Tools and Technologies Used

- **Python**: For web scraping and data preprocessing.
- **Pandas**: For data cleaning and manipulation.
- **Bright Data**: For extracting data from HTML pages.
- **Power BI**: For data visualization and dashboard creation.
- **Power Query**: For data transformation and shaping.
- **DAX (Data Analysis Expressions)**: For creating custom measures and calculations.

---

## How to Use the Dashboard

1. **Download the `.pbix` File**:

   - Clone the repository and download the `T20 Analytics Dashboard.pbix` file.

2. **Open in Power BI Desktop**:

   - Install **Power BI Desktop** from the official Microsoft website if you haven't already.
   - Open the `.pbix` file in Power BI Desktop.

3. **Interact with the Dashboard**:

   - Use the interactive filters to explore different aspects of the data.
   - Select specific teams, players, or matches to focus on.
   - Use the "Best Playing 11" feature to select your ideal team based on performance metrics.

4. **Export Insights**:
   - Export visualizations or data tables for further analysis or reporting.

---

## Future Enhancements

- **Real-Time Data Integration**: Incorporate real-time match data using APIs to provide live updates.
- **Predictive Analytics**: Implement machine learning models to predict match outcomes and player performances.
- **Advanced Visualizations**: Add more sophisticated visualizations, such as network graphs to show player interactions.
- **Mobile-Friendly Dashboard**: Optimize the dashboard for mobile devices to enable on-the-go analysis.

---

## Conclusion

The **Cricket Data Analytics** project provides a powerful tool for cricket enthusiasts, analysts, and team selectors to gain deep insights into T-20 Cricket World Cup data. By leveraging web scraping with **Bright Data**, data cleaning, and advanced analytics, this project offers a comprehensive view of player and team performances. The interactive Power BI dashboard makes it easy to explore data and make informed decisions about team selection and strategy.

Feel free to contribute to this project by suggesting improvements or adding new features!

---

## Acknowledgments

- **ESPN Cricinfo**: For providing the rich dataset used in this project.
- **Bright Data**: For enabling efficient and scalable web scraping.
- **Power BI Community**: For support and resources on building effective dashboards.
- **Python Libraries**: Special thanks to Pandas and Requests for making data collection and cleaning seamless.

---

Happy Analyzing! 🏏📊
