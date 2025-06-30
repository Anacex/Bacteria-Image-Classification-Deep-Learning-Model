# 🔬 Deep Learning Project: Bacteria Colony Classification

This project builds a deep learning model using **EfficientNetB0** to classify images of bacteria colonies into 33 different classes. It uses a small, imbalanced custom dataset sourced from Kaggle and applies data preprocessing, transfer learning, and fine-tuning strategies.

---

## 📁 Dataset

- The dataset was downloaded from Kaggle using API authentication.
- Some corrupt images were removed during preprocessing.
- Images are resized to **224x224** and normalized.
- Data augmentation is applied to improve generalization.

## 💡 Highlights

- EfficientNetB0-based image classifier
- Trained on 33-class bacterial dataset
- Applied transfer learning and fine-tuning
- Visualized training results (accuracy/loss curves)


## 🧠 Model Architecture

The model is based on **EfficientNetB0** (from `keras.applications`) with the following structure:

```
Input Image (224x224x3)
↓
EfficientNetB0 (frozen/unfrozen based on phase)
↓
GlobalAveragePooling2D
↓
Dense(128, ReLU)
↓
Dropout(0.3)
↓
Dense(33, Softmax)
```

---

## 📈 Training Phases

### Phase 1:
- Base EfficientNetB0 used with frozen weights.
- Initial results:
  - Training Accuracy: ~14.5%
  - Validation Accuracy: ~3–5%
  - Interpretation: Overfitting due to small dataset.

### Phase 2:
- Enhanced Data Augmentation
- Fine-tuned last 100 layers of EfficientNet
- Trained for 50 epochs
- Improved performance through better generalization

---

## 🧪 Tools and Libraries

- Python, TensorFlow/Keras
- Streamlit (for GUI)     --Not proceeded with as the model was for leaning purposes and did not achieve deployable results- Streamlit (for GUI)

> ⚠️ *Note: Streamlit integration was initially planned, but not completed as the model was for learning purposes and did not achieve deployable results.*

- Kaggle API (for dataset download)
- Google Colab

---

## 🚀 Streamlit Web App

- Users can upload an image via a simple interface.
- The app loads the trained model and outputs predicted class.
- Can be deployed on Streamlit Cloud or localhost.

---

## 📸 Sample Results
![Accuracy Curves](image.png)
*Accuracy improves but fluctuates due to small dataset*
![Loss Curves](image-1.png)
*Training loss decreases; validation loss shows overfitting*



---

## 📂 Folder Structure
```
📦 project/
├── DLP_proj.ipynb           # Main notebook
├── model.h5                 # Trained model file
├── requirements.txt         # Required packages
└── README.md                # This file
```

---

## 📜 License

This project is licensed under the [MIT License](LICENSE).

---

## ✍️ Author

**Muhammad Anas Khan**  
Connect on [LinkedIn](https://www.linkedin.com/in/muhammad-anas-khan-k224170/) • [GitHub](https://github.com/Anacex)
