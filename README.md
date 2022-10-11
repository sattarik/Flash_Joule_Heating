# FJH_ML
# original author: Jacob Bekham: jacobbeckham@rice.edu
# modified by Kianoosh Sattari
Code and data available for the prediction of flash graphene crystallinity from flash Joule heating parameters. 

The file "RegressionAndPD" was used to compile performance metrics and analyses for the various models trained to predict GY. This file uses data from the dataset contained in "FJH_ML_Final.csv." 

The file "publicationCode.R" contains the script used to generate new suggested datapoints using mlrMBO learners. The script "CalculatingPDMBO" shows the PD of the parameters involved in this process. These scripts use variations of the same dataset, with the PD dataset using a transformed version that more accruately represents the nature of the parameters involved. For instance, when this study began, it was not known whether the path dependence of pre-treatment would be important to consider, so we merely asked the MBO algorithm to determine the best pretreatment from a variety of options presented. In the analysis script, once we had a better idea of how pre-treatment affected GY, pre-treatment was presented as teh cumulative voltage applied and the highest voltage treatment. This is why there are multiple files containing different forms of the MBO dataset, which are used by different analysis scripts. 

# improvment:
1) Not use of features from the middle of experiments as input for developing forward model.
2) First, develping models for predicting in the middle features, then use the predicted 
proxy properties to predit the final Graphene Yield.
3) develping MOBO using develped forward model as constraint. 
