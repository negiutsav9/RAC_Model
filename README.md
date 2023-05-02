# Predicting the properties of Recycled Aggregate Concrete under Axisymmetric and True Triaxial Load

### Source : Xu, J., Chen, Y., Xie, T., Zhao, X., Xiong, B., Chen, Z., (2019), Prediction of triaxial behavior of recycled aggregate concrete using multivariable regression and artificial neural network techniques, Construction and Building Materials, Volume 226, Pages 534-554, ISSN 0950-0618, https://doi.org/10.1016/j.conbuildmat.2019.07.155


This repository consist of files which can be used to refer the training a machine learning model using [MAST-ML](https://github.com/uw-cmg/MAST-ML) and upload the trained model to the cloud foundry.

## Steps to follow

1. Run the jupyter notebook paperModel_MNR.ipynb to generate model weights, preprocessed data and calibration file for each model
2. For each model, create a directory with its model.pkl, preprocessor.pkl, calibration_file.csv, requirements.txt and X_train.csv files (refer Container files)
3. Run Repo2Docker in each directory to simulate a cloud foundry instance
4. After successful testing, upload the files to the foundry by referring the Jupyter Notebook modelDeployment.ipynb.

Note that the names of the files (model.pkl, preprocessor.pkl, calibration_file.csv, requirements.txt and X_train.csv) should be always consistent as the foundry instance will look out for these files while performing prediction tasks
