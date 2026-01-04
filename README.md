# satellite
# Multimodal House Price Valuation (Satellite + Tabular Data)

This project predicts house prices using a **multimodal approach**, combining:
- **Tabular features** (size, rooms, location, etc.)
- **Satellite images** (neighborhood context from Sentinel-2)

The goal is not only prediction accuracy, but also **interpretability** using Grad-CAM to understand *what the model looks at* in satellite images.

---

## Project Structure

CDC/
│
├── data/
│ ├── images/ # Downloaded satellite images (.png)
│ ├── satellite/
│ │ └── image_metadata.csv # id → image_path mapping
│ ├── processed/
│ │ ├── train_final.csv
│ │ ├── val_final.csv
│ │ └── test2(test(1)).csv
│ └── embeddings/
│ ├── resnet18_train_embeddings.csv
│ └── resnet18_val_embeddings.csv
│
├── preprocessing.ipynb # Data cleaning, feature engineering, log transform
├── data_fetcher.py # Downloads satellite images from Sentinel Hub
├── model_training1.ipynb # Tabular, image, and fusion models + predictions
├── explainability.ipynb # Grad-CAM explainability
├── final_predictions.csv # Final test predictions
├── requirements.txt # Python dependencies
└── README.md# CDC_satellite
# CDC_satellite
