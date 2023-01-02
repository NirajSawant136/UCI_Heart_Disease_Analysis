Group Members ->
Niraj Sawant | nxs210168
Swaroop Ranganath | sxr220019

The folder named 'data' contains the original data from UCI - https://archive.ics.uci.edu/ml/datasets/heart+disease

- heart-disease.names -> contains information about the datasets from the owners of the data

- The data is collected separately from 4 different regions ->
	
	- Cleveland
	- Hungary
	- Switzerland
	- Long Beach 

- you may find some files named processed.cleveland.data and some as cleveland.data. Note that the original data was corrupted and remaining data was processed into the processed files

- the csv files named 'ProcessedClevelandData.csv' and such are data that we generated after doing some basic preprocessing for missing values in the processed.data files.

the folder 'Data_Processing' contains python notebooks where we did our initial preprocessing.

Finally the notebook named 'experiments' is where we train and test our models on different regions 

- def learn(region1, region2, model, show_plots) -> function to train your model on one region and test on another
	
	region1 -> region whose data who you want to train on

	region2 -> region on which you want to test the trained model

	model -> model of choice 

			RF  - Random Forest Classifier
			SVM - Linear SVM
			KNN - K-Nearest Neighbours
			NB - Gaussian Naive Bayes
			XGB - XGBoost

	show_plots -> set True if you want to see metric graphs. Default = True


- test_on_rest(region, model) -> function to train your model on one region and test on all regions

	region -> region whose data who you want to train on

	model -> model of choice 

			RF  - Random Forest Classifier
			SVM - Linear SVM
			KNN - K-Nearest Neighbours
			NB - Gaussian Naive Bayes
			XGB - XGBoost


- Eg. to train Cleveland data using Random Forest and test on Hungary use -> learn('Cleveland', 'Hungary', 'RF', True)