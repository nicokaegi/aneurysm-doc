---
title: "How to run 3DUNet"
date: 2023-04-07
categories: [Tutorial]
tags: []
---


# To run 3DUNet, you'll need to follow these steps:

1. Copy the pre prepared 3dunet dir :

    `$ cp -R /home/kaegin63/aneurysm/3dunet-aneurysm .`

    This dir in theory should contain the basic things you need to get 3dunet up and training.
    as well as prepare data for 3dunet to use.   

2. Activate the virtual environment :

    `$ source 3dunet-env/bin/activate`

    In this python virtual environment you should find all the libraries necessary to run 3dunet.
    as well as the bash commands to start training

3. (optional) Auto activate the environment :

    you can have your have this enviroment activate automatically upon logging.

    first open ~/.bashrc in the editor of your choice. Then add following to the end of your .bashrc

    `source <path-to-3dunet-env>/3dunet-env/bin/activate` 

4. Start model training :

    `$ train3dunet --config <CONFIG>`

    This command will start training a 3DUNet model using a specified training.yaml config file. 
    Within each config file contains the settings for the models training.

    > The latest config file I used for training was in 3DUnet_aneurysm - nico 

5. Predict with the model :

    Similar to `train3dunet`, `predict3dunet` requires a test.yaml config file in order to know what to do.

    `$ predict3dunet --config <CONFIG>`

> See the the data prep guide to learn how to give the model custom data. 