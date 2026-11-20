# 🌿 Plant Leaf Disease Classification Using CNN

## 1. Project Overview

**Project Domain:** Agriculture | Artificial Intelligence | Deep Learning

Plant Leaf Disease Classification is a deep learning project developed to identify plant leaf diseases from images using a Convolutional Neural Network (CNN).

The system classifies uploaded leaf images into 15 different categories, including healthy and diseased leaves of pepper, potato and tomato plants.

A Streamlit web application is also developed to allow users to upload leaf images and obtain the predicted class with its confidence score.

## 2. Problem Statement

Plant diseases can negatively affect agricultural productivity and crop quality. Identifying diseases manually through visual inspection can be time-consuming.

This project aims to develop an automated image classification system that can recognise different plant leaf conditions using deep learning.

## 3. Objectives

- Develop a CNN-based plant leaf disease classification model.
- Classify plant leaf images into 15 categories.
- Preprocess and prepare the dataset for model training.
- Evaluate the model using appropriate classification metrics.
- Develop a user-friendly Streamlit application for predictions.

## 4. Dataset Description

**Dataset Name:** PlantVillage

**Source:** Kaggle – [PlantVillage Dataset](https://www.kaggle.com/datasets/emmarex/plantdisease)

**Dataset Identifier:** `emmarex/plantdisease`

| Dataset Information | Details |
|---|---:|
| Total Images | 20,638 |
| Number of Classes | 15 |
| Original Image Size | 256 × 256 |
| Model Input Size | 128 × 128 |
| Training Images | 16,511 |
| Validation Images | 4,127 |
| Split Ratio | 80:20 |

The dataset contains healthy and diseased leaf images belonging to pepper, potato and tomato plants.

The dataset is not included in this repository. Refer to `data/README.md` for dataset details.

## 5. Technology Stack

| Technology | Purpose |
|---|---|
| Python | Programming language |
| TensorFlow | Deep learning framework |
| Keras | CNN model development |
| NumPy | Numerical operations |
| Matplotlib | Data visualisation |
| Scikit-learn | Model evaluation |
| Streamlit | Web application |
| Google Colab | Model development and training |

## 6. System Architecture

The project follows the workflow below:

1. Dataset collection
2. Image loading and preprocessing
3. Image resizing and normalisation
4. Training and validation split
5. CNN model construction
6. Model training
7. Model evaluation
8. Model saving
9. Streamlit application development
10. Image upload and disease prediction

## 7. CNN Model Architecture

The CNN model uses the following layers:

| Layer | Configuration |
|---|---|
| Input | 128 × 128 × 3 |
| Rescaling | 1/255 |
| Conv2D | 32 filters, 3 × 3, ReLU |
| MaxPooling2D | 2 × 2 |
| Conv2D | 64 filters, 3 × 3, ReLU |
| MaxPooling2D | 2 × 2 |
| Conv2D | 128 filters, 3 × 3, ReLU |
| MaxPooling2D | 2 × 2 |
| Flatten | — |
| Dense | 128 neurons, ReLU |
| Dropout | 0.5 |
| Output | 15 neurons, Softmax |

**Optimizer:** Adam  
**Loss Function:** Sparse Categorical Crossentropy  
**Batch Size:** 32  
**Training Epochs:** 10

## 8. Installation and Configuration

### Step 1: Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/Plant-Leaf-Disease-Classification.git
```

### Step 2: Navigate to the project directory

```bash
cd Plant-Leaf-Disease-Classification
```

### Step 3: Install dependencies

```bash
pip install -r requirements.txt
```

### Step 4: Prepare the trained model

Place the following files inside the `models/` directory:

- `plant_leaf_disease_model.keras`
- `class_names.txt`

The trained model file may be hosted separately if it exceeds GitHub's regular upload limit. Follow the model download instructions in the repository if applicable.

## 9. Running the Application

Run the following command:

```bash
streamlit run app.py
```

Open the local URL displayed in the terminal.

1. Upload a plant leaf image.
2. Click the **Predict Disease** button.
3. View the predicted disease category.
4. View the prediction confidence score.

Supported image formats: JPG, JPEG and PNG.

## 10. Model Evaluation and Results

The model was trained for 10 epochs and evaluated on 4,127 validation images.

### Evaluation Metrics

| Metric | Result |
|---|---:|
| Training Accuracy | 88.25% |
| Validation Accuracy | 91.98% |
| Training Loss | 0.3281 |
| Validation Loss | 0.2574 |
| Weighted Precision | 0.92 |
| Weighted Recall | 0.92 |
| Weighted F1-Score | 0.92 |
| Macro Average F1-Score | 0.88 |

The model achieved **91.98% validation accuracy** across 15 plant leaf categories.

### Sample Prediction

A sample image prediction produced:

- **Predicted Class:** Tomato_healthy
- **Confidence:** 99.99%

This represents one individual prediction and not the overall model accuracy.

## 11. Screenshots and Results

The `results/screenshots/` folder is intended to contain:

- Training accuracy and loss graphs
- Confusion matrix
- Classification report
- Streamlit application interface
- Sample prediction output

## 12. Limitations

- The model is trained on the PlantVillage dataset and may not perform equally well on images captured under different real-world conditions.
- Classification performance varies across categories.
- The model can predict only the 15 categories included in its training dataset.
- Predictions should not be considered a replacement for expert agricultural diagnosis.

## 13. Future Improvements

- Include more diverse real-world plant images.
- Apply data augmentation techniques.
- Experiment with transfer learning models such as MobileNetV2 and EfficientNet.
- Improve performance on weaker classification categories.
- Deploy the application on a cloud platform.

## 14. Project Repository Structure

```text
Plant-Leaf-Disease-Classification/
│
├── README.md
├── requirements.txt
├── .gitignore
├── .env.example
├── app.py
│
├── data/
│   └── README.md
│
├── notebooks/
│   └── plant_leaf_disease_classification.ipynb
│
├── src/
│   └── README.md
│
├── models/
│   ├── class_names.txt
│   └── plant_leaf_disease_model.keras
│
├── tests/
│   └── README.md
│
├── results/
│   ├── README.md
│   └── screenshots/
│
└── reports/
    ├── README.md
    └── project_report.pdf
```

## 15. References

1. [PlantVillage Dataset – Kaggle](https://www.kaggle.com/datasets/emmarex/plantdisease)
2. [TensorFlow Documentation](https://www.tensorflow.org/)
3. [Keras Documentation](https://keras.io/)
4. [Streamlit Documentation](https://docs.streamlit.io/)
5. [Scikit-learn Documentation](https://scikit-learn.org/)

## 16. Acknowledgements

The project uses the PlantVillage dataset available through Kaggle and open-source technologies including TensorFlow, Keras, Scikit-learn and Streamlit.

Developed as an academic machine learning project.
