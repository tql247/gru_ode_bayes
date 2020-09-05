# GRU-ODE-Bayes

This implementation completes the paper : GRU-ODE-Bayes : continuous modeling of sporadically-observed time series.

Modeling real-world multidimensional time series can be particularly challenging when these are *sporadically* observed (i.e., sampling is irregular both in time and across dimensions)---such as in the case of clinical patient data. To address these challenges, we propose (1) a continuous-time version of the Gated Recurrent Unit, building upon the recent Neural Ordinary Differential Equations (Chen et al. 2018), and (2) a Bayesian update network that processes the sporadic observations. We bring these two ideas together in our GRU-ODE-Bayes method. 

This repository provides pytorch implementation of the GRU-ODE-Bayes paper. 


## Datasets
The datasets for Brusselator, double OU and processed USHCN data have been uploaded on the repo for compatibility. 
The MIMIC dataset is not directly publicly available and was thus not pushed. It can be downloaded at : https://physionet.org/physiobank/database/mimic3cdb/

Folder 'data_preproc' contains all steps taken to preprocess the Climate and MIMIC datasets.

## Acknowledgements and References

The torchdiffeq package has been extended from the original version proposed by (Chen et al. 2018)

Chen et al. Neural ordinary differential equations, NeurIPS, 2018.

For climate dataset : 

Menne et al., Long-Term Daily Climate Records from Stations Across the Contiguous United States



### **Note**

Install the main package :

```
pip install -e . 
```
And also the ODE numerical integration package : 
```
cd torchdiffeq
pip install -e .
```

```
cd experiments\me
me_gruode.py
```
```
cd data_preproc\me
generate_folds.py
```
