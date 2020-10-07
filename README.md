# Attention-Enriched-Deep-Learning-Model-for-Breast-Tumor-Segmentation-in-Ultrasound-Images

The codes in this repository are based on our work presented in the paper <a href="https://arxiv.org/abs/1910.08978">Attention Enriched Deep Learning Model for Breast Tumor Segmentation in Ultrasound Images</a>. 

# Codes
Jupyter notebooks present the implementation of the proposed approach using Keras and Tensorflow libraries.
* <a href="Codes/UNet.ipynb">UNet - implementation of the standard U-Net model for breast tumor segmentation. The U-Net is used as a baseline model for validation of our approach.
* <a href="Codes/SA_UNet.ipynb">SA_UNet - our proposed Salient Attention U-Net model. It applies attention blocks to saliency maps of breast ultrasound images. 
* <a href="Codes/SA_UNet_reduced_set.ipynb">SA_UNet_reduced_set - Salient Attention U-Net model applied on a reduced version of the dataset consisting of 118 images. The quality of the saliency maps can vary, therefore, we proposed an algorithm for estimating the quality and eliminating saliency maps with low quality.

# Citation
If you use the codes or the methods in your work, please cite the following <a href="https://www.sciencedirect.com/science/article/abs/pii/S0301562920302878">article</a>:   

    @ARTICLE{Vakanski2020,
    title={Attention-Enriched Deep Learning Model for Breast Tumor Segmentation in Ultrasound Images},
    author={Vakanski, A. and Xian, M. and Freer, P. E.},
    journal={Ultrasound in Medicine & Biology}, 
    year={2020},
    month={Feb.},
    volume={46},
    number={10}
    pages={2819-2833},
    doi={https://doi.org/10.1016/j.ultrasmedbio.2020.06.015}
    }

# License
<a href="License - MIT.txt">MIT License</a>


# Acknowledgments
This work was supported by the <a href="https://imci.uidaho.edu/get-involved/about-cmci/">Institute for Modeling Collaboration and Innovation (IMCI)</a> at the University of Idaho through NIH Award #P20GM104420.
