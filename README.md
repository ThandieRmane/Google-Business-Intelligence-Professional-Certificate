# Google Fibre

## Table Of Contents <br>
1. [Background](#Background)
2. [Merging Data](#Merging-the-data-with-SQL)
3. [Stakeholder Requirements Document](#Stakeholder-Requirements-Document)
4. [Project requirements Document](#Project-Requirements-Document)
5. [Strategy Document](#Strategy-Document)
6. [Conclusion](#Conclusion)
7. [Dashboard](Google_Fibre_Dashboard.pbix)

## Background

Google Fibre provides individuals and businesses with fibre optic internet. As part of their interview process, the Fibre customer service team has requested that I design a dashboard using fictional data. 

The team needs to understand how often customers phone customer support again after their first enquiry. Further, leaders want to explore the trends in repeated calls to understand why customers are calling more than once, as well as to improve the overall customer experience. The insights provided by the dashboard will inform the team's next steps. 

The information provided was 3 seperate spreadsheets for market 1, 2 and 3. The spreadsheets were combined on Bigquery using a union (SQL). Only information for January, February and March 2022 was provided. 

## Merging the data with SQL

```SQL
SELECT *
FROM market_1
UNION
SELECT *
FROM market_2
UNION
SELECT *
FROM market_3;
```
[Access the table here](FibreUnionTable.csv)

## Stakeholder Requirements Document
                                                                                        
**BI Professional:** Thandie R. 

**Client/Sponsor:** Google Fibre. Emma Santiago (Hiring manager).

**Business problem:** To determine how often customers call back after the first inquiry. To explore the trend in repeated calls to identify why customers have to call more than once and to explore how to improve the overall customer experience. 

**Stakeholders:** <br>
-Emma Santiago (Hiring manager)<br>
-Keith Portone (Project manager)<br>
-Minna Rah (Lead BI Analyst)<br>
-Ian Ortega, BI Analyst<br>
-Sylvie Essa, BI Analyst

**Stakeholder usage details:** Stakeholders would like to understand how often customers are calling in different markets with different problems. Insights will improve customer service and customer satisfaction. 

**Primary requirements:** <br>
-A chart or table measuring repeat calls by their first contact date<br>
-A chart or table exploring repeat calls by market and problem type<br>
-Charts showcasing repeat calls by week, month, and quarter<br>
-Provide insights into the types of customer issues that seem to generate more repeat calls<br>
-Explore repeat caller trends in the three different market cities<br>
-Design charts so that stakeholders can view trends by week, month, quarter, and year


## Project Requirements Document
                                                                                        
**BI Analyst:** Thandie R.

**Client/Sponsor:** <br>Google Fibre; Emma Santiage, Hiring Manager

**Purpose:** As part of an interview process, Fibre customer service team has requested a dashboard using fictional call center data. Google Fibre provides individuals and businesses with fibre optic internet. The customer service team would like to determine how often customers call again after the first inquiry. They would like to explore the trends in repeated calls to identify why customers are having to call more than once. Insights will improve the overall customer service experience. The dashboard created should provide valuable insights to the customer service team. 

**Key dependencies:**

*Team members:* <br>
-Ian ortega (BI Analysts)<br>
-Sylvie Essa (BI Analysts)

*Stakeholders:*<br>
-Emma Santiago, Hiring Manager (primary contact)<br>
-Keith Portone, Project Manager (primary contact)<br>
-Minna Rah, Lead BI Analyst<br>

*Expected deliverables:* <br>
-A chart or table measuring repeat calls by their first contact date<br>
-A chart or table exploring repeat calls by market and problem type<br>
-Charts showcasing repeat calls by week, month, and quarter<br>


**Stakeholder requirements:** (R - required, D - desired, or N - nice to have.)<br>
-R: A chart or table measuring repeat calls by their first contact date<br>
-R: A chart or table exploring repeat calls by market and problem type<br>
-D: Charts showcasing repeat calls by week, month, and quarter<br>
-R: Dashboard needs to be accessible, with large print and text-to-speech alternatives.<br>
-D: Provide insights into the types of customer issues that seem to generate more repeat calls<br>
-R: Explore repeat caller trends in the three different market cities<br>
-R: Design charts so that stakeholders can view trends by week, month, quarter, and year. 

**Success criteria:** <br>
The team’s ultimate goal is to reduce call volume by increasing customer satisfaction and improving operational optimization. The dashboard should demonstrate an understanding of this goal and provide stakeholders with insights about repeat caller volumes in different markets and the types of problems they represent. 

*Specific:* The insights provided by the dashboard should identify the characteristics of repeated calls and the quantity of such calls.

*Measurable:* Calls are to be evaluated using quantifiable metrics such as frequency and volume.

*Action-oriented:* The dashboard should provide insights that the team can use to reduce call volume and increase customer satisfaction

*Relevant:* All metrics and dimensions used should be relevant to Google Fibre and support the primary goal. 

*Time-bound:* Analyse data that spans at least one year to understand how repeat callers change over time.

**User journeys:** <br> 
-Current user experience: Customers call more than once before their inquiry is resolved.<br>
-Ideal future experience: Reduced repeated calls, and improved customer experience.<br>

**Assumptions:** <br>
To anonymize and fictionalize the data, the datasets the columns market_1, market_2, and market_3 to indicate three different city service areas the data represents.

The data also lists five problem types:<br>
-Type_1 is account management<br>
-Type_2 is technician troubleshooting<br>
-Type_3 is scheduling<br>
-Type_4 is construction<br>
-Type_5 is internet and wifi<br>

Additionally, the dataset also records repeat calls over seven day periods. The initial contact date is listed as contacts_n. The other call columns are then contacts_n_number of days since first call. For example, contacts_n_6 indicates six days since first contact.

**Compliance and privacy:** The datasets are fictional and anonymized. Therefore, there are no apparent privacy concerns.
 
**Accessibility:** Per Minna’s request, the dashboard needs to be accessible, with large print and text-to-speech alternatives.

**Roll-out plan:**<br> 
I expect to be done with the project in three weeks.<br>
*Week one:* Planning and follow up questions with Google Fibre<br>
*Week two:* Finalize SQL. Dashboard design. First review with the team.<br> 
*Week three:* Dashboard building and testing.<br>

## Strategy Document

**Sign off matrix**

| Name | Team/Role | Date  |
|-----------|------------|-------------|
| Thandie R | BI Analyst | 12/02/2024  |


**Proposer:** Emma Santiago (Hiring manager)

**Status:** [Draft] > *Under review* > Implemented | Not implemented (Highlight current status)

**Data received:** <br>
1. market_1<br>
2. market_2<br>
3. market_3<br>

[Access the combined table here](FibreUnionTable.csv)

*User Profiles* <br>
-Emma Santiage, Hiring Manager<br>
-Keith Portone, Project Manager<br>
-Minna Rah, Lead BI Analyst<br>
-Ian Ortega, BI Analyst<br>
-Sylvie Essa, BI Analyst

**Dashboard functionality**

*Reference dashboard* <br>
Build a new dashboard to explore the number of repeat callers in three different market cities, including their problem types.

*Access* <br>
Read only access will be provided to the individuals listed under user profiles. 

*Scope* <br>
Fields include date, market, problem type, contact_n and contact_n#

*Date filters and granularity* <br>
Data filters can be applied for market, problem type, day and month

Granularity: <br>
Any chart with detailed metrics should have the ability to click on that metric to view specific information.

**Metrics and charts**

*Chart 1*
| Chart feature| Request      |
|--------------|--------------|
| Chart title  | Repeat calls by first contact date   |
| Chart type  | Table   |
| Dimension(s)  | First contact date, subsequent repeat calls |
| Metric(s)  | Contact   |

*Chart 2*
| Chart feature| Request      |
|--------------|--------------|
| Chart title  | Repeat calls by market and problem type   |
| Chart type  | Column chart   |
| Dimension(s)  | Market, problem type, contact_n, contact_# |
| Metric(s)  | Contact   |

*Chart 3*
| Chart feature| Request      |
|--------------|--------------|
| Chart title  | Repeat calls by market and problem type |
| Chart type  | Table   |
| Dimension(s)  | Market, problem type |
| Metric(s)  | Contact   |

*Chart 4*
| Chart feature| Request      |
|--------------|--------------|
| Chart title  | Repeat calls by month |
| Chart type  | Column chart   |
| Dimension(s)  | Date, contact |
| Metric(s)  | Date  |

*Dashboard Mockup:*

![MockDiagram](Dashboard_mockup.png)

## Conclusion

*Insights*

Based on the insights provided, it was determined that the most common problem (resulting in 46% of repeat calls) is internet and wifi (type 5), followed by technical troubleshooting (type 2) at 43%. These two were the main problem types accounting for over 80% of repeat calls in January, February and March 2022. For all three months, each of these problems accounted for about 40% of repeat calls.

The dashboard further reveals that in Market 1, 2 and 3, internet and wifi (type 5) was the cause for 38%, 35% and 71% of the total repeat calls respectively. On the contrary, it is evident that in Market 1, 2 and 3, technical troubleshooting (type 2) was the cause of 52%, 45% and 16% of the total repeat calls respectively.

The days with highest repeat calls were Monday, Wednesday and Tuesday. 

The highest number of repeat calls were made one day after the initial call. The visuals reflect that in all three months, the number of repeat calls declined from 1st day after the initial call to the seventh day. This indicates that repeat calls after the seventh day are unlikely. This may be because the problem was finally resolved, or a frustrated customer had finally given up and terminated Google Fibre services. 

*Recommendations* <br>
1. Ensure experienced and fully trained staff are on duty from Monday to Wednesday.<br>
2. Allocate all calls related to internet and wifi as well as technical troubleshooting to experienced and fully trained staff.<br>
3. Request customer feedback after all repeat calls, providing more details on how the problem could have been resolved better. <br>
4. Update Google Fibre's website with a page for frequently asked questions regarding 'internet and wifi' and 'technical troubleshooting'. Provide the link to all customers monthly when emailing their bill.

[Access the dashboard here](Google_Fibre_Dashboard.pbix)
