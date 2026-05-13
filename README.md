# Harmful Object Detection

A deep learning project for detecting harmful objects using Faster R-CNN object detection model. This repository contains the implementation, model training, and evaluation of a harmful object detection system.

## 📋 Project Overview

This project implements an object detection system using **Faster R-CNN** architecture to identify and localize harmful objects in images and video streams. The model is trained on a custom dataset and provides high-confidence predictions with bounding box coordinates.

## 🎥 Demo Video

Watch the detection results in action:

<video width="640" height="480" controls>
  <source src="output.mp4">
  Your browser does not support the video tag.
</video>

## 📂 Repository Structure

```
harmful-object-detection/
├── README.md                                    # Project documentation
├── main_faster_rcnn.ipynb                      # Main Jupyter notebook with model training
├── output.mp4                                   # Detection results video demo
├── clideo_editor_ddfe959f4c6a471f87b34cdb90fd9af4.mp4  # Additional demo video
├── 1147834_720.jpg                             # Sample detection image
├── results.json                                 # Detection results in COCO format
└── .gitignore                                  # Git ignore file
```

## 📊 Files Description

### Core Implementation
- **main_faster_rcnn.ipynb** (3.4 MB)
  - Complete Jupyter notebook with model implementation
  - Data preparation and preprocessing
  - Faster R-CNN model training
  - Model evaluation and inference
  - Results visualization

### Detection Results
- **results.json** (114 KB)
  - Detection predictions in COCO format
  - Contains 200+ detection entries across 35+ images
  - Each entry includes: image_id, category_id, bounding box coordinates, and confidence score
  - Confidence scores range from 0.5 to 0.99+

### Demo Files
- **output.mp4** (4.2 MB)
  - Video demonstration of the detection system
  - Real-time object detection on video frames
  - Shows bounding boxes and confidence scores

- **clideo_editor_ddfe959f4c6a471f87b34cdb90fd9af4.mp4** (1.8 MB)
  - Additional demo video file
  - Alternative demonstration of model performance

- **1147834_720.jpg** (53 KB)
  - Sample image with detected objects
  - Visual reference for detection results

## 🔍 Detection Categories

Based on the results.json file, the model detects **6 object categories** (IDs 1-6):

| Category ID | Detections |
|------------|-----------|
| 1 | Bomb |
| 2 | Fire |
| 3 | Hand Gun |
| 4 | Knife |
| 5 | Rifle |
| 6 | Smoke |

## 📈 Model Performance

### Detection Statistics
- **Total Detections**: 200+ predictions across test set
- **Test Images**: 35+ images evaluated
- **Average Confidence**: ~0.80+ (high-confidence predictions)
- **Confidence Range**: 0.51 - 0.99
- **Bounding Box Format**: [x, y, width, height]

### Sample Detection Metrics
- Highest confidence detection: **0.9953** (image_id: 33)
- Multiple high-confidence (>0.98) detections across dataset
- Consistent multi-object detection (multiple objects per image)

## 🚀 Getting Started

### Requirements
The project uses standard deep learning libraries:
- PyTorch
- torchvision (includes Faster R-CNN)
- jupyter
- numpy
- matplotlib
- opencv-python

### Usage

1. **Clone the repository**
   ```bash
   git clone https://github.com/AurumNuraga/harmful-object-detection.git
   cd harmful-object-detection
   ```

2. **Install dependencies**
   ```bash
   pip install torch torchvision jupyter numpy matplotlib opencv-python
   ```

3. **Run the notebook**
   ```bash
   jupyter notebook main_faster_rcnn.ipynb
   ```

4. **View results**
   - Check `output.mp4` for video demonstration
   - View `results.json` for detailed detection predictions
   - See `1147834_720.jpg` for sample visualizations

## 📝 Output Format

The `results.json` file follows the COCO detection format:

```json
{
  "image_id": 0,
  "category_id": 4,
  "bbox": [x, y, width, height],
  "score": 0.9777662754058838
}
```

- **image_id**: Index of the image in test set
- **category_id**: Object category (1-6)
- **bbox**: Bounding box [x, y, width, height]
- **score**: Confidence score (0-1)

## 🎯 Model Architecture

**Faster R-CNN**
- Pre-trained on COCO dataset
- Fine-tuned on custom harmful objects dataset
- Two-stage detector (Region Proposal Network + Classification)
- Optimized for accuracy and speed

## 📦 Ignored Files

The following files are listed in `.gitignore`:
- `dataset.zip` - Training dataset (compressed)
- `*.zip` - Compressed archives
- `*.pth`, `*.pt` - Pre-trained model weights
- `__pycache__/` - Python cache files
- `.ipynb_checkpoints/` - Jupyter checkpoints

## 🔧 Key Technologies

- **Framework**: PyTorch
- **Computer Vision**: torchvision
- **Model**: Faster R-CNN
- **Format**: COCO Detection Format
- **Development**: Jupyter Notebook

## 📊 Data Processing

The project pipeline includes:
1. Image loading and preprocessing
2. Model inference
3. Detection postprocessing
4. Bounding box generation
5. Results serialization to JSON
6. Video rendering with annotations

## 🎓 Learning Resources

This project demonstrates:
- Object detection with deep learning
- Using pre-trained models from torchvision
- Custom dataset fine-tuning
- COCO format for detection results
- Video processing and annotation
- Python data science workflow

## 📄 License

This project is provided as-is for educational and research purposes.

## 👤 Author

**AurumNuraga**

---

**Last Updated**: May 13, 2026

For more information or issues, please visit the [GitHub repository](https://github.com/AurumNuraga/harmful-object-detection).
