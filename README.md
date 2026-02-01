# EuroSAT Image Classification using FastAI and ResNet18

## 📌 Project Overview
This project focuses on classifying satellite images from the EuroSAT dataset using a deep learning model (ResNet18) implemented with the FastAI library.  
The dataset contains multispectral satellite images with 13 spectral bands captured by the Sentinel-2 satellite.  
For visualization and training with ResNet18, RGB bands are extracted from the multispectral images.

---

## 🛠️ Libraries Used

The following libraries are used in this project:

- **pandas** – for data cleaning, manipulation, and loading CSV files  
- **tifffile** – for reading multispectral satellite images in `.tif` format  
- **numpy** – for numerical operations and handling image tensors  
- **matplotlib** – for visualizing satellite images  
- **fastai** – for building, training, and fine-tuning the deep learning model (ResNet18)

---

## 📂 Dataset Description

The EuroSAT dataset is organized as follows:

- `train.csv` – contains image filenames and their corresponding labels used for training  
- `validation.csv` – used to validate model performance during training  
- `test.csv` – used for final evaluation of the trained model  
- `label_map.json` – maps class names to numeric labels  
- Image files (`.tif`) – multispectral satellite images stored in class-based folders  

Each image has the shape `(64, 64, 13)` representing height, width, and 13 spectral bands.

---

## 🔄 Workflow

1. **Import Required Libraries**  
   Libraries such as pandas, tifffile, numpy, matplotlib, and fastai are imported to handle data processing, visualization, and deep learning tasks.

2. **Load CSV Files**  
   The training, validation, and testing datasets are loaded using pandas.

3. **Read Satellite Images**  
   Multispectral `.tif` images are loaded using the tifffile library and converted into NumPy arrays.

4. **Preprocess Images**  
   RGB bands (bands 4, 3, and 2) are extracted from the 13-band images and normalized for visualization and model input.

5. **Create DataLoaders**  
   FastAI DataBlock and DataLoaders are created using image paths and labels from the CSV files.

6. **Model Training (Fine-tuning ResNet18)**  
   A pretrained ResNet18 model is fine-tuned on the EuroSAT dataset using FastAI’s `cnn_learner`.

7. **Evaluation**  
   The trained model is evaluated using the test dataset to measure classification accuracy.

8. **Prediction**  
   The model can be used to predict the class of new satellite images.

---

## 🎯 Objective
The main objective of this project is to build an accurate satellite image classification model using deep learning and to demonstrate how multispectral satellite data can be processed and visualized using Python and FastAI.

---

## ✅ Key Features
- Supports multispectral satellite image data  
- Uses FastAI for rapid model development  
- Fine-tunes a pretrained ResNet18 model  
- Provides visualization of satellite images  
- Evaluates model performance using separate validation and test sets  

---

## 📌 Conclusion
This project demonstrates an end-to-end workflow for satellite image classification using the EuroSAT dataset.  
By leveraging FastAI and ResNet18, the model efficiently learns patterns from satellite images and classifies land cover types such as forests, rivers, residential areas, and more.

---
