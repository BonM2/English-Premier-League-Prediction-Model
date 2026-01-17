# Cấu trúc dự án (Project Structure)

```text
epl_prediction_project/
├── data/                    # Nơi chứa dữ liệu
│   ├── raw/                 # Dữ liệu gốc (csv từ football-data.co.uk)
│   ├── processed/           # Dữ liệu sau khi làm sạch
│   └── external/            # Dữ liệu phụ
│
├── notebooks/               # Jupyter Notebooks để thử nghiệm
│   ├── 01_data_exploration.ipynb
│   ├── 02_feature_engineering.ipynb
│   └── 03_model_training.ipynb
│
├── src/                     # Source code chính
│   ├── __init__.py
│   ├── data/                # Scripts xử lý dữ liệu
│   │   ├── load_data.py
│   │   └── clean_data.py
│   ├── features/            # Feature Engineering
│   │   └── build_features.py
│   ├── models/              # Training & Prediction scripts
│   │   ├── train_model.py
│   │   └── predict_model.py
│   └── visualization/       # Vẽ biểu đồ
│       └── visualize.py
│
├── models/                  # File model đã train (.pkl)
├── requirements.txt         # Thư viện cần thiết
└── main.py                  # File chạy chính
```