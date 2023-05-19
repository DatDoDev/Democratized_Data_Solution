# 🌁  Bridging the Gap between Citizens and Local Governments: A Democratized Data Solution
A visualization project aims to build trust between regular citizen and government. 

## Quick Links 
[:bar_chart: SEE VISUALIZATION HERE ](https://public.tableau.com/app/profile/binh.vu5742/viz/Visualization_16835996323470/MainDashboard)

[:video_camera: SEE VIDEO PRESENTATION HERE](https://www.youtube.com/watch?v=EReiQd1YQcU)

[:bookmark_tabs: SEE POSTER HERE](https://drive.google.com/file/d/1Xrp-v-Ypt75Cg9kjDuZT1scfmFaTNaCP/view?usp=share_link) or above

[:open_file_folder: DOWNLOAD FILES HERE](https://drive.google.com/drive/folders/1nTQe0mLxE-BWR_injImy1uHtF8uRVRTa?usp=share_link)



## 🔨 INSTALLATION

For the Tableau visualization, please use Tableau 2022.4 if running locally. Alternatively, the Tableau visualization can be accessed via Tableau Public at this link: https://public.tableau.com/app/profile/binh.vu5742/viz/Visualization_16835996323470/MainDashboard

If using the Tableau Public version, no further installations or dependencies are required and all data should be pre-connected. For the best experience, we recommend using a larger (e.g., desktop) computer screen to maximum display as the map renders all states and zip codes in the United States.


## 📁 CONTENTS IN FILES

* DESCRIPTION
* PACKAGE STRUCTURE
* INSTALLATION
* EXECUTION


## DESCRIPTION

This package contains a Tableau package and link to a Tableau Public dashboard. Our visualization was developed in Tableau and focuses primarily on displaying geospatial data and various overlaid attributes, specifically those related to indicators of financial need (e.g., income and unemployment levels) and federal award data. The two data sets include: (a) IRS - Individual Income Tax Statistics - ZIP Code Data and (b) USASpending.gov - Financial Assistance - ZIP Code Data. The income dataset gives total income, taxes paid, unemployment payment, net investment, and real estate info based on zip code. The award dataset shows how much the US government has given in financial assistance to each zip code.

Using these datasets, we created clusters using K-means and output them to a Tableau visualization. The end result is a tool that enables a user to explore trends in the the clustering algorithm provided an intuitive way to explore trends in the zip code data. By design, it does not inherently tell a user which clusters actually needed aid. The interactivity of the visualization allows users to identify familiar zip codes, compare them to unfamiliar zip codes, and see what attributes made them similar to be included in the same cluster. 


## 📚 PACKAGE STRUCTURE

### 📟 CODE:
- award_data_code.py
 This python scrypt is used to clean up raw data of Award Data Set as part of the data preprocessing step in the project.

- income_data_import_code.ipynb
 This Jupyter notebook is used to create a K-means machine learning model, perform clustering, and clean up Income Data set as part of the project.

- Visualization.twbx
 This file contains the main functionality of the application, which is the visualization component.

### 📄 DOC:
- poster_Democratized_Data_Solution.pdf
 This is the final version of the poject's poster.

- Democratized_Data_Solution.pdf
 This is the final report for the project



## 🎉 EXECUTION 🎊

The visualization focuses on one dashboard that features a map of the United States. The map is partitioned based on states and zip codes. The user can toggle between two views: “Clusters Only” and “Clusters + Awards Merged”. Each zip code will have a color coding based on the cluster assigned by the K-means algorithm. The K-means algorithm generated 2-20 clusters, and in both views, the user can choose how many clusters they want to explore in the “Select # of Clusters” option. There are accompanying bar graphs which inform about 1) number of zip codes per cluster,  2) award amount (thousands) per cluster, and 3) unemployment amount(thousands) per cluster. To show a bigger picture of the unemployment data, we also created a bar graph to display the unemployment amounts for all zip codes. Additionally, users can select a state to focus on a specific state’s zip codes or view the entire United States as a whole. If the user chooses to only view certain cluster assignments (i.e. cluster 2 in California), they can do so by selecting the state and changing the “Cluster Assignment”. 

The “Clusters” Only view displays a color coded map of the United States based on its cluster assignment. The “Clusters + Awards” view has an additional layer of information about the award amounts per zip code. The awards amount is represented as a circle overlaid on top of the cluster assignments. The larger the circle, the more the government has awarded aid to this zip code. The circles are also color coordinated, with yellow representing smaller award amounts and red representing larger amounts. In this view, when the user hovers over the circles or zip codes, they will find additional summary statistics such as total income, total tax paid, total amount in real estate, total amount in net investments, etc.

The clustering algorithm provides the user with an intuitive way to explore trends in the zip code data. By design, it does not inherently tell a user which clusters actually needed aid. The interactivity of the visualization allows the user to identify familiar zip codes, compare them to unfamiliar zip codes, and see what attributes made them similar to be included in the same cluster. Areas that were previously identified by federal or state governments as in high need for aid could be used as a baseline to give clusters a meaning. The cluster for these baseline areas could then be filtered to inspect other zip codes that shared the same cluster.

