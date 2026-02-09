<pre>
BoneFracture_Project/
│
├── 📂 research/                  # Nơi bạn train model (Không đưa vào sản phẩm cuối)
│   ├── fracture_detection.ipynb  # File Notebook dùng để train YOLOv8
│   ├── dataset/                  # Chứa ảnh X-ray để train
│   └── runs/                     # Output của YOLO (chứa file best.pt)
│
├── 📂 server/                    # PHẦN BACKEND (AI + API + Docker)
│   ├── models/                   
│   │   └── best.pt               # File model YOLO sau khi train xong copy vào đây
│   ├── app/
│   │   ├── __init__.py
│   │   ├── main.py               # File chính chạy FastAPI
│   │   └── core.py               # Chứa class load model và predict (tách biệt logic)
│   ├── Dockerfile                # Dùng để đóng gói folder server này
│   └── requirements.txt          # Các thư viện cho server (fastapi, ultralytics, uvicorn...)
│
├── 📂 client/                    # PHẦN FRONTEND (Desktop App PyQt)
│   ├── assets/                   # Chứa icon, logo, ảnh demo
│   ├── src/
│   │   ├── __init__.py
│   │   ├── main_window.py        # Code giao diện chính (Buttons, Labels)
│   │   └── api_client.py         # Code gửi request lên Server (không viết chung vào GUI)
│   ├── main.py                   # File chạy phần mềm (Entry point)
│   └── requirements.txt          # Các thư viện cho client (PyQt6, requests...)
│
├── .gitignore                    # Để loại bỏ file rác khi up lên Github
└── README.md                     # Tài liệu hướng dẫn (Rất quan trọng để xin việc)
</pre>
