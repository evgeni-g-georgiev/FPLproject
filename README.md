# Building a Scouting Tool for Fantasy Premier League Managers to Identify the Best Players Based on Specific Requirements

## This project develops several metrics to assess player consistency in FPL and employs K-means clustering to create a scouting tool for managers.

_Note: All work is conducted in Jupyter Lab using Python._

Most FPL managers tend to look at total points accumulated to gauge which players are the most appealing signings. However, this approach can be biased by one-off performances or outliers. To tackle this, I've introduced a more robust **Alpha Metric** that better identifies _consistent_ performers. Consistency, I believe, is key and more valuable from a managerial standpoint.

![Top 10 Consistent Players by "Alpha Metric"](https://github.com/evgeni-g-georgiev/FPLproject/blob/main/images/Top%2010%20Alpha%20Metric.png?raw=true)

After developing this metric, we utilize K-means clustering to segment players into groups exhibiting similar attributes (i.e., premium, high-points players, budget players with consistent game contributions, squad rotation players, etc.). This provides the basis of our scouting tool, which helps managers identify players based on their specific needs. Our **Alpha Metric** then assists managers in pinpointing the best options based on their unique criteria.

## How to Get Up and Running with the Scouting Tool?

I've written the notebooks so that you can run the code sequentially. I've also taken the time to comment on the code and explain some of my processes more clearly.

🚨 **Please note: most of the code should be straightforward to run on your own computer, assuming all relevant packages/libraries are installed. However, pay special attention to code where I specify local file paths. You will need to adjust these to match your computer's file paths.** 🚨

A quick rundown of the different files and folders:

- **"data_visualisation.ipynb":** This is the main file where we focus on consistency metrics, analyze the data, and eventually build our scouting tool.
- **"web_scraping.ipynb":** Run this to web scrape the FPL website yourself and access the latest live data. Note: the rest of the folders contain data for the 2023-2024 season up to Gameweek 20 only. If you need data up until Gameweek 20, you can simply use the folders I've provided.
- **player_dataframes:** Folder containing 20 dataframes, one for each Gameweek, with individual statistics for every FPL player.

I also scrape the following data, but it is not used in my code:

- **static_data:** Folder containing team data and some manager performance data.
- **fixtures:** Folder containing fixture information and other related data.

## Some Final Notes...

I believe this project provides some valuable insights on how to best understand past player performance, but I'm aware there are several areas in which it can be improved...

Here are some suggestions for anyone who wants to take things to the next level:

- Invest time in improving the UI for the scouting tool. E.g., make it possible for a manager to search by type of player, such as "affordable, consistent starting defender from a solid defensive team".
- Implement a fixture difficulty element into the scouting tool. For instance, use fixture data that combines the Alpha Consistency Metric with a player's fixture difficulty over the next few games to gain better insight into potential future performance.
- Apply sentiment analysis to analyze pre-match news for predicting starting line-ups, injuries, etc.
