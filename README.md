# Reimplementing Semantic Synthesis using SPADE
Link to paper: https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8953676

Dataset: COCO-stuff
download from: https://github.com/nightrome/cocostuff

Make a folder on your drive. Henceforth referred to as DatasetFolder
Store its path in ROOT_PATH, in cell 16 of project.ipynb.

* Training images: http://images.cocodataset.org/zips/train2017.zip
put training images in DatasetFolder/images/train2017/

* Validation images: http://images.cocodataset.org/zips/val2017.zip
put validation images in DatasetFolder/images/val2017/

* Annotations: http://calvin.inf.ed.ac.uk/wp-content/uploads/data/cocostuffdataset/stuff_trainval2017.zip
put annotation files in DatasetFolder/annotations/

<hr>

To write the code, I referred to the block diagram in the appendix of paper at https://arxiv.org/abs/1903.07291.
Most of project.ipynb is original code.

### Borrowed code

* GANLoss class defined in cell 11 of project.ipynb
referred to from https://github.com/NVlabs/SPADE/blob/master/models/networks/loss.py

* preprocess_input function in Pix2PixModel class in cell 13 of project.ipynb
referred to from https://github.com/NVlabs/SPADE/blob/master/models/pix2pix_model.py

<hr>

### How to use

There is one notebook: project.ipynb
To use, run all cells.

* Cells 1, 2, 3: handle imports and setup
* Cells 4, 5, 6, 7, 9: define neural networks
* Cell 11: defines the losses
* Cell 13: has the main network class, and all the important functions
* Cell 14: the trainer class
* Cells 16, 17: load the dataset and dataloader
* Cell 19: This is where training happens
* Cells 20, 21, 22, 23: plot losses
* Cell 24: this is for evaluating performance on validation dataset

<hr>

### Trained model:

* included in the zip file as 2_net_G.pth, 2_net_D.pth, 2_net_E.pth
