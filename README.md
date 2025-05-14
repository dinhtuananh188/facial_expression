
# Hệ Thống Nhận Diện Khuôn Mặt / Face Recognition System

## 📋 Yêu cầu / Requirements

### 🖥️ Yêu cầu hệ thống / System Requirements
- Python 3.10

### 📦 Các thư viện Python cần thiết / Python Dependencies

#### ⚙️ Cho máy hỗ trợ GPU (WSL/Linux) / For GPU Support (WSL/Linux)
```bash
# Cập nhật hệ thống và cài đặt Python 3.10
sudo apt update && sudo apt upgrade
sudo apt install python3.10 python3.10-venv

# Tạo môi trường ảo tên là venv
python3 -m venv venv
source venv/bin/activate

# Cài pip và các công cụ cần thiết
sudo apt install python3-pip
sudo apt install wslu

# Cài đặt thư viện
pip install tensorflow[and-cuda]
pip install jupyter
pip install ipykernel

# Thêm kernel vào Jupyter
python3 -m ipykernel install --user --name=venv --display-name "Python (venv)"

# Cài các thư viện nhận diện khuôn mặt
pip install deepface
pip install ultralytics

# Cài Torch với hỗ trợ CUDA
pip uninstall torch torchvision torchaudio -y
pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu126

# Fix numpy version
pip uninstall numpy -y
pip install numpy==1.26.4
```

#### 🧱 Cho máy chỉ dùng CPU (Windows) / For CPU Only (Windows)
```bash
# Tạo môi trường ảo tên là .venv
python -m venv .venv
.\.venv\Scripts\Activate.ps1

# Cài Jupyter và kernel
pip install jupyter
pip install ipykernel
python -m ipykernel install --user --name=.venv --display-name "Python (.venv)"

# Cài các thư viện nhận diện khuôn mặt
pip install deepface
pip install ultralytics
pip install torch torchvision torchaudio
```

> ⚠️ **Lưu ý / Note**: Khuyến khích sử dụng GPU để có hiệu suất tốt hơn  
> **GPU is highly recommended for better performance**

---

## ⚙️ Cài đặt / Installation

1. Clone repository này:
   ```bash
   git clone https://github.com/dinhtuananh188/facial_expression.git
   cd facial_expression
   ```

2. Tạo môi trường ảo phù hợp với hệ điều hành của bạn và cài đặt các thư viện như hướng dẫn ở trên.

3. Nếu bạn sử dụng GPU, hãy đảm bảo bạn đã cài đúng phiên bản CUDA và cuDNN.

---

✅ Dự án đã sẵn sàng để phát triển và thử nghiệm hệ thống nhận diện khuôn mặt!
```
