# Prostate Segmentation

This repositorty provides a minimal working example of the prostate segmentation segmentation nnU-Net models, a series of tools for the segmentation of such anatomy from multi-parametric MR images. The model was trained using 48 multi-parametric MR images, where the annotations were computed using the transverse T2-weighted scans and apparent diffusion coefficient (ADC) maps.

We test the model by implementing an end-to-end (cloud-based) pipeline on publicly available chest CT scans hosted on the Imaging Data Commons (IDC), starting from raw DICOM CT data and ending with a DICOM SEG object storing the segmentation masks generated by the AI pipeline. The testing dataset we use is external and independent from the data used in the development phase of the model (training and validation) and is composed of prostate transversal T2-weighted MRIs acquired at 3T.

The way all the operations are executed - from pulling data to data postprocessing and the standardisation of the results - have the goal of promoting transparency and reproducibility.
You can find the notebook [here]([https://github.com/modelhub-ai/colab_liver/blob/main/nnunet_liver_mwe.ipynb](https://github.com/modelhub-ai/colab_prostate/blob/main/nnunet_prostate_mwe.ipynb)).


### Publication

Please cite the following article if you use this code or pre-trained models:

Isensee, F., Jaeger, P.F., Kohl, S.A., Petersen, J. and Maier-Hein, K.H., 2021. nnU-Net: a self-configuring method for deep learning-based biomedical image segmentation. Nature methods, 18(2), pp.203-211, [https://doi.org/10.1038/s41592-020-01008-z](https://doi.org/10.1038/s41592-020-01008-z).

The original code is published on [GitHub](https://github.com/MIC-DKFZ/nnUNet) and the p[retrained network can be found [here](https://zenodo.org/record/4003545). The original code is published using the [Apache-2.0 license](https://github.com/MIC-DKFZ/nnUNet/blob/master/LICENSE).
