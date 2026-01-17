epl_prediction_project/
├── data/                    # Nơi chứa dữ liệu (Không bao giờ sửa trực tiếp file raw)
│   ├── raw/                 # Dữ liệu gốc tải về (csv từ football-data.co.uk)
│   ├── processed/           # Dữ liệu sau khi đã làm sạch và tạo features
│   └── external/            # Dữ liệu phụ (ví dụ: bảng xếp hạng FIFA, thời tiết...)
│
├── notebooks/               # Nơi chạy thử nghiệm (Jupyter Notebooks)
│   ├── 01_data_exploration.ipynb   # Phân tích, vẽ biểu đồ xem dữ liệu
│   ├── 02_feature_engineering.ipynb # Thử tạo các cột mới (phong độ, đối đầu...)
│   └── 03_model_training.ipynb     # Thử train các model khác nhau
│
├── src/                     # Source code chính (Đây là phần "Package" anh hỏi)
│   ├── __init__.py          # Đánh dấu thư mục này là một package Python
│   ├── data/                # Code xử lý dữ liệu
│   │   ├── __init__.py
│   │   ├── load_data.py     # Hàm tải dữ liệu
│   │   └── clean_data.py    # Hàm xử lý null, chuẩn hóa tên đội bóng
│   │
│   ├── features/            # Quan trọng nhất: Code tạo "đặc trưng" (Feature Engineering)
│   │   ├── __init__.py
│   │   └── build_features.py # Hàm tính phong độ 5 trận, tỷ lệ thắng sân nhà...
│   │
│   ├── models/              # Code liên quan đến thuật toán
│   │   ├── __init__.py
│   │   ├── train_model.py   # Script để train model
│   │   └── predict_model.py # Script để dự đoán kết quả mới
│   │
│   └── visualization/       # Code vẽ biểu đồ
│       ├── __init__.py
│       └── visualize.py
│
├── models/                  # Nơi lưu file model đã train xong (.pkl, .joblib)
├── requirements.txt         # Các thư viện cần thiết (pandas, scikit-learn...)
└── main.py                  # File chạy chính của chương trình