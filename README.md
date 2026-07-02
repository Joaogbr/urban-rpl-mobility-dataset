# Urban RPL Mobility Dataset

This repository contains the RSSI traces and preprocessing scripts used to generate the datasets employed in the paper:

> *An HMM-Based Link-State Prediction Objective Function for Mobility-Aware RPL Networks*

## Repository structure

### rssi_traces/

Contains the RSSI traces extracted from Cooja simulations. Each trace includes the information required to reconstruct the datasets used in this work, such as timestamps, RSSI measurements, and node identifiers.

### Urban_RPL_Mob_Dataset_Processing.ipynb

Contains the Python preprocessing script used to generate the datasets for HMM training.
The script generates observation vectors containing the input variables of the proposed HMM (RSSI, trend, and staleness) at intervals defined by the WINDOW parameter.
This preprocessing mode was used to generate the dataset employed for HMM training in the paper.


* **Packet Vector:** generates one sample for each received packet.
* **Observation Vector:** generates observation vectors at fixed 1-second intervals. This is the preprocessing mode used to generate the dataset employed for HMM training in the paper.
  
## Reproducibility

The Observation Vector dataset used to train the Hidden Markov Model can be fully reproduced from the RSSI traces provided in this repository using the supplied preprocessing script.

## Citation

If you use this dataset in your research, please cite the corresponding publication.
