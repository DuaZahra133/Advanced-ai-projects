# Transfer Learning Flowers Classifier

## Project Overview
This project demonstrates a ** image classification model** using **transfer learning**, **data augmentation**, and **fine-tuning** on the built-in `tf_flowers` dataset. The goal is to classify images of flowers into **5 categories**: Daisy, Dandelion, Roses, Sunflowers, and Tulips.

---

## Dataset
- Built-in **TensorFlow `tf_flowers` dataset**  
- 5 Classes: Daisy, Dandelion, Roses, Sunflowers, Tulips  
- Dataset automatically downloaded and loaded via **TensorFlow Datasets**  
- Images are preprocessed to **224x224** and normalized  

---

## Model Architecture
- **Base model:** VGG16 pretrained on ImageNet (top layers removed)  
- **Data augmentation layer:** Random flips, rotations, zoom, contrast adjustment  
- **Classifier:**  
  - GlobalAveragePooling2D  
  - Dense layer (128 units, ReLU)  
  - Dropout (0.5)  
  - Output layer (Dense(NUM_CLASSES, softmax))  

---

## Training
- **Feature Extraction:** Train classifier only, 5 epochs  
- **Fine-Tuning:** Unfreeze last few layers of VGG16, 5 epochs  
- **Optimizer:** Adam  
- **Batch Size:** 16  
- **Image Size:** 224x224  

---

## Results
- Achieved good **training and validation accuracy** on a small dataset  
- Plots of **accuracy & loss curves** included  

---

## Project Structure
