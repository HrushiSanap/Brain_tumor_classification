# 🧠 Pre-trained Model Weights

Due to GitHub's file size limits (files >100MB), the trained model weights are **not stored directly in this repository**. 

Instead, they are hosted in the **Releases** section of this project.

## 📥 How to Download

1.  Navigate to the **[Releases](../../releases)** page of this repository (look for the "Releases" tag on the right sidebar).
2.  Download the `.keras` files attached to the latest release (e.g., `v1.0`).
3.  **Move the downloaded files into this folder (`models/`).**

## ✅ Required Files

Ensure you have the following files in this directory for the inference scripts to work correctly. Do not rename them.

* `best_DenseNet121.keras`
* `best_EfficientNetV2S.keras`
* `best_EfficientNetV2M.keras`
* `best_InceptionResNetV2.keras`

## 💻 Loading the Models

Once the files are in place, you can load them in Python as follows:

```python
import tensorflow as tf
from tensorflow import keras

# Example: Loading EfficientNetV2M
model_path = 'models/best_EfficientNetV2M.keras'

# Note: If you used custom layers (like Augmentation), you might need to handle custom_objects
# For this project, standard loading usually works if the inference script recreates the environment
model = keras.models.load_model(model_path)

print("Model loaded successfully!")