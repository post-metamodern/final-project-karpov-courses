# final-project-karpov-courses

This repository contains two tasks from the final karpov.courses project.

- In the first task I preprocess the data, calculate metrics, and based on that I do A/B testing. I use Python libraries to perform tests and plot graphs.
- In the second task, I connect to the database and create SQL queries to calculate product metrics.

A detailed description of the tasks, as well as the described solution progress, is contained inside the .ipynb files.


## Task 1. A/B testing

Task: Analyze the results of an A/B test, during which the target group was offered a new payment mechanics on the site, and the control group used the basic mechanics. Based on the data obtained, it is necessary to evaluate whether it is worth implementing the new payment mechanics for all users.

Input data: Four CSV files were provided for analysis:

groups.csv — information about users belonging to the control (A) or experimental (B) group.
groups_add.csv — an additional file with users, transferred two days after the start of the experiment.
active_studs.csv — information about users who visited the platform on the days of the experiment.
checks.csv — data on user payments on the days of the experiment.

Metrics: The following were selected as the main metrics for the analysis:

CR (Conversion Rate) — the percentage of users who made a payment. This metric shows the effectiveness of the new mechanics in attracting payments.
ARPPU (Average Revenue Per Paying User) — the average revenue per paying user, which allows us to assess the economic feasibility of the new mechanics.
Differences in metrics: During the analysis, differences were found in the CR and ARPPU values ​​between the control and experimental groups. These differences may be due to changes in user behavior caused by the new payment mechanics.

Statistical significance: To test the statistical significance of differences between the groups, the chi-square and t-tests were used. These tests showed that the observed differences are statistically significant, indicating the impact of the new payment mechanics on user behavior.

Final conclusion: Three statistical tests were conducted, two of which accepted the alternative hypothesis. From this I can conclude that the new mechanics of paying for services on the site turned out to be more effective than the basic mechanics. I believe that the new mechanics of paying for services should be implemented for all users of the site.


## Task 2. SQL

Problem 1: Identifying Very Diligent Students

Problem: An educational platform tracks students' progress in lessons, each of which includes many small tasks called "peas". A very diligent student is one who has solved 20 or more peas correctly at least once during the current month.

Solution: An optimal SQL query was developed that determines the number of very diligent students for the current month. The query takes into account users who have solved at least 20 peas correctly during this period. To ensure optimal performance, the query was structured to minimize the load on the database, taking into account the volume of data and the frequency of requests.

Problem 2: Optimizing the Conversion Funnel

Problem: An educational platform conducted an experiment testing a new payment screen. The experiment divided users into control and target groups, offering different approaches to paying for the course. It was necessary to analyze and compare key metrics for each group, including ARPU (average revenue per user), ARPAU (average revenue per active user), conversion rates (CR) into purchase, and others.

Solution: To solve the problem, a complex SQL query was written that displays the following metrics in one result:

ARPU — average revenue per user, taking into account all those who were included in the experiment.
ARPAU — average revenue per active user who solved more than 10 problems correctly.
CR into purchase — conversion rate into purchase among all users.
CR of active user into purchase — conversion rate among active users.
CR in mathematics — conversion rate among users actively engaged in mathematics.
The query effectively uses aggregation functions and filters, which allows you to get the necessary data in an optimal form, minimizing execution time and resource consumption.


## Task 3. Python

Task 1: Automatic data loading and metrics recalculation

Requirement: Implement a function that automatically loads data from the additional file groups_add.csv, taking into account possible differences in headers, and recalculates key metrics based on this data.

Solution: A function has been developed that performs the following steps:

Data loading: The function first loads the main and additional data. A flexible approach to column naming is used to handle headers that may differ.
Data merging: Data from the additional file is integrated into the main dataset, which allows taking into account new records.
Metrics recalculation: After merging the data, key metrics such as CR (Conversion Rate) and ARPPU (Average Revenue Per Paying User) are recalculated. The function takes into account the new data for more accurate analysis.
Task 2: Plotting graphs by metrics

Requirement: Implement a function for plotting graphs that visualize the recalculated metrics.

Solution: Created a function for visualizing metrics. Function:

Create graphs: Uses matplotlib and seaborn libraries to create graphs. A separate graph is created for each type of metric.
Configure graphs: Graphs are configured to display metrics by groups, with clear axis labels and titles, making it easier to interpret the results.
Print output: Visualization is displayed on the screen taking into account the general appearance and readability of the graphs.
Result: The implemented functions allow you to automatically load data from additional sources, update metrics based on new data, and visualize the results, which facilitates analysis and decision-making based on the results of experiments.









