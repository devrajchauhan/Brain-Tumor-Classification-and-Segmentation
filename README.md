# Brain-Tumor-Classification-and-Segmentation
**Title:** Integrated Brain Tumor Classification and Segmentation using Custom CNN Architectures and Transfer Learning

**Dataset Used:** https://figshare.com/articles/dataset/brain_tumor_dataset/1512427

This brain tumor dataset containing 3064 T1-weighted contrast-inhanced images from 233 patients with three kinds of brain tumor: meningioma (708 slices), 
glioma (1426 slices), and pituitary tumor (930 slices). Due to the file size limit of repository, we split the whole dataset into 4 subsets, and achive 
them in 4 .zip files with each .zip file containing 766 slices.The 5-fold cross-validation indices are also provided.

This data is organized in matlab data format (.mat file). Each file stores a struct containing the following fields for an image:

cjdata.label: 1 for meningioma, 2 for glioma, 3 for pituitary tumor
cjdata.PID: patient ID
cjdata.image: image data
cjdata.tumorBorder: a vector storing the coordinates of discrete points on tumor border.
		For example, [x1, y1, x2, y2,...] in which x1, y1 are planar coordinates on tumor border.
		It was generated by manually delineating the tumor border. So we can use it to generate
		binary image of tumor mask.
cjdata.tumorMask: a binary image with 1s indicating tumor region


**ABSTRACT:** 

This research project focuses on brain tumor analysis using a combination of custom convolutional neural network (CNN) architectures, transfer learning, and image segmentation techniques The main goal is twofold: accurate brain tumor classification and tumor accurate zone segmentation from MRI images. The custom CNN image and pre-trained images are used and optimized for grayscale MRI images for classification. These models receive extensive training and evaluation, resulting in promising levels of accuracy. In parallel, the U-Net algorithm is used to achieve high tumor area segmentation accuracy. This comprehensive approach provides valuable insight into the specific diagnosis and location of brain tumors and contributes to advances in medical imaging studies


**INTRODUCTION:** 

Brain tumors pose a serious threat to public health, such that accurate and timely diagnosis is required for effective treatment strategies. Magnetic resonance imaging (MRI) has become a cornerstone for the diagnosis and evaluation of brain tumors due to its non-invasive properties and imaging resolution but analysis of MRI data, especially tumor classification and accurate tumor segmentation is still lacking still strong and difficult.
This research work addresses the need for robust and accurate brain tumor detection through advances in deep learning, particularly convolutional neural networks (CNNs) and improvements in feature learning techniques applied to in other fields. The main objective of this study is to develop an integrated algorithm that combines a standard CNN algorithm with state-of-the-art pre-trained images, optimized for high-resolution MRI images, with image background classification, in particular system using U-Net together


**Tumor Classification:**

The initial phase of the project focuses on brain tumor classification. Custom CNN architectures, inspired by prior research, are designed, and trained on a dataset of 128x128 pixel grayscale MRI images. To enhance the model's ability to classify tumors accurately, preprocessing steps include tumor region segmentation based on masks, extending the segmentation to adjacent tissues, and selecting the most effective expansion factor. This approach aims to maximize classification accuracy and aid in precise tumor localization.
This research is primarily concerned with the classification of brain tumors. The customized CNN algorithms are carefully designed and trained on a dataset of 128x128 pixel grayscale MRI images. However, there are important preliminary steps in the journey to successful classification. Motivated by previous research, we apply a mask-based tumor classification method. This mask defines the tumor boundaries on the MRI images, helping to accurately localize the infection. Furthermore, we extend this classification to include adjacent healthy neurons, another approach that shows great promise in improving classification accuracy. By strongly detecting different expansion factors, we optimize the ability of the model to distinguish tumor from non-tumor regions, thereby increasing the accuracy of analysis


**Transfer Learning:**

In addition to custom CNNs, pre-trained models such as ResNet-18, ResNet-50, DenseNet121, VGG19, and VGG16 are adapted to the task. These models are modified to accommodate grayscale images and tailored to classify MRI images into one of three tumor categories. By leveraging transfer learning, the research explores whether pre-trained models can improve classification performance and reduce training time compared to training from scratch.

**Tumor Segmentation:**
The work delves into tumor classification, an important aspect of brain tumor research. U-Net architecture is used to obtain remarkable specificity in defining tumor areas through architecture, transfer learning methods, and advanced classification models, the study seeks to improve the accuracy of brain tumor detection and localization. The goal is to provide valuable insights to medical professionals and researchers in medical imaging research, ultimately improving patient care and medical outcomes.

