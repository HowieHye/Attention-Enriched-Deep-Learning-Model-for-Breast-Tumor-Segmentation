# Attention-Enriched-Deep-Learning-Model-for-Breast-Tumor-Segmentation-in-Ultrasound-Images

The codes in this repository are based on our work presented in the paper <a href="https://arxiv.org/abs/1910.08978">Attention Enriched Deep Learning Model for Breast Tumor Segmentation in Ultrasound Images</a>. 

An important avenue for improved performance of data-driven models is via incorporating prior domain-specific knowledge. Incorporating prior knowledge in deep models for breast cancer detection is challenging, because unlike other medical organs—such as the kidney or the heart, whose features naturally lend themselves to the application of shape or boundary priors—breast tumors have large variability in shape and boundaries from case to case. Extracting other priors in the form of curvature, texture, intensity, or number of regions for breast tumors is also not an option.

In this work, we propose a new approach to integrating visual saliency into a deep learning model for breast tumor segmentation in ultrasound images. Visual saliency refers to image maps containing regions that are more likely to attract radiologists’ visual attention. The proposed approach introduces attention blocks into a
U-Net architecture and learns feature representations that prioritize spatial regions with high saliency levels. The validation results indicate increased accuracy for tumor segmentation relative to models without salient attention layers.

# Codes
Jupyter notebooks present the implementation of the proposed approach using Keras and Tensorflow libraries.
* <a href="Codes/UNet.ipynb">UNet</a> - implementation of the standard U-Net model for breast tumor segmentation. The U-Net is used as a baseline model for evaluation of our approach.
* <a href="Codes/SA_UNet.ipynb">SA_UNet</a> - our proposed Salient Attention U-Net model. It applies attention blocks to saliency maps of breast ultrasound images. 
* <a href="Codes/SA_UNet_reduced_set.ipynb">SA_UNet_reduced_set</a> - Salient Attention U-Net model applied on a reduced version of the dataset consisting of 118 images. The quality of the saliency maps can vary significantly across a collection of images; therefore, in the article we proposed an algorithm for estimating the confidence level of the saliency maps and eliminating the saliency maps with low confidence.

# Data
This repository uses an open public dataset of breast ultrasound images known as <a href="https://ieeexplore.ieee.org/document/8003418">Dataset B</a> for implementing the proposed approach. Note that the implementation in this repository is different from the validation presented in the paper, which is based on a larger dataset that is not public. 
* Images - the dataset consists of 163 breast ultrasound images.
* Masks - segmentation masks corresponding to the images.
* Saliency - saliency maps for the 163 breast ultrasound images; the maps are obtained based on our approach presented in <a href="https://ieeexplore.ieee.org/document/8545599">Xu et al. (2019) A Hybrid Framework for Tumor Saliency Estimation</a>.
* Saliency_maps_118 - a reduced set of saliency maps consisting of 118 images.

# Network Architecture
![SA-UNet Architecture](images\model.jpg)
<img style=\"float: left; height:200px;\" src=\"images\model.jpg\">
Architecture of the proposed U-Net model with salient attention. The model uses breast ultrasound images and saliency maps as inputs and produces segmentation probability maps as outputs. Conv = convolution; Deconv = deconvolution.

# Citation
If you use the codes or the methods in your work, please cite the following <a href="https://www.sciencedirect.com/science/article/abs/pii/S0301562920302878">article</a>:   

    @ARTICLE{Vakanski2020,
    title={Attention-Enriched Deep Learning Model for Breast Tumor Segmentation in Ultrasound Images},
    author={Vakanski, A. and Xian, M. and Freer, P. E.},
    journal={Ultrasound in Medicine & Biology}, 
    year={2020},
    month={Sep.},
    volume={46},
    number={10}
    pages={2819-2833},
    doi={https://doi.org/10.1016/j.ultrasmedbio.2020.06.015}
    }

# License
<a href="License - MIT.txt">MIT License</a>


# Acknowledgments
This work was supported by the <a href="https://imci.uidaho.edu/get-involved/about-cmci/">Institute for Modeling Collaboration and Innovation (IMCI)</a> at the University of Idaho through NIH Award #P20GM104420.
