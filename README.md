# Cryptocurrency Analysis

## Project Overview
Performed data analysis on cryptocurrency data for the Advisory Services Team at Accountability Accounting, a prominent investment bank, to offer a new cryptocurrency investment portfolio for its customers.

## Resources
- Data Source: Crypto_data.csv
- Software: Jupyter Notebook, sklearn, hvplot, pandas

## Summary

### 1) Preprocessing the Data for PCA
 - First, the dataframe was created with the raw 'Crypto_data' csv file.
 
 ![originalDF](https://github.com/frlinh/cryptocurrencies/blob/ab1c550e654abc055c1ae1e515cf101fd7d11d91/Resources/originalDataframe.png)
 
 - Next, the dataset was filtered to only traded cryptocurrencies, mined coins, and no 'Null Values'.
 
 ![dropNADF](https://github.com/frlinh/cryptocurrencies/blob/ab1c550e654abc055c1ae1e515cf101fd7d11d91/Resources/dropNADataframe.png)

 - Furthermore, the index column was removed, the 'unnamed' column was renamed to 'CryptoCode', and the 'CoinName' was dropped from the dataframe.
 
 ![cleanedDF](https://github.com/frlinh/cryptocurrencies/blob/20b89b2d60d686ba752778c82b8b4d5fafa05040/Resources/cleanedwoCoinNameDataframe.png)
 
### 2) Reducing the Data Dimensions using PCA
- Used 'get_dummies' to create new variables for text features on 'Algorithm' and 'ProofType'.
- Used PCA to reduce the dimension to three principal components
- Created a new dataframe with three principal components

![3PCs](https://github.com/frlinh/cryptocurrencies/blob/f244dd26a46506c0e1d16021aaf14d86d39fc757/Resources/3PCs.png)

### 3) Clustering Cryptocurrencies Using K-means
- Calculate the inertia for the range of K values and created the elbow curve plot

![elbowCurve](https://github.com/frlinh/cryptocurrencies/blob/ab1c550e654abc055c1ae1e515cf101fd7d11d91/Resources/ElbowCurve.png)

### 4) Visualizing Cryptocurrencies Results
- Created a 3D-Scatter plot with PCA data and clustered dataframe.

![3D-Scatter](https://github.com/frlinh/cryptocurrencies/blob/ab1c550e654abc055c1ae1e515cf101fd7d11d91/Resources/3D-ScatterFig.png)

- Created a new table with tradable cryptocurrencies.

![tradableCryptoTable](https://github.com/frlinh/cryptocurrencies/blob/ab1c550e654abc055c1ae1e515cf101fd7d11d91/Resources/tradableCryptosFig.png)

- Finally, a hvplot scatter plot was created using x='totalcoinsmined' and y='totalcoinssupply'.
![hvplot](https://github.com/frlinh/cryptocurrencies/blob/ab1c550e654abc055c1ae1e515cf101fd7d11d91/Resources/hvplotScatterFig.png)
