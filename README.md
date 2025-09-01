# Face Mask Detection using YOLOv5 & YOLOv7  

*A deep learning project for real-time mask compliance detection.*  

---

## Introduction  
In the wake of COVID-19, automatic detection of face mask usage became a crucial public health application.  
This project explores **YOLOv5** and **YOLOv7** object detection models to identify:  
- ✅ With Mask  
- ❌ Without Mask  
- ⚠️ Mask Worn Incorrectly  

The system aims to provide an efficient tool for enhancing safety in public environments.  

---

## Dataset  
- **Source**: [Kaggle – Face Mask Detection Dataset](https://www.kaggle.com/datasets/andrewmvd/face-mask-detection)  
- **Annotations**: Pascal VOC (XML), converted to YOLO (TXT).  
- **Classes**: 3 (`with_mask`, `without_mask`, `mask_weared_incorrect`).  
- **Size**: ~853 annotated images.  
- **Preprocessing**: XML → TXT conversion, grayscale examples, train/val/test split.  

---

## Methodology  

### Data Preparation  
- Converted VOC XML annotations → YOLO TXT format.  
- Created directory structure for YOLO training (train/val/test).  
- Generated `data.yaml` configuration file with class names.  

### Models  
- **YOLOv7**  
  - Trained for 50 epochs (batch size = 16).  
  - Configured with custom dataset and hyperparameters.  
  - Evaluated on unseen test images.  

- **YOLOv5**  
  - Trained for 50 epochs with transfer learning (`yolov5s.pt`).  
  - Same dataset and splits for fair comparison.  

---

## Results  

- **YOLOv7**:  
  - Higher **precision, recall, and mAP** compared to YOLOv5.  
  - More robust to occlusion, lighting variations, and mask placement.  
  - Faster convergence during training.  

- **YOLOv5**:  
  - Strong baseline with decent accuracy.  
  - Slightly lower detection performance compared to YOLOv7.  


