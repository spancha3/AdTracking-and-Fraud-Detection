1. train_sample.csv is our input data for this model
2. FeatureDriver.R reads this file and then invokes methods from FeatureGeneration.R to generate new features after grouping the data per app.
3. The output file thus created is named FeatureEngineeredData.csv (this is unsampled data)
4. Use this file as input to run the sampling codes: SmoteSampling.R and RoseSampling.R are two separate processes which further sample the data into Smote_Sampled.csv and Rose_Sampled_Data.csv. 
5. The Rose_n_SmoteModeling.R file has two processes who respectively apply the various prediction algorithms on the sampled data generated in the above step.
6. DataModeling.R contains processes which apply the prediction algorithms on the unsampled data created in step 3
