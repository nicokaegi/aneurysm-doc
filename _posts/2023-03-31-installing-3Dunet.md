---
title: "Installing and Running 3DUNet"
date: 2023-03-31 15:47:42 +0200
categories: [Tutorial]
tags: []
---

To install and run 3DUNet, you'll need to follow these steps:

1. Clone the needed training scripts to your local machine by running the following command in your terminal:

git clone https://github.com/wolny/pytorch-3dunet.git

this is so you can get access to the traing, and testing config files later on. 

2. Create a new conda environment with the required dependencies:

conda create -n pytorch-3dunet --c pytorch -c nvidia -c conda-forge -c awolny pytorch-3dunet

3. Activate the new environment:

conda activate pytorch-3dunet

4. Train a model using the `train3dunet` script:

To train a model, you can run the `train3dunet` script with the provided configuration file:

train3dunet --config <CONFIG>

This command will start training a 3DUNet model using the specified configuration file. You can replace `<CONFIG>` with the path to your own configuration file.

