# AdvAttByGAN

## Adversarial Attacks on Deepfake Detectors: A GAN-Based Approach for Generating Imperceptible Perturbations

# Adversarial Attacks on Deepfake Detectors: A GAN-Based Approach

## Overview

This repository contains the code for generating imperceptible perturbations to adversarially attack deepfake detectors using a GAN-based approach. The code is implemented in PyTorch and has been tested with Python 3.8.10.

## Dataset

The dataset used for this project is the FaceForensics++ dataset, which is a large-scale, diverse dataset for deepfake detection and face forensics.

## Environment

- **Python**: 3.8.10
- **Framework**: PyTorch

## Setup

Before you begin, ensure you have the necessary environment and dependencies installed. You can set up your environment by installing the required packages using the following command:

```bash
pip install -r requirements.txt
Usage
Training
To train a generative network for universal perturbations, follow these steps:
1.	Specify the paths to both training and validation folders.
2.	Run the training script with the specified parameters:
Bash
CUDA_VISIBLE_DEVICES=0,1 python main.py --expname test_incv3_universal_targeted_linf10_twogpu --batchSize 32 --testBatchSize 16 --mag_in 10 --foolmodel incv3 --mode train --perturbation_type universal --target -1 --gpu_ids 0,1 --nEpochs 10
Testing
The testing process is performed when the mode is set to test. Use the following command to run the testing:
bash
CUDA_VISIBLE_DEVICES=0,1 python main.py --expname test_incv3_universal_targeted_linf10_twogpu --mode test
Parameters
•	--expname: Name of the experiment.
•	--batchSize: Batch size for training.
•	--testBatchSize: Batch size for testing.
•	--mag_in: Magnitude of the perturbation.
•	--foolmodel: Model to be fooled (e.g., incv3).
•	--mode: Mode of operation (train or test).
•	--perturbation_type: Type of perturbation (e.g., universal).
•	--target: Target label for targeted attacks.
•	--gpu_ids: IDs of the GPUs to use.
•	--nEpochs: Number of epochs to train.
Contributing
If you'd like to contribute to this project, please fork the repository and submit a pull request with your changes. Make sure to include documentation and tests for any new features.
Acknowledgements
We would like to thank the creators and maintainers of the FaceForensics++ dataset for providing a valuable resource for deepfake detection research.


