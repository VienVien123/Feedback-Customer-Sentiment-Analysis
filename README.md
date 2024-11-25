
# Phân Tích Cảm Xúc Khách Hàng Thông Qua Feedback

## Mục Lục
1. [Giới Thiệu](#giới-thiệu)
2. [Quy Trình Phân Tích Dữ Liệu](#quy-trình-phân-tích-dữ-liệu)
3. [Phương Pháp Gắn Nhãn Dữ Liệu](#phương-pháp-gắn-nhãn-dữ-liệu)
   - [1. Đánh Giá Nhãn Dựa Trên Số Sao](#1-đánh-giá-nhãn-dựa-trên-số-sao)
   - [2. Sử Dụng Mô Hình Được Huấn Luyện Sẵn (5CD/AI)](#2-sử-dụng-mô-hình-được-huấn-luyện-sẵn-5cdai)
4. [Công Nghệ Sử Dụng](#công-nghệ-sử-dụng)
5. [Hướng Dẫn Cài Đặt](#hướng-dẫn-cài-đặt)
   - [1. Clone Repository](#1-clone-repository)
   - [2. Tạo Virtual Environment (venv)](#2-tạo-virtual-environment-venv)
   - [3. Cài Đặt Các Thư Viện Yêu Cầu](#3-cài-đặt-các-thư-viện-yêu-cầu)
   - [4. Chạy Project](#4-chạy-project)
6. [Tham Khảo](#tham-khảo)

---

## Giới Thiệu
Dự án này tập trung vào phân tích cảm xúc của khách hàng thông qua các phản hồi sau khi mua sản phẩm của công ty X. Dataset ban đầu chứa các feedback từ khách hàng, nhưng chưa được làm sạch và chưa gắn nhãn cảm xúc.

Mục tiêu của dự án là thực hiện các bước tiền xử lý, gắn nhãn dữ liệu, và phân loại cảm xúc khách hàng thành ba loại: **Tích cực**, **Tiêu cực**, và **Bình thường**. 
---

## Quy Trình Phân Tích Dữ Liệu
Dữ liệu ban đầu chứa các phản hồi từ khách hàng nhưng chưa được xử lý. Các bước chính trong quy trình phân tích bao gồm:

1. **Tiền Xử Lý Dữ Liệu**: Làm sạch dữ liệu bằng cách loại bỏ các ký tự không cần thiết, xử lý từ đồng nghĩa và lỗi chính tả.
2. **Gắn Nhãn Cảm Xúc**: Dữ liệu được phân loại thành ba nhãn cảm xúc: Tích cực, Tiêu cực, và Bình thường.
3. **Phân Tích Cảm Xúc**: Đánh giá cảm xúc khách hàng bằng hai phương pháp gắn nhãn khác nhau.
4. **So sánh kết quả giữa cách đánh nhãn**
5. **visualazation**

---

## Phương Pháp Gắn Nhãn Dữ Liệu

### 1. Đánh Giá Nhãn Dựa Trên Số Sao
- Phản hồi được gắn nhãn cảm xúc dựa trên số sao mà khách hàng đánh giá.
  - **Tích cực**: Đánh giá 4 hoặc 5 sao.
  - **Bình thường**: Đánh giá 3 sao.
  - **Tiêu cực**: Đánh giá 1 hoặc 2 sao.

### 2. Sử Dụng Mô Hình Được Huấn Luyện Sẵn (5CD/AI)
- Sử dụng mô hình đã được huấn luyện trước - **[5CD/AI Vietnamese Sentiment visobert](https://huggingface.co/5CD-AI/Vietnamese-Sentiment-visobert)**.
- Mô hình sẽ gắn nhãn cảm xúc cho các phản hồi và kết hợp với thuật toán **KMeans** để cải thiện độ chính xác của nhãn.

Bạn có thể tìm hiểu thêm về mô hình 5CD/AI qua liên kết [tại đây](https://huggingface.co/5CD-AI/Vietnamese-Sentiment-visobert).

---

## Công Nghệ Sử Dụng
- **Ngôn Ngữ**: Python, Jupyter Notebook (`.ipynb`)
- **Phiên Bản Python**: 3.8 trở lên
- **Hệ Điều Hành**: Windows và macOS
---

## Hướng Dẫn Cài Đặt

### Set Up Virtual Environment and Install Libraries

```bash
python -m venv venv
source venv/bin/activate       # macOS/Linux
source .venv\Scripts\activate        # Windows

pip install -r requirements.txt
```
