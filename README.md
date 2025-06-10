# 🖼️ Image Inpainting with U-Net (CelebA Dataset)

This project showcases **image inpainting** using a deep learning model trained on the **CelebA facial image dataset**. A U-Net-like architecture is used to reconstruct masked portions of facial images.

> 🧪 **This project was developed and run in a Google Colab environment.**

---

## 📁 Dataset

* **Dataset:** CelebFaces Attributes Dataset (CelebA)
* **Source:** [http://mmlab.ie.cuhk.edu.hk/projects/CelebA.html](http://mmlab.ie.cuhk.edu.hk/projects/CelebA.html)
* **Direct Download (Google Drive):** [https://drive.google.com/uc?id=0B7EVK8r0v71pZjFTYXZWM3FlRnM](https://drive.google.com/uc?id=0B7EVK8r0v71pZjFTYXZWM3FlRnM)
* **Used:** 20,000 aligned and cropped images (128x128)

---

## 📌 Project Highlights

* ✅ Custom U-Net for image inpainting
* ✅ Trains on 20,000 CelebA images
* ✅ Automatically applies random rectangular masks
* ✅ Visualizes predictions vs ground truth
* ✅ Live Gradio demo for testing with adjustable masks

---

## 🧠 Model Architecture

The U-Net model is composed of:

* **Encoder:** Conv2D + MaxPooling layers
* **Bottleneck:** Deeper features + Dropout
* **Decoder:** Conv2DTranspose + skip connections
* **Output:** 128×128×3 image (sigmoid activation)

---

## 🧪 Training Setup

* **Framework:** TensorFlow / Keras
* **Loss:** Binary Crossentropy
* **Optimizer:** Adam
* **Epochs:** 50
* **Batch Size:** 32
* **Early Stopping & LR Scheduler** included
* **Augmentation:** Random square mask applied on-the-fly

---

## 📊 Results

Training/validation **loss** and **accuracy** are plotted. The model outputs are compared side-by-side:

* **Original Image**
* **Masked Input**
* **Predicted Inpainting Output**

---

## 🚀 Gradio Demo: Try It Yourself

Launch the interactive demo using Gradio:

```python
interface.launch()
```

* Upload a face image (128×128 recommended)
* Adjust sliders to control mask location
* View original, masked, and inpainted versions

---

## 📦 Installation

Install dependencies via pip:

```bash
pip install -U gradio gdown opencv-python-headless tensorflow tqdm
```

## 📸 Sample Output

![Output](sample_outputs/sample-output.png)

---

## ✍️ Author

* 💻 Project by: *Omar Maged*

---

## 📜 License

Licensed under the MIT License.
