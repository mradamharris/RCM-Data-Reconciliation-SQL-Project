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
 
<img src="https://i.imgur.com/62TgaWL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Select the disk:  <br/>
<img src="https://i.imgur.com/tcTyMUE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Enter the number of passes: <br/>
<img src="https://i.imgur.com/nCIbXbg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Confirm your selection:  <br/>
<img src="https://i.imgur.com/cdFHBiU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Wait for process to complete (may take some time):  <br/>
<img src="https://i.imgur.com/JL945Ga.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Sanitization complete:  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
