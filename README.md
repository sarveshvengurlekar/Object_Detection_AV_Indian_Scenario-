# Major Project: Object Detection for Autonomous Vehicles (Indian Scenario)

This repository contains the training, tuning, and evaluation notebooks for a YOLOv8-based object detection model tailored for the Indian road environment. The goal of this project is to perform robust object detection for autonomous vehicles (AV), addressing unique challenges present in Indian scenarios such as stray animals, rickshaws, and potholes.

## 🎯 Detected Classes

The model is trained to detect the following **16 classes** commonly found on Indian roads:

1. `animal`
2. `bridge`
3. `building`
4. `bus`
5. `car`
6. `motorcycle`
7. `person`
8. `pothole`
9. `rickshaw`
10. `road barrier`
11. `road sign board`
12. `street light`
13. `traffic signal`
14. `trees`
15. `truck`
16. `zebra crossing`

## 📂 Directory Structure

```plaintext
Major Project Repo/
│
├── Code_Notebook/                              # Core Jupyter Notebooks for model processing
│   ├── YOLO_Hyperparameter_Tuner_Notebook.ipynb  # Identifies optimal hyperparameters
│   ├── YOLO_Hypertuned_Trainer_Notebook.ipynb    # Trains the YOLO model with tuned params
│   ├── YOLO_Epoch_Comparator_Notebook.ipynb      # Compares model performance across different epochs
│   └── YOLO_Evaluator_Notebook.ipynb             # Evaluates functionality & generates metrics
│
├── Results/                                    # Outputs, metrics, and generated comparisons
│   ├── Hyperparameter_Tuned_Results/             # Results from hyperparameter tuning
│   ├── YOLO_Evaluation_Results/                  # Final evaluation charts and metrics
│   └── YOLO_Training_Results/                    # Training charts (loss, mAP, etc.)
│
└── README.md                                   # Project documentation
```

## 🚀 Environment and Dependencies

This workflow has been designed to run efficiently on platforms like Kaggle (supporting Tesla T4 dual-GPU verification natively), but can be run locally using the following core dependencies:

- **Python 3.x**
- **Ultralytics YOLOv8**
- **PyTorch** & **Torchvision** (CUDA enabled recommended)

You can install the core dependencies via:

```bash
pip install ultralytics torch torchvision torchaudio
```

## ⚙️ Model Workflow

1. **Hyperparameter Tuning:** Start with `YOLO_Hyperparameter_Tuner_Notebook.ipynb` to hone in on the best training conditions based on the dataset metrics.
2. **Training:** Pass the optimally discovered hyperparameters to `YOLO_Hypertuned_Trainer_Notebook.ipynb` to launch the full training phase.
3. **Evaluation:** Use `YOLO_Evaluator_Notebook.ipynb` to calculate mAP50, Precision, and Recall scores across all classes.
4. **Comparison:** Check results iteratively over different epochs using `YOLO_Epoch_Comparator_Notebook.ipynb` to find the exact epoch where the model converges without overfitting.
