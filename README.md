# 🧠 Brain MRI Tumor Segmentation using U-Net

This project builds a deep learning model to segment brain tumors from MRI scans using a U-Net architecture. The model is trained on paired MRI images and their corresponding tumor segmentation masks.

---

## 📂 Dataset

- **Source**: [Brain Tumor Dataset (Kaggle)](https://www.kaggle.com/datasets/tinashri/brain-tumor-dataset-includes-the-mask-and-images)
- **Images folder**: Contains MRI scan images.
- **Masks folder**: Contains binary segmentation masks for the tumors.
- All files are named consistently (e.g., `1.png`, `10.png`, etc.).

> Total images: 3064  
> Input shape: Resized to 256x256  
> Mask format: Binary (0 = background, 1 = tumor)

---

## 🧠 Model Architecture

- **Model**: U-Net (implemented using TensorFlow/Keras)
- **Loss Function**: Binary Crossentropy
- **Optimizer**: Adam
- **Post-processing**:
  - Morphological closing
  - Connected component filtering (keep only largest tumor region or threshold-based cleanup)
- **Overlay**: Tumor segmentation results are overlaid on MRI images with a green mask for visualization.

---

## 🔍 Inference on New Image

- Upload any MRI image during runtime.
- The model performs tumor segmentation and overlays the predicted mask.

---

## 🧪 Results

| Metric              | Training Set | Validation Set   |
|---------------------|--------------|------------------|
| Accuracy            | **98.60%**    | **98.58%**      |
| Binary Crossentropy | **0.042**     | **0.043**       |

---

## 🚀 How to Use

1. **Mount Google Drive** to access `images/` and `masks/` folders.
2. **Preprocess** images and masks:
   - Resize to 256×256
   - Normalize pixel values to [0, 1]
3. **Train the model** using the provided U-Net architecture.
4. **Predict** tumor masks for validation or new input images.
5. **Post-process** predictions to remove noise and small patches.
6. **Visualize** masks overlaid on MRI scans with customizable color.

---

## 📦 Requirements

```bash
tensorflow
opencv-python
numpy
matplotlib
scikit-learn
```

---

### To get the trained .h5 model file, feel free to contact me:
📧 k.prabhav2005@gmail.com
