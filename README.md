# ASTR502_project_Foote
Repository for Hayden Foote's term project in ASTR 502, Spring 2022

The goal of this project was to replicate the DeepShadows CNN and results of Tanoglidis et al. 2021, a copy of which may be found in this repository, or here: https://ui.adsabs.harvard.edu/abs/2021A%26C....3500469T/abstract

Code in this repository is based heavily on the DeepShadows repository here: https://github.com/dtanoglidis/DeepShadows

## Data Availability
Due to the size of the full datasets, they are not uploaded to this repository, though a small subset of the data sufficient to run the codes is included in the Data directory. The full datasets along with copies of the coordinate files from https://github.com/dtanoglidis/DeepShadows may be found in the Data folder here: https://drive.google.com/drive/folders/1Ut5VBYog58yztF_jeYothogKvMu3aW-k?usp=sharing

To train and test the network with the full datasets, clone the repository, then replace the included Data directory with the version found at the above link. You may also run fetch_data.ipynb to download the full sets from scratch.

## Notebooks 
*fetch_data.ipynb* Reads the coordinates of LSBGs and artifacts from the files provided in the DeepShadows repository, then downloads and saves the image cutouts in training, validation, and test sets. 

*network_tf.ipynb* Reads the datasets, then defines, trains, and tests my implementation of the DeepShadows CNN. Additionally, this notebook performs transfer learning on a dataset from HSC. This notebook saves two versions of the trained network, both of which may be found in the Trained_networks folder at the above Google Drive link. DeepShadows_tf is trained on the DES dataset alone, and DeepShadows_tf_HSC has been fine-tuned on a small dataset from HSC.

Some of the testing cells in this notebook will load the saved network(s) before testing it. If you only want to test the network, make sure you download the saved networks from the google drive folder. If you run the whole notebook in order, you don't need to do this as it will save the networks as they're trained. 
