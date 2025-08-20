# Road-Surface-Damage-Detection-using-YOLOv8n
[![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)]()
[![PyTorch](https://img.shields.io/badge/PyTorch-2.0+-red.svg)]()
[![YOLOv8](https://img.shields.io/badge/YOLOv8-green.svg)]()
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 1. Giới thiệu dự án (Introduction)

Dự án này sử dụng mô hình YOLOv8n để phát hiện và phân loại các hư hại trên bề mặt đường. Với mục tiêu xây dựng một giải pháp hiệu quả và nhẹ, dự án tập trung vào việc triển khai mô hình trên các thiết bị biên (edge devices) nhằm phục vụ các ứng dụng thực tế như hệ thống giám sát đường tự động.

- **Mục tiêu chính**: Tự động phát hiện các vết nứt, ổ gà, và các hư hại khác trên đường một cách chính xác.
- **Mô hình**: YOLOv8n (phiên bản Nano) - Lựa chọn tối ưu cho hiệu suất cao với chi phí tính toán thấp.
- **Bộ dữ liệu**: SVRDD (Surface Vechicular Road Damage Dataset) - Bộ dữ liệu chuyên biệt để huấn luyện mô hình phát hiện hư hại đường.

## 2. Cài đặt (Installation)

Để cài đặt các thư viện cần thiết, bạn có thể sử dụng `pip` từ file `requirements.txt`.

pip install -r requirements.txt

3. Cấu trúc thư mục (File Structure)

Link dataset: https://zenodo.org/records/10100129

Dự án được tổ chức theo cấu trúc sau (Cấu trúc dữ liệu của dataset có thể hơi khác so với cấu trúc dữ liệu được yêu cầu bên dưới):

```bash
Road-Surface-Damage-Detection/
├── dataset/
│   ├── images/
│   │   ├── train/
│   │   ├── val/
│   │   └── test/
│   └── labels/
│       ├── train/
│       ├── val/
│       └── test/
├── requirements.txt
├── DoAnEmbeddedAI.ipynb (notebook huấn luyện)
├── ChayMoHinh.ipynb (notebook dự đoán)
└── README.md
```

## 4. Cách sử dụng (Usage)
Huấn luyện mô hình
Sử dụng notebook DoAnEmbeddedAI.ipynb để huấn luyện mô hình trên bộ dữ liệu của bạn.

Dự đoán và phát hiện
Sử dụng notebook ChayMoHinh.ipynb để chạy mô hình đã huấn luyện trên tập test được cung cấp sẵn.

## 5. Kết quả (Results)
Sau quá trình huấn luyện, mô hình đạt được các chỉ số hiệu suất sau:

mAP50: 0.311

mAP50-95: 0.19

Đây là những kết quả chứng minh khả năng định vị hư hại đường một cách hiệu quả. Kết quả có thể hơi khác tùy vào số epoch hoặc các chỉ số khác như learning rate, batch size,...bị thay đổi.

Hình ảnh minh họa

## 6. Cải tiến trong tương lai (Future Works)
Tối ưu hóa sâu hơn: Thử nghiệm các kỹ thuật lượng tử hóa (quantization) như INT8 để giảm kích thước mô hình và tăng tốc độ suy luận trên thiết bị biên.

Mở rộng bộ dữ liệu: Huấn luyện trên các bộ dữ liệu đa dạng hơn để cải thiện khả năng tổng quát của mô hình.

Triển khai thực tế: Xây dựng một ứng dụng nhúng trên các thiết bị như Raspberry Pi hoặc Jetson Nano để thực hiện dự đoán thời gian thực.

## 7. Tác giả (Author)
Nguyễn Hoàng Nam

Danh Nat

Email: ng.h.nam0802@gmail.com

LinkedIn: https://www.linkedin.com/in/NamIsStudyingCE
