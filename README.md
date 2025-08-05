# IPL-Data-Analysis-using-Apache-Spark-and-Databricks

This project leverages Apache Spark to perform in-depth analysis on IPL (Indian Premier League) cricket data, uncovering insights from ball-by-ball actions, player statistics, team performance and match summaries.

## Dataset Overview
The project uses the following datasets:  
- match.csv: Contains match-level details like venue, date, teams, toss, and result.
- ball_by_ball.csv: Granular data for every ball bowled across matches.
- player.csv: Profile information for players including batting/bowling style and nationality.
- team.csv: Metadata on IPL teams.
- player_match.csv: Player-level stats and attributes per match.

## Project Architecture
This project follows a cloud-based architecture to analyze IPL cricket data using a scalable and modular data pipeline:

<p align="center">
  <img src="https://raw.githubusercontent.com/mpriya19/IPL-Data-Analysis-using-Apache-Spark-and-Databricks/main/assets/Architecture.jpeg">
</p>

- **Data Source:** The raw cricket data, including ball-by-ball events, match details, player stats, and team info, is collected as CSV files.
- **Storage (Amazon S3):** The CSV files are stored in an Amazon S3 bucket, serving as a centralized data lake. This enables efficient and scalable access to structured files.
- **Processing & Transformation:** Azure Databricks with Apache Spark.  
  Apache Spark is used to perform distributed data processing and complex transformations, such as calculating strike rates, economy rates, and aggregating match-level statistics.  
  Spark SQL allows querying of the transformed data using SQL-like syntax, making the analysis accessible and performant.
- **Analytics & Visualization:** Pandas is used for lightweight data manipulation during final-stage analysis while Matplotlib and Seaborn support the visualization of insights such as top players, match outcomes, and performance trends.
- **Platform:** Azure Databricks - All Spark processing, SQL operations, and notebook-based workflows are executed within Azure Databricks, enabling seamless integration, interactive development, and auto-scaling compute.
