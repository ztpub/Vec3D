# Vec3D

Vec3D: Exploring structured molecular landscape by an explainable multi-modal model on single-cell multi-omics data

Vec3D for MATLAB is a free, open-source code for a broadly applicable “AI-for-biology” method for multi-modal analysis of single-cell multi-omics data, and provides a new and unified mathematical and biological explanation scheme for cellular heterogeneity.

At present, the manuscript about Vec3D is under review, and the code package V0.1 is freely accessed, whose decompression password can be requested from authors.

Contact Email: tanghui2020@scut.edu.cn; zeng_tao@gzlab.ac.cn or zengtao@sibs.ac.cn.



##################### V0.1 ######################################
Vec3D: Vec3D for MATLAB is free, open-source code for Structured Molecular Landscape (SML) construction, feature selection and prediction.

(1) Input files include multimodal feature matrix and labels.
(2) Main.m is the main program to execute Vec3D algorithm. The program can be run step by step for each analysis phase.
(3) Output file with *.mat contains the well-trained model, the predicted accuracy of the test data, the SML of defined cell types and the informative molecules (features).
(4) Aoria.mat is provided to verify the code.

Note : 
(1) The trainNetwork() function in Matlab is used when training a CNN model, and the Matlab version should comply with: > MTALAB2016a.
(2) Vec3D can be trained on either CPU or GPU. For image classification, a single network can be trained in parallel using multiple GPUs or a local or remote parallel pool to save training time. 
(3) MaxEpochs is set to 400 in function parameters.m, which can be adjusted for different datasets taking into account the processing time of training.


