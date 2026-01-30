<h1>Splunk Data Analysis Configuration Documentation</h1>

<h2>Preview of Splunk Dashboard</h2>


<h2>Description</h2>
This project documents a data analysis process which was developed using a pre-developed dataset of fraudulent transactions from CommonWealth Bank. Through Splunk a variety of search rules were added into the system to generate a visually appealing dataset view which makes it easier to identify the common merchant targets surrounding fradulent transactions within CommonWealth Bank. <br /> <br/> The work demonstrates my ability to utilise Splunk to configure and develop a data anaylsis dashboard to identify trends across fradulent transactions within an organisation, this knowledge is critical within cybersecurity to promptly identify core aspects for improvements. <br /> <br/> This Splunk data analysis dashboard demonstrates my ability to develop data analysis tools using my practical experience in Splunk.
<br />

<h2>Languages and Utilities Used</h2>

- <b>Splunk</b> 
- <b>SPL</b>
- <b>CSV files</b>

<h2>Rules incorporated within Splunk</h2>
<h3>Count Fraudulent Transactions by Category, Age and Merchant</h3>


 - index=your_index_name isFraud=1 | stats count AS fraud_count BY "type" | sort - fraud_count <br />
<br /> In this rule it is used to filter all the transactions to find the fraudulent ones and group them based on category, age and merchant (stats count AS fraud_count BY "type"), while sorting from highest to lowest fraud count (sort - fraud_count). <br /> 

 <h3>Fraud detected by Age, Category, Step (Month), Gender</h3>
 - index=your_index_name isFraud=1 | stats count AS fraud_count BY age category step gender | sort - fraud_count <br />
<br /> In this rule, it is mainly used to find trends in the dataset of fradulent transactions, as well as seeing spikes based on months and comparing target age and gender patterns.   <br /> 

<h3>Gender performed the most fraudulent activities and in what category</h3>

 - index=your_index_name isFraud=1 | stats count AS fraud_count BY gender category | sort - fraud_count <br />
<br /> In this rule, it is basically used to list out the gender that commited the most fraud and the specific category they committed the crime in. <br /> 

<h3>Age group performed the most fraudulent activities and to what merchant</h3>

 - index=your_index_name isFraud=1 | stats count AS fraud_count BY age merchant | sort - fraud_count <br />
<br /> In this rule, it is basically used to list out how age group X committed the most fraud against the specific merchant of Y. 





<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
