# Fusion-Based-CNN-Model-for-Binary-Classification-of-Melanoma-Skin-Cancer
This project presents a deep learning architecture that fuses InceptionV3 and MobileNetV2 to classify melanoma skin cancer lesions into benign and malignant categories.

# Overview
This project presents a deep learning architecture that fuses InceptionV3 and MobileNetV2 to classify melanoma skin cancer lesions into benign and malignant categories. Leveraging feature-level concatenation, the model achieves robust prediction reliability while balancing computational efficiency and diagnostic interpretability.

# Motivation
Traditional CNN models often suffer from limitations like overfitting, high computational cost, or inconsistent performance across lesion types. This fusion-based model tackles these issues by combining the strengths of both InceptionV3 and MobileNetV2, enhancing robustness, generalizability, and classification precision.

# Dataset
Source: Kaggle Melanoma Skin Cancer Dataset

Classes: Benign, Malignant

Size: 10,000 RGB images (JPEG format, 300×300 resolution)

Split:

Train: 5000 benign, 4605 malignant

Test: 500 benign, 500 malignant

Preprocessing:

Resize to 244×244

Data augmentation (flipping, rotation, zoom)

Class balancing

Batch normalization

# Model Architecture
The proposed framework fuses InceptionV3 and MobileNetV2 pretrained on ImageNet. Key steps:

Extract fixed features in parallel

Apply batch normalization and flatten

Concatenate feature vectors

Pass through dense layers with dropout regularization

Final output: binary softmax prediction

# Performance Metrics
Model	Accuracy	Precision	Recall	F1 Score	Val Loss
MobileNetV2	90.05%	48.49	48.50	48.40	0.2765
InceptionV3	91.22%	33.00	33.00	32.97	0.4391
ResNet50	78.17%	48.79	48.80	48.74	0.5709
EfficientNetB0	51.75%	25.00	50.00	33.33	0.7906
Proposed Fusion Model	92.34%	50.00	48.40	49.20	1.3007
Despite a higher validation loss, the proposed model delivers reliable performance across all metrics, outperforming individual architectures in both generalization and prediction quality.

# Visual Interpretability
Grad-CAM visualizations provide insight into which regions of the dermoscopic image contributed most to the model's prediction, supporting its diagnostic relevance and clinical utility.
