# Automatic-Segmentation-of-Nuclei-in-Single-cell-and-Multi-cell-images-using-Deep-Learning-Approaches

# Abstract
Cervical cancer is a type of cancer that occurs in the cells of the cervix, the lower part of the uterus that connects to the vagina. Various strains of the human papillomavirus (HPV) play a role in causing most cervical cancer.  

A Papanicolaou test (Pap smear) is the most reliable screening method for identifying cancerous cells. Traditionally, pathologists visually examine the slide after performing the test to detect malignancy. However, this process is time-consuming, challenging, and limited by the availability of certified professionals. Moreover, the accuracy of visual screening can decrease due to the increased workload of pathologists.  

To improve diagnostic efficacy, **computer-aided diagnosis (CAD) systems** are essential. Nuclei segmentation is a crucial step in automated cervical cancer detection, as the nucleus carries essential information about cellular alterations during disease progression. Automated segmentation of nuclei can significantly enhance diagnostic results.  

Recent studies have shown that neural networks outperform traditional segmentation methods. This research is divided into **two phases**:

1. **Phase 1:** Segmentation of nuclei in single-cell slide images using the **Herlev Dataset**.  
2. **Phase 2:** Segmentation of nuclei in multicell slide images using the **CCEDD Dataset**.  

The **base deep learning model** used in this project is **U-Net** with an **EfficientNet-B0 encoder**.

# Features
- Automated segmentation of nuclei in single-cell and multicell images.
- Utilises deep learning (U-Net with EfficientNet-B0 encoder) for improved accuracy.
- Aims to enhance the quality of Pap test results and enable early diagnosis of cervical cancer.


# Datasets
- **Herlev Dataset**: Single-cell Pap smear images.  
- **CCEDD Dataset**: Multicell Pap smear images.

# Technology Stack
- **Python**  
- **TensorFlow / Keras** (for deep learning)  
- **OpenCV** (for image preprocessing)  
- **NumPy, Pandas** (for data handling)

# Results

## Phase 1: Single-Cell Nuclei Segmentation (Herlev Dataset)
- **Model:** U-Net with EfficientNet-B0 encoder  
- **Training:** Loss 0.02, IoU 0.95, Accuracy 96%  
- **Validation:** Loss 0.028, IoU 0.94, Accuracy 95%  
- **Test:** Dice loss 0.031, IoU 0.938, Accuracy 95%

## Phase 2: Multi-Cell Nuclei Segmentation (CCEDD Dataset)

**Unsupervised Learning:**  
- Detected general nuclei patterns, but segmentation was imprecise.  
- Training loss 0.0286, Validation loss 0.0285, Test loss 0.03 

**Semi-Supervised Learning:**  
- Masks resembled single-cell features; performance was suboptimal.  
- Training loss 0.37, Validation loss 0.38, Test loss 0.3  

# Conclusion
- Phase 1 achieved **high accuracy (~95–96%)** in single-cell nuclei segmentation.  
- Phase 2 needs **more labelled data or alternative mask generation** for better multi-cell segmentation.  
- In conclusion, the model shows potential for **automated cervical cancer detection**.
