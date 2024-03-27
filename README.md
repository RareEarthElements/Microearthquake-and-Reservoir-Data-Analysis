# Microearthquake-and-Reservoir-Data-Analysis
Geoscience Data Analysis 

# Business Problem
This notebook contains descriptive data analysis and visualization of microearthquake (MEQ) data and reservoir engineering operational parameters from a particular geothermal field. Operational parameters such as injection rate, wellhead pressure, total injection quantity, well location, and geologic and geomechanical characteristics are known to affect the rate of induced earthquakes (He et al., 2020; Hofmann et al., 2018), therefore the collaborative analysis of induced seismicity and operational parameter shall be carried out.

The notebook includes a quality check of the microearthquake catalogue (MEQ) from December 2019 to October 2023, spatial and temporal analysis of the MEQ catalogue data, calculation of the total number of microearthquake events over time, analysis of operational reservoir data, and the joint analysis of microseismicity and reservoir operational parameters.

The goal of this project is to performing MEQ catalogue data quality control, depicting patterns hidden within the seismicity data, as well as understand injection-induced microseismicity in the geothermal system using integrated data analysis of MEQ and reservoir operational parameter.

# Data Analytics Summary
### 1. MEQ Catalogue Quality ###
   - In the MEQ catalogue records from December 2019-October 2023, missing values are still dominant in the local and moment magnitude features, but the missing values are filled using the KNN imputation method.  
   - The data contained in the catalogue are categorized as microseismic event as their magnitude are less than 3.
   - MEQ events majorly have an RMS error range in the range of 0 - 0.05, this indicates that this MEQ catalog is reliable.
   
### 2. MEQ Data Analysis ###
   - A total of 1534 MEQ events were detected over a period of ±4 years.  
   - This dataset is comprised of 58.7% of events that have been processed up to the WCC stage, and shows 2 clusters, one of which clearly shows an ENE-WSW orientation.
   - The majority of MEQ events occur at shallow depths (-2000 - 0 m) from late 2019 until the fourth quarter of 2023.
   - Remarkable rises in microseismic activity occur in the first five months of 2020 and during 2023. However, there is less microseismicity in the intervening period.
   
### 3. Operational Reservoir Parameter Data Analysis ###
   - ML E1 was identified as the well with the highest average of injection temperature and WHP.
   - Compared to the other wells, ML D2 was the highest in average injection rate and the highest in average FCV opening percentage.
   
### 4. Integrated MEQ and Reservoir Data Analysis ###
   - The temperature of reinjected fluids and the amount of reinjected fluids follow a similar trend and tend to correlate positively.
   - By plotting the injection rate and injection temperature of all wells against the total daily MEQ events from January 2021 to May 2023, it is not very clear that there is a relationship between these two reservoir operating parameters and increased microseismic events.
   - According to the visualization of WHP against the total daily MEQ events, the intensity of the microseismicity started to increase after the first quarter of 2022 and increased dramatically in the first quarter of 2023. This is inline with ML D1 and ML E2 wellhead pressures being fully minimalized, while ML E1 was increased and ML D2 reduced and maintained in the 7-17 barg range.

# Business Implementation

### 1. Establishing Discrete Fracture Network (DFN) for numerical simulation ###

The effective and confirmatory numerical simulation technique associated with the discrete fracture network constructed based on microseismicity data will help to estimate the power output for specific years based on the P10/P50/P90 scenario and describe the geothermal resource potential in MWe. 

### 2. Identifying fluid path ###

Induced seismicity recorded due to fault reactivation that produces a swarm of fractures, will show the orientation of the fractures. For example, in our cases, a cluster of microseismic events described in ENE-WSW, this cluster could be aligned with structural trends, indicating that the events could be correlated with these structures. If so, this structure is favourable for geothermal fluid flow.

### 3. Assisting well targeting ###

The information from microseismicity would help to determine the permeable zone of the geothermal area, as well as the reservoir connectivity, which could help to locate injection and production wells.

# Recommendation
   1. Combined microseismic analysis with reservoir operational data will be more comprehensive when both datasets have the same data availability date. In this case, MEQ and reservoir data are only synchronised from 1 January 2021 to 29 May 2023. If possible, reservoir operational data should be available from December 2019 to December 2020 and from 30 May 2023 to the present.

   2. In order to identify which features influence the occurrence of daily microseismic events, the application of machine learning methods with tree-based models for feature-of-importance analysis can be helpful.
   
   3. Data-driven modelling can be performed, using (a) lagged linear regression of seismicity rate as a function of well injection rates; and (b) systematic extraction of injection time series features, which were then evaluated for associations with seismicity. Using these models, we were able to determine which wells had the highest correlation with microseismicity.
