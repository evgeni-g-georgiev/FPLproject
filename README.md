# Building a scouting tool for Fantasy Premier League managers to identify consistent performers 

## This project builds several metrics to measure player consistency in FPL and utilises K-means clustering to build a scouting tool for managers. 

_Note: all work is written in Jupyter Lab with Python code._

Most FPL managers would resort to looking at total points accumalated in order to guage which players are the most interesting signings. Such an approach is more biased by one-off performances/ outliers. I introduce a more robust **Alpha Metric** that does a better job of identifying _consistent_ performers. Which, I would argue, is more important and valuable from a managing perspective.

![Top 10 Consistent Players by "Alpha Metric"](https://github.com/evgeni-g-georgiev/FPLproject/blob/main/images/Top%2010%20Alpha%20Metric.png?raw=true)

After devising this metric, we utilise k-means clustering to segment players into groups exhibitting similar attributes (i.e. premium, high-points players, budget players with consistent game contributions, squad rotation players etc). This provides the basis of our scouting tool which helps managers identify players based on their specific needs. Our **Alpha Metric** then helps managers identify the best choices based on their specific criteria. 


## How to get up and running with the scouting tool?

I have written the notebooks so that you can run the code sequentially. I have also taken some time to write comment on the codes and explain some of what I do better. 

🚨 **Please note: most of the code should be simple to run on your own computer assuming all relevant packages/libraries are installed. But pay special attention to code where I call specific local filepaths. You will need to change code here to match your own computers filepath.** 🚨

A quick run down here of the different files and folders:

* **"data_visualisation.ipynb":** this is the main file where we work on the consistency metrics, analyse the data and eventually build our scouting tool.
* **"web_scraping.ipynb":** this is the file which you can run to web scrape the FPL website yourself and access the latest live data. Note: the rest of the folders contain data for 2023-2024 season up to gameweek 20 only. If you only need data until gameweek 20, you can simply download the folders I provide.
* **player_dataframes:** folder containing 20 dataframes, one per gameweek, with every FPL players individual statistics for that gameweek.

I also scrape the below data, but it is not used in my code...

* **static_data:** folder containing teams data and some manager performance data.
* **fixtures:** folder containing fixtures information and other related information.

## Some final notes...

I believe this project provides some interesting insights on how to best understand past player performance but I know there are several areas in which it can be improved...

Some suggestions for anything who wants to take things to the next level!

* Spend some improving the UI for the scouting tool. E.g. make it possible for a manager to search by type of player such as "cheap, consistent starting defender for solid defensive team".
* Implement fixture difficulty element into scouting tool. I.e. utlising fixutures data that combines the Alpha consistency Metric with a players fixtures difficulty over next N games to gain better insight into potential future performance.
* Use sentiment analysis to analyse news pre-matches to predict starting line-ups, injuries, etc.

