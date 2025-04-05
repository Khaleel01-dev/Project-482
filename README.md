# Nationwide Crime Prediction and Prevention in Canada  
**A Decision Intelligence Approach to Understanding SDG 16**

*By:Khaleel Mohammed*

## Table of Contents
1. [Introduction](#introduction)
2. [Research Objective](#research-objective)
3. [Milestone 2: Exploratory Data Analysis with Tableau](#milestone-2-exploratory-data-analysis-with-tableau)
   - [KPI 1: Crime Severity Index by Province (1998–2023)](#kpi-1-crime-severity-index-by-province-19982023)
   - [KPI 2: Homicide Trends in Canada](#kpi-2-homicide-trends-in-canada)
   - [KPI 3: Hate Crime Trends in Canada](#kpi-3-hate-crime-trends-in-canada)
   - [KPI 4: Trends in Robbery, Motor Vehicle Theft, and Breaking & Entering (1998–2023)](#kpi-4-trends-in-robbery-motor-vehicle-theft-and-breaking--entering-19982023)
   - [KPI 5: Sentencing Trends of Young Offenders (Ages 18–24) in Canada (2015–2023)](#kpi-5-sentencing-trends-of-young-offenders-ages-18-24-in-canada-20152023)
   - [Tableau Limitations](#tableau-limitations)
4. [Milestone 3: Correlation & Causal Inference Analysis](#milestone-3-correlation--causal-inference-analysis)
   - [Descriptive Statistics](#descriptive-statistics)
   - [Correlation Analysis](#correlation-analysis)
   - [Causal Model (DAG)](#causal-model-dag)
   - [Interpretation of Findings](#interpretation-of-findings)
   - [Limitations](#limitations)
5. [Conclusion & Future Work](#conclusion--future-work)
6. [References](#references)


## Introduction 
This project addresses the challenge of crime prevention and prediction in Canada through the lens of **Sustainable Development Goal 16: Peace, Justice & Strong Institutions**. By utilizing open crime data from various provinces and integrating decision intelligence tools such as Python and Tableau, we aim to predict crime trends, identify high-risk areas, and propose actionable interventions for improving public safety. Our analysis blends traditional statistical techniques with machine learning methods to forecast crime patterns, uncover correlations, and assess the effectiveness of potential crime prevention strategies.

[Read detailed background information here](Background.md)

## Research Objective
The main goal is to understand crime trends across Canada using five key performance indicators (KPIs). We combine **visual dashboards** (Tableau) with **quantitative methods** (correlation and causal inference) to:
- Identify high-risk crime areas,
- Predict future crime patterns,
- Propose data-driven interventions.


## Milestone 2: Exploratory Data Analysis with Tableau

During Milestone 2, I developed **Tableau dashboards** for five KPIs:

## Key Performance Indicators (KPIs)

### 1. Crime Severity Index by Province (1998-2023)

The Crime Severity Index (CSI) aggregates the severity of crimes across Canadian provinces from 1998 to 2023. This analysis highlights Ontario and British Columbia as the provinces with the highest CSI values over this period, indicating a higher occurrence of severe crimes.

![Crime Severity Index](/Images/Crime%20Severity%20Index.png)

### Insights:
- Ontario and British Columbia have the highest aggregated CSI values.
- Provinces with lower CSI values could have better crime control measures in place or lower crime rates.


### 2. Homicide Trends in Canada

**Dashboard: Homicide Trends in Canada (Total vs. Rate per 100,000)**  
This dashboard presents a **comprehensive analysis of homicide trends in Canada**, comparing total homicides across all provinces and homicide rates per 100,000 people in Atlantic provinces.  

![Homicide Dashboard](Images/Homicide%20Trends%20in%20Canada.png)  

### **Key Insights**  
**Total Homicides in Canada (2001-2023)**  
- Homicides have been **increasing** across most provinces.  
- **Ontario, British Columbia, and Alberta** have the highest homicide counts.  

**Homicide Rate per 100,000 in Atlantic Provinces (2004-2023)**  
- **Nova Scotia** consistently has the **highest homicide rate** in the region.  
- The homicide rate varies significantly despite similar geographic and demographic conditions.  



### 3. Hate Crime Trends in Canada

**Dashboard: Hate Crime Trends in Canada (Total vs. Rate per 100,000)**
This dashboard presents an overview of hate crime trends in Canada by analyzing both total cases and the rate per 100,000 people.

![Hate Crime Dashboard](Images/Hate%20Crime%20Trends%20in%20Canada.png)

### Key Insights

- **Total Hate Crimes in Canada (2014-2023)**:
  - The highest number of reported hate crimes are in **Ontario, Quebec, British Columbia, Alberta, and Nova Scotia**.
  - Ontario has the most reported cases due to its large population and urban centers.
  - Hate crimes have increased over the years, indicating a growing concern.

- **Average Hate Crime Rate per 100,000 (2014-2023)**:
  - **Nunavut has the highest hate crime rate per 100,000**, despite having fewer total cases.
  - The Atlantic provinces have relatively lower total cases but noticeable variations in crime rates.
  - A province's total number of hate crimes does not always reflect its impact when adjusted for population size.

### 4. Trends in Robbery, Motor Vehicle Theft, and Breaking & Entering (1998-2023)

**Forecast of Crime Categories in Canada**
This visualization presents a forecast of three major property-related crimes—**Robbery, Motor Vehicle Theft, and Breaking & Entering**—across Canada from **1998 to 2023**.

![Crime Forecast](Images/Forecast%20Robbery,Motor%20theft,%20Breaking%20and%20Entering.png)

### Key Insights

- **Robbery** and **Breaking & Entering** show a **declining trend** over the years, suggesting improvements in security measures, law enforcement, and crime prevention strategies.
- **Motor Vehicle Theft**, however, exhibits an **increasing trend**, indicating a growing concern in vehicle-related crimes.
- The forecast suggests that while traditional property crimes are decreasing, emerging factors may be driving the rise in motor vehicle theft.


### 5. Sentencing Trends of Young Offenders (Ages 18-24) in Canada (2015-2023)

**Sentencing Distribution Over Time**
This visualization showcases the **sentencing distribution of youth offenders (aged 18-24)** in Canada between **2015 and 2023**, highlighting how the allocation of sentences has evolved.

![Youth Sentencing Distribution](Images/Sentencing%20Distribution%20of%20Young%20Offenders%20%20(18-24)%20Over%20Time.png)

### Key Insights

- **Custody sentences have shown a decreasing trend**, indicating a shift towards alternative rehabilitation-focused approaches rather than incarceration.
- **Probation and Conditional Sentences have increased**, suggesting a preference for supervised reintegration and rehabilitation over strict punitive measures.
- **Fine and Other Sentences have remained relatively stable** over the years.
- This shift may reflect **policy changes** favoring rehabilitation over incarceration, emphasizing alternative sentencing methods for young offenders.

#### Tableau Limitations
While Tableau dashboards effectively showcase trends, they do not provide advanced statistical or causal insights. This led to **Milestone 3**, where we used Python for correlation and causal inference to further investigate these KPIs.

---

## Milestone 3: Correlation & Causal Inference Analysis

### Descriptive Statistics
Below are the descriptive statistics for our KPIs (2019–2022):

### Correlation Analysis
A correlation heatmap was generated to see how these KPIs move together from 2019–2022. 

![Correlation Matrix of KPIs](Images/Correlation%20Matrixof%20KPIs.png)

Key findings include:
- **High Positive Correlation:** CSI and PropertyCrimeTrend (0.92).
- **Strong Negative Correlations:** HomicideRate and HateCrimeCount with YoungOffenderSentencing.
- **Weak Correlation:** CSI and YoungOffenderSentencing.

**Note:** Correlation alone does not establish causation, especially with only 4 data points.

### Causal Model (DAG)
Based on theoretical and qualitative insights, we constructed a Directed Acyclic Graph (DAG):
- **HomicideRate, HateCrimeCount, and PropertyCrimeTrend** → CSI
- **CSI** → YoungOffenderSentencing
- Confounders also directly affect YoungOffenderSentencing.

![Causal Inference Diagram](Images/Causal%20Inference.png)


Due to the limited sample size (N=4), regression-based causal estimates were unstable. This highlights the exploratory nature of the analysis.

### Interpretation of Findings
- **Interdependencies:** The correlation heatmap reveals several relationships (e.g., CSI ↔ PropertyCrimeTrend, HateCrimeCount ↔ HomicideRate).
- **Potential Causation:** The DAG offers a framework for how these KPIs might influence each other.
- **Limitations:** With only four observations (2019–2022), the regression results must be treated as highly tentative. A single outlier year can drastically affect the results.

### Limitations
1. **Small Sample Size:** Only four annual observations severely limit the reliability of statistical and causal estimates.
2. **Exploratory Analysis:** The negative effect of CSI on YoungOffenderSentencing is likely not robust given the limited data.
3. **Data Sensitivity:** Outliers can drastically alter correlation and regression results.
4. **Future Work:** Including more years or panel data across provinces could strengthen the analysis.

---

## Conclusion & Future Work
- **Milestone 2** gave us broad insights through **Tableau** dashboards, revealing crime patterns and sentencing trends but lacking deeper statistical inference.
- **Milestone 3** extended the analysis with **Python**-based correlation and causal inference, uncovering potential relationships but highlighting the severe constraints of a small dataset.
- **Next Steps:** Acquire more data points (either by extending the time frame or using provincial panel data) to produce more robust causal estimates and reduce the instability seen in the current analysis.

---

## References
- [Statistics Canada](https://www.statcan.gc.ca/)  
- [Tableau Public Documentation](https://public.tableau.com/en-us/s/resources)  
- [DoWhy Causal Inference Library](https://github.com/py-why/dowhy)  
- Additional academic papers and sources relevant to SDG 16 and crime analysis.
