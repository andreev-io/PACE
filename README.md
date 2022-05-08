# Replicating PACE - Learning Effective Task Decomposition for Human-in-the-loop Healthcare Delivery

## Citation

Kaiping Zheng, Gang Chen, Melanie Herschel, Kee Yuan Ngiam, Beng Chin Ooi, and Jinyang Gao. 2021. PACE: Learning Effective Task Decomposition for Human-in-the-loop Healthcare Delivery. Proceedings of the 2021 International Conference on Management of Data. Association for Computing Machinery, New York, NY, USA, 2156–2168. https://doi.org/10.1145/3448016.3457281


## Replication Instructions

1. Set up a conda environment with the packages defined in the provided environment.yml, and activate the environment

```bash
conda env create --name pace-replication --file=environment.yaml
conda activate pace-replication
```

2. Download the preprocessed dataset built using [MIMIC Extract](https://github.com/MLforHealth/MIMIC_Extract) from GCP: https://console.cloud.google.com/storage/browser/mimic_extract. To access this, you will need access to the MIMIC-III dataset, and link your physionet account to GCP.

3. Run the code in `mimic_extract_analysis.ipynb`, to process the downloaded file, and generate training, validation and test datasets.

4. Run the code in `model.ipynb` to train the model, run tests, and save the predictions and trained model to a local directory.

5. Run the code in `metrics.ipynb` to obtain the graphs used in the report

## Dependencies

Listed in `environment.yml`

## Table of results

The predictions used in the paper are included in the `predictions` directory, which is used in `metrics.ipynb`. The reference labels for these labels are provided in `test_labels.pkl`.
