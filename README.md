# Synthetic Data for BLENDER project
## Description

The creation of a synthetic dataset to simulate the behaviour of BLENDER is motivated by the fact that public datasets don’t contain usable device fingerprints* linked to a device. To get a better understanding of BLENDER you can visit [this repository](https://github.com/netlab-sapienza/blender).

 ***Device fingerprint**: Refers to a unique ID of a device that has a BLE technology (ie, phones).*


The dataset must consider the following characteristics:
- The station’s distance must be taken into account, to create paths. Closer stations should be more likely to be part of the same path of a device.
- Inability of a station to produce device fingerprint data.  For example, the station doesn’t detect the device in time and the device goes out of range first.
- Not all the stations have the same amount of people passing through the day. 
- Patterns in visiting places each day, week and month. For example, workers have almost the same path during a working week with a slightly difference in the time range.

This repository contains the code, data and models employed when generating the synthetics dataset. It also provides a small guide on how to run and replicate the results obtained for future use. 

## Prerequisites

This project was done using a combination of Google Colab and Google Drive (to store the data). Then, if you want to replicate the results it is necessary to follow the next steps:

1. Download the whole repository (from GitHub to your PC).
2. Store (upload) the decompressed file downloaded in the desired (own) Google Drive folder.
3. Open each one of the Notebooks stored in the `code` folder. They are named in the order of how they should be executed. Besides, each file contains explanations on how to use them.

## Directory explanation

```
BLENDER_Synthetic_Data
├── code: Contains the Google Colab notebooks used
│   ├── 01_Geolocalize stations.ipynb
│   ├── 02_Synthetic data generation and EDA.ipynb
│   └── 03_Predict number of devices.ipynb
├── data: Contains the datat generated during the project
│   ├── full_data_generated.zip: This file needs to be uncompressed manually to be used
│   ├── Possible places for stations.csv
│   └── stations_geocoded.csv
├── documentation: Has a presentation of the main results
│   └── Synthetic data generation process.pptx
└── models: Contains the models created to predict number of devices
   ├── best_params_RandomForest.pkl
   ├── best_params_XGboost.pkl
   ├── CatBoost_model.pkl
   ├── elasticnet_model.pkl
   ├── params_CatBoost_model.pkl
   ├── RandomForest_model.zip: This file needs to be uncompressed manually to be used
   └── XGboost_model.pkl

```

## Credits
This project was developed by [Daniel Jimenez](https://github.com/damjimenezgu) (MSc. Data Science student) with the guidance and supervision of [Massimo Perri](https://github.com/mp-76) (MSC. Candidate). The whole project was supervised by the Prof. [Francesca Cuomo](https://francescacuomo.site.uniroma1.it/) from the Dipartimento di Ingegneria dell'Informazione, Elettronica e Telecomunicazioni in SAPIENZA Università di Roma.

