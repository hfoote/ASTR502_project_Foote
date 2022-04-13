# ASTR502_project_Foote
Repository for Hayden Foote's term project in ASTR 502, Spring 2022

## Notebooks 
*fetch_data.ipynb* Reads the coordinates of LSBGs and artifatcs from the files provided in the paper repository, then downloads and saves the image cutouts in training, validation, and test sets. Due to the size of the datasets, they are not uplodaed to this repository. The Data directory for this project with the coordinate files and all datasets created by this notebook may be found here: https://drive.google.com/drive/folders/1Ut5VBYog58yztF_jeYothogKvMu3aW-k?usp=sharing

*network_tf.ipynb* Reads the datasets (which may be found at the above link), then defines, trains, and tests my implementation of the DeepShadows CNN. Additionally, this notebook performs transfer learning on an additional dataset from HSC. This notebook saves two versions of the trained network, both of which may be found in the Trained_networks folder at the above link. DeepShadows_tf is trained on the DES dataset alone, and DeepShadows_tf_HSC has been fine-tuned on a small dataset from HSC.
