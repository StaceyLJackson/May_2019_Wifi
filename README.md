May_2019_Wifi

Evaluating techniques for wifi locationing

PROJECT GOAL

Investigate the feasibility of using "wifi fingerprinting" to determine a person's location in indoor spaces by producing different predictive models and assessing their accuracy.

SUPPLIED DATA
The supplied data is for three buildings with either four or five floors. There are 21,049 sampled points: 19,938 for training and 1,111 for validation. 

Indoor Locationing Data Set (Training and Validation Sets): http://archive.ics.uci.edu/ml/datasets/UJIIndoorLoc

TECHNICAL APPROACH

LANGUAGE USED: R

1. INITIAL EXPLORATION
Readings from 80 WAPs (wireless access points) were removed due to a range of reasons including they weren't receiving a signal or had a low variance. Irrelevant variables were also removed: relative position, Space Id and the timestamp. Data collected by a defective phone was also removed.

2. WATERFALL APPROACH
The modelling followed the waterfall approach - first predicting the building and then the floor, longitude and final the latitude.

3.MODELLING
Random Forest and GBM models were used as they are part of the H2O package, which is fast.

4. CONCLUSIONS
The best results were a combination of Random Forest and GBM models depending on the building and variable being predicted.
The final predictions had a MAE rate of 11m for building 0, 17m for building 1 and 14m for building 2.