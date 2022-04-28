# New-York-Property-Fraud-Detection

This project employed unsupervised machine learning model to detect fraud and anomaly in New York Real Estate Property Valuation and Assessment database. The data is obtained from NYC Open Data and provided by Department of Finance.(https://data.cityofnewyork.us/Housing-Development/Property-Valuation-and-Assessment-Data/rgy2-tti8). It provides address, owner, property characteristics, assessed tax values, etc. with over 1 million records and 32 fields.

The following summarizes the steps entailed to analyze the data and build the fraud detection model:

1. **Exploratory Data Analysis:** We first did preliminary quantitative analysis that explores the basic characteristics of ~1M rows of data to get familiar with it and generated a data quality report.
2. **Data Cleaning**: This involved cleaning the data and imputing those records which have missing values and zero values.
3. **Feature Engineering**: We built expert variables that look for the fraud mode and standardized the data. 
4. **Dimensionality Reduction**: We employed the Principal Component Analysis (PCA) to remove correlations and reduce dimensions in the data.
5. **Calculating Fraud Scores**: The two approaches used to compute the fraud scores are described as follows:
- Score 1: Combine the zscores with a heuristic algorithm
- Score 2: Autoencoder on the z scaled PCs, and the fraud score is the reconstruction error.
- Final Score: Take the average of the rank orders obtained from the two methods described above.
- We used Euclidean distance in this case. The scores from the above methods were used individually to rank order the records in order of their likelihood of being fraudulent or anomalous. 
6. **Investigating anomolies:** We ranked the records by final scores and investigated the top anomalous records in the NY property dataset. These records were analyzed in great detail to elicit insightful information regarding the anomalous records and provide recommendations for future work.




