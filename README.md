# Replication materials for "Anti-Immigrant Rhetoric and ICE Reporting Interest: Evidence from a Large-Scale Study of Web Search Data"
This is code to reproduce the results and figures in "Anti-Immigrant Rhetoric and ICE Reporting Interest: Evidence from a Large-Scale Study of Web Search Data", by Masha Krupenkin, Shawndra Hill, and David Rothschild, Published online by Cambridge University Press: 25 January 2024.

## Requirements
R, with the following packages: tidyverse, gridExtra, scales, broom, lsr, knitr, and lsmeans.

## Running the code
To reproduce results, simply run the Makefile by typing make on the command line, or open and run the paper_replication_final.Rmd file.

## Files

**For Replication**
  
paper_replication_final.Rmd: Main analysis code in Rmarkdown format
paper_replication_final.html: Rendered output from running analysis.Rmd containing all results and figures in the paper, this can also be viewed here: https://rpubs.com/ubaydulsami/paper-replication
from_google_trends/google_3_terms_trend_data_04_20.csv: contains our obtained Google search data for reporting, crime, and welfare topics from 2024
from_replication_files/google_trends_crime.csv: contains the original Google search data for crime used in the paper
from_replication_files/google_trends_report.csv: contains the original Google search data for reporting used in the paper
from_replication_files/google_trends_welfare.csv: contains the original google search data for welfare used in the paper
from_replication_files/gt_report_daily.csv: contains daily google search data for reporting used for Table 4
from_replication_files/gtopic_model_lite.Rdata: contains the topic model used for figures 3-4 and table 4
  
**For Extended Research Question:**
  
extended_research/ice_reportings.csv: This file contains the number of undocumented immigrants arrested from 2014 t0 2020

# Brief Details about the research paper and our extended research question:

## About Paper:
This paper studies whether media cues can motivate interest in reporting suspected unauthorized immigrants to Immigration and Customs Enforcement (ICE). Using web search data and automated content analysis of cable news transcripts, they examined the role of media coverage on searches for how to report immigrants to ICE and searches about immigrant crime and welfare dependency. They demand of finding significant and persistent increases in news segments on crime by after Trump’s inauguration, accompanied by a sharp increase in searches for how to report immigrants. They also claim to find a strong association between daily reporting searches and immigration and crime coverage. Using searches during broadcasts of presidential speeches, they isolated the specific effect of anti-immigrant media coverage on searches for how to report immigrants to ICE. The findings indicate that the media’s choices regarding the coverage of immigrants can have a strong impact on the public’s interest in behavior that directly harms immigrants.

## Our Replication:
Our mission was to replicate the results mentioned in the paper using our own scratched data from Google Trends and Verify the results. In order to do that we have downloaded search trend data form https://trends.google.com/trends/ using the below search criteria:

To measure Immigration reporting searches, we pulled searches with the following string: “report immigrant+report immigration+report illegals+report illegal alien+report to ice”. 

To measure immigration and crime searches, we pulled searches with the following string: “immigrant crime+immigrant criminal+immigrant murder+immigrant kill”. 

To measure Immigration and welfare searches, we pulled searches with the following string: “immigrant welfare+immigrant cost+immigrant benefits”.

After obtaining the data from Google Trends we also used some files from paper resources (which can be found in the 'from_replication_files' folder). we used all these data to perform the same kind of analysis that the paper did and the result was almost similar to the paper's findings so we concluded the paper's observations were valid.

**Since we replicated and validated the research paper's results we thought of any extension that we could add to the paper's findings**

## Extended Research:

One of the Hypotheses for the paper was "People will have more interest in reporting immigrants when they believe the government supports deportation." that means there is more interest in immigrant denunciation when people believe that reporting will lead to some action by the government. In finding the paper suggests that "Reporting searches (search of "how to report immigrant") increased sharply after Trump took office and that media reporting on Trump’s immigration policies during his administration (but not during the Trump campaign) is associated with more reporting searches"

### Our Finding:

So for research, we decided to look at data from Law enforcement to see if there is a change in the number of arrests of immigrants during the Trump period. We used immigrant arrest data from "The office of homeland Security" for our observation.

### Our Process:

We looked into the immigrant arrest data from 3 points of view,

1)  Total number of immigrant arrests from January 2014 to December 2019

2)  Number of Immigrants arrested for committing a crime

3)  Number of Immigrants arrested even without committing a crime

### Observation Result

**1) For Total number of arrest & for immigrant arrest for criminal activity:**

-   There are higher amounts of arrests pre-campaign (highest),

-   a lower number during the campaign (lowest),

-   then a spike in numbers post-inauguration but not as high as Pre-campaign (2nd highest)

**2) For the number of arrests without criminal activity:** - The highest number of arrests occurred during the "post-inauguration" of Trump. These numbers are way higher than pre-campaign or during the campaign.

*This suggests that when President Trump openly gave an anti-immigrant speech people's tendency to report undocumented immigrants increased significantly. That means people were reporting undocumented immigrants even when they were not doing any harm to anyone. This finding of ours validates the paper's statement that because the government is supporting anti-immigrant activity people are more likely to report undocumented immigrants (even without a crime)*
