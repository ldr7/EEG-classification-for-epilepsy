# EEG-Classification-for-Epilepsy 
## Objective  
The objective of this project is to create a model that can classify a given EEG signal as that from an epileptic or non-epileptic patient.  

## Data
The dataset used in this project is the single channel Anderzak dataset which has five folders labeled A through E with 100 txt files each.
Each txt file consists of a EEG signal of 23.6 seconds duration.
The sets were selected from EEG records after purifying artifacts caused by eye and muscle movements. 
Sets A (eyes open) and B (eyes closed) were extracranially taken from five healthy subjects. 
Sets C, D, and E were intracranially taken from five epilepsy patients. 
While sets D and C contained the EEG activity measured in seizure-free intervals from epileptic hemisphere and the opposite hemisphere of the brain,respectively, set E only contained the seizure activity.   
  
## Classifier
7 Classification models are constructed to classify the data as coming from an epileptic or non-epileptic patient.  
The best model computes statistical parameters listed below for the coefficients of the DWT of the EEG signal. It then applies KNN (k=2) to classify the signals.
* mean
* mean-square
* standard deviation
* absolute difference
* skew  
  
The best model obtains accuracy between 95-96% on 2000 splits of the data.  
Scope for imporovement in this work would involve use of GridSearch (scikit-learn) or frameworks like TPOT for tuning hyperparameters.  
  
## Technologies  
The project uses the following:
* Python 3
* Jupyter
* Numpy
* Pandas
* Scikit-learn 
* Keras
* Scipy
* pywt
