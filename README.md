# Sampling_experiments_LET_Argo

This repository contains code used for the study "The importance of adding unbiased Argo observations to the ocean carbon observing system" (Heimdal & McKinley, 2024, Scientific Reports). In this paper, we reconstruct surface ocean pCO2 using the Large Ensemble Testbed (Gloege et al., 2021, https://doi.org/10.1029/2020GB006788) and the pCO2-Residual method (Bennington et al., 2022, https://doi.org/10.1029/2021MS002960). In addition to a "SOCAT-baseline", we tested 2 different Argo float sampling schemes (Historical and potential optimized sampling). We did 3 different  experiments for each sampling scheme: a baseline, biased floats, and floats with random uncertainty. All float experiments also include SOCAT sampling. 

This repository contains code for running the machine learning models and processing data. The reconstructed pCO2 model fields are not published due to large file sizes (75 reconstructions per sampling experiment), however please feel free to reach out if you are interested in any of these. Model output of the Large Ensemble Testbed can be found here: https://figshare.com/collections/Large_ensemble_pCO2_testbed/4568555. The SOCAT+Argo sampling masks are published on Zenodo https://doi.org/10.5281/zenodo.13367537.     

Overview of files in this repository:

Data processing and machine learning:

"Calculate_pco2_components.ipynb": Code for calculating pCO2, pCO2-T (direct effect of temperature on pCO2) and pCO2-Residual. We use pCO2-Residual as a target variable for the reconstruction.

"LET_dataframe_XGB.ipynb": Code for setting up data and performing the machine learning for reconstructing pCO2.  

"Calculate_flux.ipynb": Code for calculating air-sea CO2 fluxes from the reconstructed pCO2 model fields and the LET "model truth" fields.

Supporting files with functions:

"Val_mapping.ipynb": To create map plots.

"pre_argo.py": Needed to run the data processing and machine learning notebook. 

Environment file:

"environment_file.yml": list of packages and versions needed to set up an environment to run the code.

Folder: "Figures":

- "Fig_Argo_masks.ipynb"
- "Fig_boxplots.ipynb"
- "Fig_timeseries.ipynb"
- "Fig_maps.ipynb"
- "Table_IQR.ipynb"





