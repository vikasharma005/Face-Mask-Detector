# Face Mask Detector
[![Python](https://img.shields.io/badge/Python-3.9-blue.svg)](https://www.python.org/) 
[![Keras](https://img.shields.io/badge/Keras-2.4.3-orange.svg)](https://keras.io/) 
[![OpenCV](https://img.shields.io/badge/OpenCV-4.5.1-green.svg)](https://opencv.org/) 

A **real-time face mask detection system** using a convolutional neural network (CNN). This project detects whether a person is wearing a mask or not from live video feed or images.

---

## 🚀 Features
- **Real-Time Detection**: Detects faces and classifies them as "With Mask" or "Without Mask".
- **Data Augmentation**: Enhances training dataset with transformations like rotation, zoom, and flipping.
- **User-Friendly Interface**: Visualizes detection results with bounding boxes and color-coded labels.
- **Customizable**: Easy to modify for different datasets or detection tasks.

---

## 📂 Project Structure
```plaintext
Face-Mask-Detector/
├── train.py          # Script to train the mask detection model
├── test.py           # Script to test the model with live video feed
├── model-010.h5      # Pre-trained model file
├── train/            # Training dataset directory
├── test/             # Testing dataset directory
├── README.md         # Project documentation
```

---

## 🛠️ Prerequisites
Ensure you have the following installed:
1. **Python 3.6+**
2. **Keras**
3. **TensorFlow**
4. **OpenCV**
5. **Numpy**

Install dependencies with:
```bash
pip install -r requirements.txt
```

---

## ⚙️ Setup

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/Face-Mask-Detector.git
   cd Face-Mask-Detector
   ```

2. **Prepare Dataset**:
   - Place your **training dataset** in the `train/` folder.
   - Place your **testing dataset** in the `test/` folder.
   - The dataset should have two subdirectories: `mask/` and `no_mask/`.

3. **Train the Model**:
   Run the `train.py` script to train the model:
   ```bash
   python train.py
   ```

4. **Test the Model**:
   Use the `test.py` script to run real-time detection:
   ```bash
   python test.py
   ```

---

## 📊 Model Details
The CNN architecture includes:
- **Two Convolutional Layers** with 100 filters each.
- **MaxPooling** layers to reduce spatial dimensions.
- **Dropout** for regularization.
- Fully connected **Dense** layers for classification.

Loss function: `binary_crossentropy`  
Optimizer: `adam`  
Metrics: `accuracy`  

---

## 🧪 Data Augmentation
The training data is augmented with:
- **Rotation**: up to ±40 degrees.
- **Zoom**: range of 20%.
- **Shifts**: Horizontal and vertical by 20%.
- **Flipping**: Horizontal flips.

This improves model robustness and prevents overfitting.

---

## 📈 Training
The model trains for **10 epochs** with `ImageDataGenerator` for augmentation.

Example command:
```bash
python train.py
```

---

## 🖥️ Usage Instructions
1. Run the detection system:
   ```bash
   python test.py
   ```
2. Press `Esc` to exit the live detection window.

---

## 📂 Dataset Example
Your dataset structure should look like:
```plaintext
train/
├── mask/
│   ├── image1.jpg
│   ├── image2.jpg
│   ...
├── no_mask/
│   ├── image1.jpg
│   ├── image2.jpg
│   ...

test/
├── mask/
├── no_mask/
```

---

## 🤝 Contributing
Contributions are welcome! Feel free to submit a PR or open an issue.

---

## 🛡️ License
This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).

---

## 📧 Contact
For any queries or issues, reach out to:
- **Email**: vikas.sharma005@protonmail.com
- **GitHub**: [vikasharma005](https://github.com/vikasharma005)
```
