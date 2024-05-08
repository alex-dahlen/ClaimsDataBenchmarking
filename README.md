# Claims Data Benchmarking
Python code to reproduce the analysis in "Benchmarking Healthcare Claims Data".  While the MarketScan claims data and the SID reference data are both proprietary and cannot be shared, this repository contains all of the code run used to clean and explore the data, conduct the analysis, and produce the visualizations.

There are 3 python files contained in this repository:
1) 'main_analysis_MarketScan_vs_SID_2019.ipynb'. This python notebook imports and cleans the SID and Marketscan datasets, and conducts the primary statistical models in the paper.  For each of the top 250 inpatient procedures, we: (A) compute the rates in both datasets and the bias; and (B) compute the strength of the association between each procedure and our two measures of SDOH.  Finally, we compute the procedure-level association between these two.
2) 'defining_SES_variable_and_rolling_up_to_MSA_level.ipynb'.  This python notebook reads in census data, rolls it up to the zip code- and MSA-levels, and uses PCA to dimentionally reduce to a single SDOH indicator variable. 
3) 'sensitivity_analysis_restricting_target_cohort.ipynb'.  This python notebook repeats the above analysis for two new target populations.  The original analysis used a target population of all Americans 18-64 living in CA, IA, MA, MD, and NJ in 2019; the two addional target populations we consider here are (A) restricting to just the subset that are insured; and (B) further restricting to the subset that are commercially insured.

Feel free to direct any questions about the above to: ad7203 AT nyu.edu.
