# MGPM
Miami Glioma Prediction Map

Welcome to the MGPM code. To use the attached code, follow these instructions: 
-All source code and data are stored on GDrive. Must run code from a non-academic Google account. 
-Run code through Google Colab for integration of source data

1) To process data from scratch:
-Once connected, run the "Load Packages" tab. This loads dependencies
-Next, run the "Filename + Data" tab. This should already have filename = 'wbf_recurrence', which reflects our most relevant calculations
-Next, run "Feature + Classifier Setup". This prepares the data for ML Classifier training and testing.

2) To train new models: 
-First complete the above instructions
-You can then go through each model and train the model, gridsearch parameters, and calculate AUC
-The bottom few tabs below each SK learn model reflect calculations for previous publication; can be ignored for these purposes

3) *If you want to skip to the unsupervised clustering, you can **skip step 2!!**
-Simply run the "Intro Code" to get started. Here, you can adjust the parameters for the clustering in the second block
-The GBoost supervised classifier is found here:
'''
with open("/content/drive/Shareddrives/MR_Spectroscopy/wbf_for_cluster_backup.pkl", "rb") as f:
    wbf_cohort = pickle.load(f)
'''
-Under "Main Code", ignore "Old DB" and run "New DB" for the clustering of all 16 patients
-Below is a sandbox of current analysis ideas including overlay onto MRI imaging and other various statistics. Active as of 12/2024. 
