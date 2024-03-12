# Investigating Causal Impacts on Incident Duration

The objective of this project is to detect the presence (or non-presence) of a causal impact of the time delay between a ServiceNow incident ticket being opened and its subsquent access (i.e. for initial triage) on the overall resolution time. This was accomplished using uber's causalml package.

Note: This notebook was created in Google Colab for a quick start given package conflicts with causalml as at Feb 2024. Creating a local virtual environment is another alternative to circumvent these conflicts. 

## Context & Business Impact
ServiceNow is a cloud based workflow management system which can, among other features, be used for managing IT incidents. 

Understanding the causal relationship between triage delay and resolution time can inform process improvements in incident management. Specifically, it can help determine whether targeted strategies to reduce initial triage times are worth the organizational resources to implement them.

## Process
The notebook is divided into the sequential tasks undertaken in the project including: preprocessing, feature engineering, exploratory data analysis, deriving average treatment effects, and assessing feature importances. 

## Findings Summary
Across various models and upon test sets, the average treatment effect of first access being over 12 hrs from ticket open was between a 30 to 40 hrs increase in time to resolve.

## Data Source
The [enriched event log](https://archive.ics.uci.edu/dataset/498/incident+management+process+enriched+event+log) used for this project was procured from UC Irvine's Machine Learning Repository.
