This folder contains features extracted from the GPDS-960 dataset [1], using the SigNet model [2] (CNN trained on a subset of the GPDS dataset).

The dataset is split as follows:

 \Exploitation: First 300 users (GPDS-300).
 \Validation: Users 301-350 (used as validation set for choosing the CNN architecture)
 \Development: Users 351+ (used to train the CNN)

There are two files for each user: real_X.mat and forg_X.mat. The first contains a matrix of size N x 2048, containing the feature vectors of N genuine signatures from that user. The second contains a matrix of size 30 x 2048, containing the feature vectors of each of the 30 skilled forgeries made targetting the user. The numbering of the users follow the original GPDS dataset.

## Loading the feature vectors in matlab

>> f = load('real_2.mat')
% f.features: [24x2048 single]

## Loading the feature vectors in python

>> from scipy.io import loadmat
>> features = loadmat('real_2.mat')['features']
# features: numpy array of shape (24, 2048)


For more information about our project, please visit: https://www.etsmtl.ca/Unites-de-recherche/LIVIA/Recherche-et-innovation/Projets/Signature-Verification.

If you use these features in your work, please cite the paper that introduced the dataset and the work that described the model:


[1] Vargas, J.F., M.A. Ferrer, C.M. Travieso, and J.B. Alonso. 2007. “Off-Line Handwritten Signature GPDS-960 Corpus.” In Document Analysis and Recognition, 9th International Conference on, 2:764–68. doi:10.1109/ICDAR.2007.4377018.

[2] Hafemann, Luiz G., Robert Sabourin, and Luiz S. Oliveira. 2017. “Learning Features for Offline Handwritten Signature Verification Using Deep Convolutional Neural Networks.” Pattern Recognition 70 (October): 163–76. doi:10.1016/j.patcog.2017.05.012.

