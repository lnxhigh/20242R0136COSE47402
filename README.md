# Monocular Depth Estimation with Segment Anything Model
## COSE474-2024F Deep Learning Final Project

### All.ipynb
It contains the code for the entire pipeline.
- Model Construction
- Load data and build dataloader
- Train models

### data.ipynb
It contains the code for loading data and building data loader.

[NYU-Depth-V2](https://cs.nyu.edu/~fergus/datasets/nyu_depth_v2.html) dataset is used to train the model.
I downloaded the data from [Kaggle](https://www.kaggle.com/datasets/soumikrakshit/nyu-depth-v2)

NYU Depth Dataset V2 is a dataset for research in 3D computer vision.
It focuses on tasks like depth estimation and indoor scene understanding. 
It provides paired RGB images and depth maps.

I referred to the [Kaggle Notebook](https://www.kaggle.com/code/shreydan/monocular-depth-estimation-nyuv2)
to build a Dataset and DataLoader.

![](https://github.com/lnxhigh/20242R0136COSE47402/blob/main/FinalProject/Report/figures/nyu-depth-v2.jpg)

### model.ipynb
It contains a code for constructing the model.
- The given image is encoded using SAM encoder to generate a feature map. 
- The feature map is then decoded into a depth map through residual connections and transposed convolutions.
- The output depth map is resized to match the target size using bilinear interpolation.
- Finally, a loss function is applied to compare the predictions with the ground truth.

![](https://github.com/lnxhigh/20242R0136COSE47402/blob/main/FinalProject/Report/figures/model-figure.png)

### train.ipynb
It contains a code for training models.

Training results are in the all.ipynb file.

### compare.ipynb
It contains a code for evaluating the model.

The baseline model for comparison is Depth-Anything-V2-Small.

![](https://github.com/lnxhigh/20242R0136COSE47402/blob/main/FinalProject/Report/figures/model-comparison.png)

