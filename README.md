# TumSeg
Author: Utku Türkbey

Date: 13.09.2023

Hello traveler, welcome to TumSeg!

If you are here, perhaps you are looking for a Tumor Segmentation algorithm for your biomedical images. Luckily TumSeg offers a few of them.
At the very essence, TumSeg is a group of 4 supervised deep learning-based binary semantic segmentation models trained and tested on a subset of LIDC-IDRI Dataset of Lung Nodules on CT Scan [1]. With the help of nnU-Net [2] framework such 4 models are trained and tested in the TumSeg_pipeline.ipynb notebook. Pretrained Models Genesis [3] model is also used while benchmarking model performances.

For the organization of the project folders, development/evaluation process of TumSeg models, visualization of dataset and predicted segmentation masks, inference demo with your own data and any further details then you should check the notebook. Further instructions on how to navigate the notebook are also included in the notebook (duh).

But if you insist for a quick intro for folder organization, there you go:

dataset/: Where the raw and test data is stored for each case as image and mask pairs with the same name.
demo_inference/: For an inference demo, you need to store your data here in a specific format. Your predicted segmentation masks are also saved here. (Check the notebook for further details.)

nnUNet/: This folder is structured to utilize the nnU-Net framework. Training data, model architectures, training details/outcomes and many more is stored here. (Check the notebook and the nnU-Net GitHub repo link inside the notebook for organization of the folder.)

results/: Segmentation masks predicted with each model for test images are stored here. Saved model weights are also copied here in addition to nnUNet/ folder for simplicity. And most importantly, model performance evaluation results are saved here at TumSeg_results.json file.

Hope you can find your way through what you are looking for, traveler. And thanks for your visit!

[1] Data from The Lung Image Database Consortium (LIDC) and Image Database Resource Initiative (IDRI): A completed reference database of lung nodules on CT scans (LIDC-IDRI)

[2] Isensee, Fabian, et al. "nnU-Net: a self-configuring method for deep learning-based biomedical image segmentation." Nature methods 18.2 (2021): 203-211.

[3] Zhou, Zongwei, et al. "Models genesis: Generic autodidactic models for 3d medical image analysis." Medical Image Computing and Computer Assisted Intervention–MICCAI 2019: 22nd International Conference, Shenzhen, China, October 13–17, 2019, Proceedings, Part IV 22. Springer International Publishing, 2019.
