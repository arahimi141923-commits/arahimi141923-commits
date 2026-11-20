# Hi, I'm Aisan Rahimi 👋
### AI Engineer | Computer Vision Expert | Medical Imaging Specialist

🏢 Founder of [Apadana AI Research Center](https://github.com/Apadana-AI-Research-Center)  
📍 Tehran, Iran  
📧 a.rahimi141923@gmail.com  

---

## 🧠 About Me

AI Engineer and Computer Vision Expert with **5+ years of experience** in medical
imaging, petroleum data analysis, and AI software development. MSc in Photogrammetry
and Image Processing from K.N. Toosi University of Technology.

I build end-to-end AI pipelines for real-world clinical and industrial applications —
from research and model training to deployment and software integration.

---

## 🎯 Expertise

### 🏥 Medical AI


## 🏥 Featured Clinical AI Project | Automated Mammography Lesion Detection & BI-RADS-Guided Classification

**Clinical Collaboration:** Razi Radiology Center — Dr. Vahid Alizadeh  
**Joint Development:** AI-PACS & Iran Nobat | 2025  
**Research Status:** Manuscript in preparation for journal submission

Developed and clinically demonstrated an **end-to-end AI-assisted mammography analysis system** in collaboration with **Dr. Vahid Alizadeh at Razi Radiology Center**. The system was designed to assist radiologists in detecting subtle breast abnormalities, including suspicious lesions that may be difficult to identify during routine visual examination.

The framework integrates **deep learning-based lesion detection, precise candidate localization, multi-view mammographic analysis, and BI-RADS-guided multi-label classification**. It analyzes mammography images from different projections (CC and MLO), detects potentially abnormal regions, and classifies findings into **Mass, Suspicious Calcification, Focal Asymmetry, and No Finding**.

The system provides visual bounding boxes, confidence scores, and interpretable classification results to support radiological review and screening decisions.

### 🔬 Clinical Demonstration — Razi Radiology Center

The following examples demonstrate AI-generated abnormality predictions and localization of suspicious regions in mammographic examinations.

<p align="center">
  <img src="images/IMG-61795_pred.png" width="48%" />
  <img src="images/IMG-61797_pred.png" width="48%" />
</p>
<p align="center">
  <img src="images/IMG-61799_pred.png" width="48%" />
  <img src="images/IMG-61801_pred.png" width="48%" />
</p>

<p align="center">
  <em>Clinical AI demonstrations showing abnormality predictions,
  candidate lesion localization, and associated confidence scores.</em>
</p>

### ⚙️ AI Architecture & Technical Innovation

A three-stage architecture was developed:

1. **Hybrid FCOS Detection:** Customized FCOS with a ResNet-50/FPN backbone and an auxiliary classification head for abnormality detection and lesion localization.
2. **BI-RADS-Guided Feature Extraction:** Quantitative analysis of lesion shape, margins, density, texture, calcification patterns, and cross-view consistency.
3. **Stacked XGBoost Classification:** Multi-label classification using per-class ensemble stacking, probability calibration, and clinically constrained threshold optimization.

**Complete Processing Pipeline**

<p align="center">
  <img src="images/paper_pipeline_overview.png" width="65%" />
</p>

**Hybrid FCOS Detection Architecture**

<p align="center">
  <img src="images/paper_hybrid_fcos_architecture.png" width="75%" />
</p>

### 📊 Experimental Results & Model Precision

**Dataset:** RSNA Screening Mammography  
**Total Images:** 20,486  
**Training Images:** 16,391  
**Validation Images:** 3,745  
**Detection Test Images:** 350

#### 1. Abnormality Detection Performance

The Hybrid FCOS detector achieved the following results on the reported independent 350-image test set:

| Evaluation Metric | Result |
|---|---:|
| **Accuracy** | **99.1%** |
| **Precision (PPV)** | **97.8%** |
| **Sensitivity (Recall)** | **100.0%** |
| **Specificity** | **98.6%** |
| **F1-Score** | **98.9%** |

These results demonstrate high sensitivity for distinguishing abnormal from normal mammographic images under the evaluated test conditions.

**Training and Localization Results**

<p align="center">
  <img src="images/paper_localization_iou.png" width="75%" />
</p>

Candidate lesion localization achieved an **86.8% detection rate at IoU > 0**, with **60.3% of abnormal cases reaching IoU ≥ 0.3**. The detector was optimized to prioritize sensitivity and candidate lesion discovery rather than exact boundary delineation.

#### 2. BI-RADS-Guided Classification Performance

The multi-view XGBoost classification stage achieved:

| Mammographic Finding | Sensitivity | Specificity | Precision (PPV) |
|---|---:|---:|---:|
| Mass | **87.3%** | 98.9% | 84.1% |
| Suspicious Calcification | 82.4% | **99.6%** | **93.3%** |
| Focal Asymmetry | 71.4% | 97.8% | 45.5% |
| No Finding | **100.0%** | 84.1% | 97.3% |

**Overall Multi-Label Classification Performance:**

- **Micro F1-Score:** 98.1%
- **Macro F1-Score:** 85.8%
- **Mass Classification F1:** 87%
- **Suspicious Calcification F1:** 82%
- **Focal Asymmetry F1:** 73%

**Multi-View Classification Results**

<p align="center">
  <img src="images/paper_classification_results.png" width="85%" />
</p>

#### 3. Impact of Multi-View Mammographic Analysis

A comparative evaluation investigated four feature configurations:

| Configuration | Test Macro F1 |
|---|---:|
| Single-View Features | 74.5% |
| **Multi-View CC/MLO Features** | **85.8%** |
| Bilateral Features | 73.8% |
| Combined Features | 84.1% |

Multi-view integration significantly improved the classification of subtle mammographic findings, particularly **Focal Asymmetry**, where the F1-score increased from **42% to 73%** — approximately **74% relative improvement** compared with single-view analysis.

<p align="center">
  <img src="images/paper_multiview_performance.png" width="90%" />
</p>

### 🖥️ Clinical Software Integration

The AI detection and classification workflow was demonstrated through a medical imaging interface supporting mammographic image visualization, candidate lesion marking, and classification output.

<p align="center">
  <img src="images/paper_clinical_interface.png" width="80%" />
</p>

<p align="center">
  <img src="images/msg39090518-6456.jpg" width="45%" />
</p>

### 🎯 Clinical Significance

This project demonstrates the potential of AI-assisted mammography to support the identification of subtle suspicious findings, including lesions that may be challenging to recognize through visual inspection alone.

Its key strengths include:

- High image-level abnormality detection sensitivity in the evaluated dataset.
- Detection and visual localization of suspicious mammographic regions.
- Multi-label classification aligned with BI-RADS finding terminology.
- Improved recognition of subtle focal asymmetries through multi-view analysis.
- Interpretable model outputs to support radiologist review.
- Clinical software demonstration at Razi Radiology Center.

The system is intended as a **radiologist-assistance and clinical decision-support tool**, not a replacement for specialist interpretation. Prospective clinical validation and radiologist reader studies remain necessary to establish real-world diagnostic benefit.

### 📄 Scientific Publication

**Manuscript Title:**  
*Automated Multi-View Mammography Analysis Using BI-RADS-Guided AI for Clinical Decision Support*

**Research Status:** Manuscript prepared for submission to a peer-reviewed scientific journal.



-Evaluation & Fine-Tuning of Vision-Language Models for Medical Image Understanding

Conducted experimental research on medical Vision-Language Models (VLMs) and Large Language Models (LLMs), focusing on multimodal medical image understanding, anatomical localization, disease interpretation, and automated radiology report generation. Evaluated and experimented with models including MedGemma, Gemma-based architectures, and PaliGemma-related object detection approaches, using brain imaging and chest CT datasets. Explored domain-specific fine-tuning strategies involving LoRA/PEFT, vision encoder adaptation, quantization, and image-text instruction tuning to improve medical image interpretation and structured clinical reporting. Investigated the ability of multimodal models to recognize abnormalities, identify anatomical regions, estimate spatial positions, and associate findings with their correct locations. Experiments revealed significant limitations in precise anatomical localization, spatial reasoning, and position-aware reporting, highlighting the challenges of applying general-purpose VLMs to detailed medical imaging tasks. This research provided hands-on experience in multimodal model evaluation, medical dataset preparation, fine-tuning, prompt engineering, and failure analysis, supporting the development of more reliable hybrid workflows combining specialized computer vision models with medical LLMs.

Technologies: Python | PyTorch | Hugging Face Transformers | MedGemma | PaliGemma | Vision-Language Models | LoRA/PEFT | Quantization | Medical Image Analysis | Multimodal Fine-Tuning

-Automated Lumbar Disc Disease Detection, Classification & AI-Assisted Radiology Reporting

Developed an end-to-end deep learning pipeline for automated lumbar spine MRI analysis, integrating intervertebral disc localization, segmentation, and pathology classification using Vision Transformers (ViT), object detection, and multi-task deep learning architectures. The system analyzes sagittal and axial MRI images to identify lumbar disc levels (L1–L2 through L5–S1) and classify disc conditions into four categories: Normal, Bulging, Protrusion, and Extrusion, providing confidence scores and visual bounding-box annotations. The project incorporated DICOM–NIfTI image-mask alignment, class-imbalance optimization, and multi-task segmentation and classification. Additionally, MedGemma integration was explored to transform structured imaging findings into AI-generated radiology-style reports, supporting automated medical image interpretation and clinical decision-support workflows.
Technologies: Python | PyTorch | Vision Transformers (ViT-B/16) | Object Detection | Medical Image Segmentation | DICOM | NIfTI | SimpleITK | MedGemma

<h4>Project Results — Lumbar Disc Disease Detection</h4>

<p align="center">
  <img src="IN7.1.3.12.2.1107.5.2.46.174759.2025042215232592237339269_pred.png"
       alt="Sagittal MRI Disc Detection Example 1"
       width="32%" />
  <img src="IN7.1.3.12.2.1107.5.2.46.174759.2025050819132415023625248_pred.png"
       alt="Sagittal MRI Disc Detection Example 2"
       width="32%" />
  <img src="msg39090518-6461.jpg"
       alt="Axial MRI Disc Detection"
       width="32%" />
</p>

<p align="center">
  <em>AI-based lumbar disc detection and classification
  on sagittal and axial MRI images, with predicted
  pathology labels, bounding boxes, and confidence scores.</em>
</p>

-Automated Lumbar Vertebrae Segmentation & Classification Using Deep Learning

Developed an AI-powered lumbar spine MRI analysis system using a customized U-Net deep learning architecture for automated vertebral segmentation, identification, and anatomical classification. The model processes 2D sagittal MRI images and incorporates specialized strategies to address class imbalance and improve segmentation performance. An integrated classification head was designed to identify individual lumbar vertebrae and assign their corresponding anatomical levels (L1–L5). The system generates individual color-coded segmentation masks with anatomical labels, enabling automated vertebral localization and identification. This project demonstrates the application of Deep Learning, Medical Image Segmentation, Computer Vision, and Anatomical Structure Recognition to support quantitative spinal imaging analysis.

<h4>Automated Lumbar Spine MRI Analysis — Project Results</h4>

<p align="center">
  <img src="lumbar-mri.png"
       alt="Original Lumbar Spine MRI"
       width="46%" />
  <img src="lumbar-segmentation.png"
       alt="AI-Based Vertebral Segmentation and Classification"
       width="46%" />
</p>

<p align="center">
  <em>Original sagittal lumbar MRI (left) and
  AI-generated color-coded vertebral segmentation (right).</em>
</p>


Technologies: Deep Learning | Customized U-Net | Medical Image Processing | Semantic Segmentation | Multi-Class Classification | Lumbar Spine MRI
-AI-Assisted Goldmann Visual Field Analysis & Measurement Automation

Collaborated with an ophthalmology specialist on an AI-based medical image analysis project focused on Goldmann visual field perimetry. The project aimed to automate the interpretation and quantitative measurement of ophthalmic diagnostic charts using Computer Vision, Image Processing, and Artificial Intelligence. The proposed solution focused on identifying coordinate systems, detecting colored isopters and visual field boundaries, extracting geometric features, and supporting automated measurements of visual field extent and irregularities. The objective was to reduce time-consuming manual measurements, improve analytical consistency, and support ophthalmologists in clinical assessment through AI-assisted image analysis.

<h4>Goldmann Visual Field Analysis — Project Images</h4>

<p align="center">
  <img src="goldmann-original.png"
       alt="Original Goldmann Visual Field"
       width="46%" />
  <img src="goldmann-ai-analysis.png"
       alt="AI-Assisted Visual Field Analysis"
       width="46%" />
</p>

<p align="center">
  <em>Original visual field chart (left) and
  AI-assisted analysis (right).</em>
</p>

- Mammography AI pipeline — BI-RADS classification, 85–98% precision
- Spine MRI segmentation — 85% Dice/IoU
- Bone age estimation from MRI — ~3 month mean error (ages 7–14)
- Ophthalmology AI — retinopathy detection & fundus analysis
- 3D medical depth estimation (Depth Anything V2, DPT)
- Vision-Language Model evaluation (MedGEMMA, CLIP, BLIP)

### 🛢️ Petroleum AI
- MFL pipeline defect detection (YOLO, UNet, FCOS)

- Well log conversion: LAS/DLIS → SEG-Y
- AI-assisted fracture & corrosion detection

### 👁️ Computer Vision
- Object detection & segmentation (YOLO v3/v5/v8, UNet, RetinaNet, FCOS)
- Medical image processing (ITK, VTK, SimpleITK, MONAI)
- Cross-platform AI software (C++/Qt, C#, Python)

---

## 🛠️ Tech Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat&logo=pytorch&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat&logo=cplusplus&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat&logo=opencv&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat&logo=tensorflow&logoColor=white)

**Frameworks:** PyTorch · TensorFlow · ONNX · Scikit-learn · XGBoost  
**Vision:** YOLO · UNet · RetinaNet · FCOS · EfficientNet · SAM  
**Medical:** ITK · VTK · MONAI · pydicom · SimpleITK  
**Software:** Qt/C++ · C# WPF · Python APIs · DICOM/PACS integration  

---

## 🏛️ My Company

**[Apadana AI Research Center](https://github.com/Apadana-AI-Research-Center)**  
Independent AI research & development — Medical Imaging | Petroleum AI | Computer Vision

---


## 📚 Education

🎓 **MSc** — Photogrammetry & Image Processing, K.N. Toosi University (KNTU), 2006  
🎓 **BSc** — Surveying Engineering, K.N. Toosi University (KNTU), 2002  

---

*Open to research collaboration and AI development partnerships.*
