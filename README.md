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

##################### V0.2 ######################################

An improved version of Vec3D, providing a complete definition and quantification of SML and additional evaluations on single-cell multi-omics data analysis.

The whole datasets are in Data directory. Noted that, the Atlas and CITE datasets can be required from authors due to their large size exceeded the file size requirement of github.

##################### V0.3 ######################################

Another improved version of Vec3D, especially includes a branch of python version.

Updated code usage guidance for this release:

(1) Multimodal datasets are required: the input data dset is processed as struct，including dset.Xtrain, dset.train_labels, dset.Xtest, dset.test_labels and dset.class.

(2) Main.m is the main program for executing the Vec3D algorithm. You can run the program step by step. Additionally, the sample folder provides a demo of the six datasets used for benchmarking.

(3) The output files include Result.mat (the well-trained model net)，out.mat (the pseudo images), SML.mat (the SML for each class), IFMs.mat (the informative molecules), and the prediction accuracy of the test data.

(4) Multiple datasets (dataset1, MUSE, Dyngen, DLPFC, altas) are provided to verify the Matlab code and results. The complete datasets can now also be downloaded at https://drive.google.com/drive/folders/17PwKM3JAMsG4i1rOma_CIuyHTNrc4T7d

(5) The python implementation for Vec3D is based on PyCharm. The Dyngen dataset is provided to verify the python code. We call the MATLAB code Vec3D from Python. The MATLAB Engine API for Python provides a package for Python to use MATLAB as a computation engine. The engine supports a reference implementation (CPython). For supported version information, see MATLAB product (by version) compatible Python versions. https://ww2.mathworks.cn/help/matlab/matlab-engine-for-python.html

Note:

(1) The trainNetwork() function in Matlab is used to train a CNN model. Please note your Matlab version (>= MTALAB2020a).

(2) You can train on either a CPU or a GPU (i.e. setting in line 131 of makeObjFcn5.m). For image classification, you can train a single network in parallel using multiple GPUs or a local or remote parallel pool to save training time. To use a GPU for deep learning, you must also have a supported GPU device.

(3) The MaxEpochs is set to 500 in Parameter.m. Please change this as desired. This will affect the completion time of the training.
