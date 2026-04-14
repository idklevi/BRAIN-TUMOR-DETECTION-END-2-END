<div align="center">

# 🧠 Brain Tumor Detection — End to End

> A deep learning project that classifies brain tumors from MRI scans into three types using a fine-tuned ResNet50 model.  
> Built as a complete pipeline — from raw dataset preprocessing to a working Flask web app.

</div>

---

## ⚠️ Medical Disclaimer

This project is for **educational purposes only**.  
It should not be used for medical diagnosis. Always consult a qualified medical professional.

---

## 🔬 About the Project

This project explores how deep learning can be applied to classify brain tumors using MRI scans.

Instead of training a model from scratch, I used **transfer learning with ResNet50** and fine-tuned it on a brain tumor dataset to improve performance with limited data.

What makes this project “end-to-end” is that it doesn’t stop at model training. It includes:
- Data preprocessing from raw `.mat` files  
- Model training and evaluation  
- A Flask web app for real-time predictions  

---

## ⚙️ How It Works

1. User uploads an MRI image  
2. Image is preprocessed (resized, normalized)  
3. Model predicts tumor type  
4. Result + confidence score is displayed  

Classes:
- Glioma  
- Meningioma  
- Pituitary  

---

## 📊 Dataset

- Source: Figshare (Jun Cheng dataset)  
- Total images: 3,064  
- Format: `.mat` → converted to `.jpg`  
- Task: 3-class classification  

⚠️ Note:
- Dataset is relatively small  
- Class imbalance exists (glioma > meningioma)  

---

## 🏗️ Model

- Base model: ResNet50 (pretrained on ImageNet)  
- Approach: Transfer learning + fine-tuning  
- Final layer modified for 3-class classification  

---

## 📈 Performance

- Accuracy: ~99% (on test split)

⚠️ Important:
- High accuracy does not guarantee real-world reliability  
- Model is trained on a limited dataset  

---

## 🖥️ Application

A simple Flask web app allows users to:
- Upload MRI images  
- Get predictions instantly  

---

## 🚀 Running the Project

```bash
git clone https://github.com/idklevi/BRAIN-TUMOR-DETECTION-END-2-END-.git
cd "BRAIN TUMOR DETECTION [END 2 END]"

python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate on Windows

pip install -r requirements.txt
python app.py