# Dogs vs. Cats Image Classification using CNN

This repository contains a Deep Learning project that classifies images of dogs and cats using a Convolutional Neural Network (CNN). The model is built using **TensorFlow/Keras** and achieves high accuracy through structured preprocessing and a deep stacked CNN architecture.

## 🚀 Project Overview
The goal of this project is to build a robust binary classifier capable of distinguishing between feline and canine images. The pipeline involves:
* **Data Cleaning:** Shuffling and filtering out corrupted or non-image files.
* **EDA:** Visualizing class distributions and sample images.
* **Deep Learning:** Building and training a custom CNN with multiple convolutional and pooling layers.
* **Prediction:** A script to test the model on individual local images.

## 📊 Dataset
The model is trained on the classic **Dogs vs. Cats dataset** (Kaggle). 
* **Total Images:** ~25,000
* **Classes:** 0 for Cat, 1 for Dog.
* **Preprocessing:** All images are resized to `128x128` pixels and normalized to a range of `[0, 1]`.

## 🛠️ Tech Stack
* **Language:** Python
* **Libraries:** * `TensorFlow` & `Keras` (Model building)
    * `Pandas` & `NumPy` (Data manipulation)
    * `Matplotlib` (Visualization)
    * `PIL` (Image processing)
    * `tqdm` (Progress tracking)

## 🧠 Model Architecture
The CNN consists of several blocks designed to extract complex spatial features:
1.  **Input Layer:** 128x128 RGB images.
2.  **Feature Extraction:**
    * 4 Convolutional Layers with increasing filters (32, 64, 128, 128).
    * Max Pooling layers after each convolution to reduce dimensionality.
3.  **Classification Head:**
    * Flatten Layer.
    * Dense Layer (512 units) with ReLU activation.
    * Output Layer (1 unit) with **Sigmoid activation** for binary classification.

## ⚙️ Installation & Usage
1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/your-username/dogs-vs-cats-cnn.git](https://github.com/your-username/dogs-vs-cats-cnn.git)
    cd dogs-vs-cats-cnn
    ```
2.  **Organize Data:**
    Ensure your images are stored in a `PetImages/` directory with subfolders `Cat/` and `Dog/`.
3.  **Run the Notebook:**
    Open `Dogs vs Cats CNN.ipynb` in Jupyter or Google Colab and run all cells.
4.  **Testing a Custom Image:**
    Use the prediction block at the end of the notebook:
    ```python
    image_path = "your_image.jpg"
    # ... preprocessing ...
    pred = model.predict(img)
    label = 'Dog' if pred[0] > 0.5 else 'Cat'
    ```

## 📈 Results
The model utilizes a validation split to monitor performance. Final accuracy and loss plots are generated at the end of the training cycle to visualize the learning curve.

---
*Developed as a demonstration of Computer Vision and Deep Learning workflows.*
