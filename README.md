# 🌱 Crop Health Monitoring Model

A machine learning model to classify crop health using Sentinel-2 satellite imagery.

## 📦 Model Files
- `crop_health_model_v1.joblib` - Pretrained model (GradientBoostingClassifier)
- `metadata.json` - Model specifications and performance

## 🛠 Features
- **Input**: 
  - NDVI (Normalized Difference Vegetation Index)
  - NDWI (Normalized Difference Water Index)
  - MSI (Moisture Stress Index)
- **Output Classes**:
  - `0`: Stressed vegetation
  - `1`: Healthy vegetation
  - `2`: Non-crop area

## 🚀 Usage
```python
import joblib

# Load model
model = joblib.load('crop_health_model_v1.joblib')

# Example prediction (NDVI, NDWI, MSI)
sample = [[0.65, 0.12, 0.3]]  # Replace with your features
prediction = model.predict(sample)
print(["Stressed", "Healthy", "Non-crop"][prediction[0]])
