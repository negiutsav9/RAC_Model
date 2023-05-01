# Predicting the properties of Recycled Aggregate Concrete under Axisymmetric and True Triaxial Load

### Source : Li, Y., Zhang, X., Zhang, Y., & Song, S. (2021). Prediction of triaxial behavior of recycled aggregate concrete using multivariable regression and artificial neural network techniques. Construction and Building Materials, 298, 123846. https://doi.org/10.1016/j.conbuildmat.2021.123846

This repository consist of files which can be used to refer the ways of training a machine learning model using MAST-ML and upload the model to the cloud foundry.

## Steps to follow

1. Run the jupyter notebook paperModel_MNR.ipynb to generate model weights, preprocessed data and calibration file for each model
2. For each model, create a directory with its model.pkl, preprocessor.pkl, calibration_file.csv, requirements.txt and X_train.csv files (refer Container files)
3. Run Repo2Docker in each directory to simulate a cloud foundry instance
4. After successful testing, upload the files to the foundry by referring the model upload section of the Jupyter Notebook.

Note that the names of the files (model.pkl, preprocessor.pkl, calibration_file.csv, requirements.txt and X_train.csv) should be always consistent as the foundry instance will look out for these files while performing prediction tasks
