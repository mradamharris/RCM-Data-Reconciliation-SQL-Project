# RCM-Data-Reconciliation-SQL-Project

<h2>Description</h2>
This project is a single example of my experience in RCM (Revenue Cycle Management) healthcare analytics. The dataset and metrics shown here are a subset of dummy data to protect the rights and privacy of the company this was done for and those it serves. Although the data is fictional, this project was not. It helped an organization identify bottlenecks and millions of dollars in potential miscalculations. Allow me to walk you through an overview of the journey...
<br />


<h2>Languages and Utilities Used</h2>

- <b>SQL Server</b> 
- <b>Excel</b>

<h2>Project walk-through:</h2>

<p align="left">
 A healthcare organization had recently migrated all of their data from one system to another. About a year and a half later, the executives noticed millions in financial losses and huge data gaps in their current reporting. They brought in a team of consultants to locate the major issues. 
 
 That's where I was called in to perform a major reconciliation comparing the data from the former system to the current. They wanted to know the best way to compare "apples to apples" using the previous data as the source of truth.
 
 The first step was understanding the complexity of the data. The new system had the data organized into two servers. One for the data before the major transition to the current system and one for everything after. To take it a step further, they seperated the data between multiple databases within those servers based on the region the data originated from. After multiple talks with the client, it was time to strategize my next steps...<br/>

<img width="80%" height="80%" alt="Focused on Data Insights" src="https://github.com/user-attachments/assets/e040ac7d-819e-4e3c-8fa2-8f69d3e3a0cd" />

I then analyzed the reporting views and compared them to the fact tables they derived from. If all of the data had been migrated over, why would the new database not line up to the previous? I looked for the month with the biggest charge variances. From there I narrowed it down to the day within that month with the largest variance. Lastly, I chose a single patient's charges for that day. That's when I discovered a flaw in the ingestion process. The data was all there if properly pulled from the fact tables, taking into account a few nuances. However, there were outliers due to key identifiers being updated in the system. Because of all the different payment processes, plans and denials, some edits took longer than others to make it to the reporting tables. Seeing how there were only a few analysts but the overall analytics department was in a rebuilding season, it was easy to ascertain why these blind spots existed. It was time to figure out the correct way to query the fact tables in a way the matched the old database. I first produced a query that compared the charges, payments and refunds month by month.

(Insert query link)

After validation, I extracted the data into excel in a straightforward way for the executive team to view. Since there were multiple databases, I had to query each and combine the totals to match that of the old system. At this point, the team began to regain confidence in the integrity of the data. 

(Insert excel file link)

<p align="right">
<img width="80%" height="80%" alt="ChatGPT Image Oct 26, 2025, 06_45_17 AM" src="https://github.com/user-attachments/assets/f5b31cae-b4f9-4d6e-8bfb-dd51c15fcd81" />

Once it was confirmed that everyone was confident in results of the monthly reconciliation, the team wanted me to produce one more query based on my same logic to pull all of the data for the full year at the transaction level. They wanted to be able to continue using this query going forward to gain further insight. Although this wasn't the most complicated part of the project, it took a little more time seeing as how they wanted every transaction from the last couple of years.

(Insert query link)

This was also extracted into multiple excel files and organized for the team to easily assess.

(Insert excel file)

In the end, the company was able to gain insight into how to move forward as an organization. It was a huge weight lifted off of the decision making and a memorable experience!

<p align="middle">
<img width="80%" height="80%" alt="ChatGPT Image Oct 26, 2025, 07_15_18 AM" src="https://github.com/user-attachments/assets/8ce7cdc9-3019-45d6-8429-2995ebce9dbf" />

<p align="middle">
The End

<br />
<br />
</p>
