Chest X-Ray Pneumonia Detection using CNNs  
Comparative Study of Custom CNN and Transfer Learning Models  
Project Overview
Pneumonia is a serious respiratory infection that can be life-threatening if not diagnosed early.
This project focuses on building an automated deep learning system that classifies chest X-ray images into two categories: Normal and Pneumonia.
The main objective is to compare the performance of a Custom CNN model built from scratch with pre-trained transfer learning models (ResNet50, MobileNetV2) for medical image classification.
Additionally, this project explores Explainable AI (XAI) techniques such as Grad-CAM to improve model interpretability and support clinical decision-making.

Objectives
Develop a binary classification model for pneumonia detection  
Compare Custom CNN vs Transfer Learning models  
Handle class imbalance using class weighting techniques  
Improve sensitivity (recall) for pneumonia detection  
Apply explainability methods (Grad-CAM, SHAP)  
Build a reliable AI-based diagnostic support system  

Dataset Information

Dataset Name: Chest X-Ray Images (Pneumonia)  
Source:Kaggle (Paul Timothy Mooney)  
Link: https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia  

Dataset Structure:
Train/
├── NORMAL/
└── PNEUMONIA/

Validation/
├── NORMAL/
└── PNEUMONIA/

Test/
├── NORMAL/
└── PNEUMONIA/

 Dataset Details

- Total Images:5,856
- Classes:2 (Binary Classification)
  - NORMAL
  - PNEUMONIA
- Image Type: Chest X-ray (Grayscale → Converted to RGB)
- Image Size:224 × 224 pixels
- Format: Digital medical radiographs (AP view)

Class Distribution

| Data Split   | Normal | Pneumonia | Total |
|--------------|--------|-----------|-------|
| Training     | 1,341  | 3,875     | 5,216 |
| Validation   | 8      | 8         | 16    |
| Testing      | 234    | 390       | 624   |
| Total        | 1,583  | 4,273     | 5,856 |

 Models Used

Custom CNN (From Scratch)
- Built using sequential convolutional layers
- Designed for baseline comparison
- Learns features directly from data

Transfer Learning Models
- ResNet50
- MobileNetV2
- Pre-trained on ImageNet dataset
- Fine-tuned for medical classification
- 
 Preprocessing Steps

- Image resizing to 224 × 224 pixels  
- Normalization of pixel values  
- Grayscale → RGB conversion  
- Real-time data augmentation (if applied)  
- Batch-wise loading using Image Data Generators  

 Evaluation Metrics

- Accuracy  
- Precision  
- Recall (very important for pneumonia detection)  
- F1-Score  
- Confusion Matrix  

Research Questions

- RQ1: Can a custom CNN detect subtle lung opacities compared to transfer learning models?  
- RQ2:How does class weighting reduce bias in imbalanced datasets?  
- RQ3:Do Grad-CAM and SHAP explanations align with clinical lung regions?  

 Expected Results

 Transfer learning models (ResNet50, MobileNetV2) are expected to outperform the custom CNN  
 Faster convergence and better feature extraction from pre-trained models  
 Improved recall for pneumonia detection  
 Custom CNN may underperform due to limited feature learning capacity  
 XAI methods will improve model interpretability  

 Technologies Used

- Python  
- TensorFlow / Keras  
- NumPy, Pandas  
- Matplotlib, Seaborn  
- OpenCV  
- Scikit-learn  

 Future Improvements

- Integration into a web-based diagnostic tool  
- Deployment using Flask or Streamlit  
- Use of attention-based deep learning models  
- More advanced explainability methods
   
Conclusion
This project demonstrates the effectiveness of deep learning for automated pneumonia detection from chest X-ray images. The comparative study highlights the superiority of transfer learning models while emphasizing the importance of interpretability and class imbalance handling in medical AI systems.
Chest-XRay-Pneumonia-Detection/
│
