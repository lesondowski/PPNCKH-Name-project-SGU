# 🎯 Dự đoán Sự Hài Lòng của Khách Hàng bằng Học Máy/Học Sâu  
**(Predicting Customer Satisfaction with Machine Learning and Deep Learning)**

## 📘 Giới thiệu
Trong bối cảnh thương mại điện tử phát triển mạnh mẽ, việc **giữ chân khách hàng** và **nâng cao trải nghiệm người dùng** trở thành yếu tố sống còn đối với doanh nghiệp. Đề tài nghiên cứu này đề xuất một hệ thống **dự đoán mức độ hài lòng của khách hàng** dựa trên dữ liệu hành vi và phản hồi, ứng dụng các thuật toán học máy/học sâu hiện đại như **Random Forest**, **LightGBM**, và **CNN**.

## 🎯 Mục tiêu nghiên cứu
- Phân tích các yếu tố ảnh hưởng đến sự hài lòng của khách hàng.
- Xây dựng, huấn luyện và đánh giá các mô hình dự đoán sử dụng ML/DL.
- So sánh hiệu suất giữa các mô hình và đề xuất giải pháp tối ưu.
- Ứng dụng mô hình vào thực tiễn để hỗ trợ doanh nghiệp nâng cao dịch vụ.

## 📊 Dữ liệu và tiền xử lý
- **Nguồn**: `train_dataset.csv` (mô phỏng dữ liệu thương mại điện tử).
- **Đặc trưng**: Thông tin người dùng, lịch sử giao dịch, chương trình khách hàng thân thiết, đánh giá sản phẩm, phương thức thanh toán,...
- **Biến mục tiêu**: `customer_experience` với 3 mức: `good`, `neutral`, `bad`.
- **Tiền xử lý**:
  - Xử lý thiếu dữ liệu, mã hóa biến phân loại.
  - Chuẩn hóa dữ liệu (MinMax/Z-score).
  - Loại bỏ ngoại lai (IQR), xử lý trùng lặp.
  - Feature engineering: nhóm tuổi, tần suất tương tác...

## 🧠 Mô hình đã thử nghiệm
| Mô hình         | Mô tả ngắn gọn                                             |
|------------------|-------------------------------------------------------------|
| Random Forest     | Mô hình ensemble truyền thống, đơn giản, dễ triển khai.     |
| LightGBM          | Boosting dựa trên cây quyết định, hiệu quả với dữ liệu lớn. |
| CNN (1D)          | Mạng nơ-ron tích chập, dùng cho đặc trưng chuỗi/tabular.   |

## 🧪 Kết quả đánh giá
| Chỉ số        | LightGBM | Random Forest |
|---------------|----------|----------------|
| Accuracy      | 0.6731   | 0.6043         |
| F1-Score      | 0.6741   | 0.6054         |
| F1 lớp 0      | 0.63     | 0.55           |
| F1 lớp 1      | 0.73     | 0.57           |
| F1 lớp 2      | 0.68     | 0.67           |
| Tổng quát     | Tốt      | Trung bình     |

✅ **LightGBM đạt kết quả tốt nhất**, đặc biệt trong việc dự đoán nhóm khách hàng trung tính – phù hợp để triển khai thực tế.

## 🧩 Ý nghĩa thực tiễn
- Hỗ trợ doanh nghiệp **dự đoán sớm mức độ hài lòng**, chủ động xử lý phản hồi tiêu cực.
- Tối ưu hóa chiến dịch tiếp thị, chăm sóc khách hàng và cá nhân hóa trải nghiệm.
- Mô hình có thể áp dụng cho **nhiều lĩnh vực khác**: y tế, giáo dục, du lịch...
- Đóng góp cho **chuyển đổi số và ứng dụng AI** trong doanh nghiệp Việt Nam.

## 🚧 Khó khăn & Hướng khắc phục
- Accuracy còn giới hạn (~67%), mô hình có thể bị ảnh hưởng bởi dữ liệu nhiễu.
- Hướng xử lý:
  - Grid Search, Bayesian Optimization để tối ưu siêu tham số.
  - Stacking/Bagging/Boosting đa tầng.
  - Phát hiện & loại bỏ outlier (IQR, Isolation Forest).
  - Feature engineering nâng cao.
  - Thử nghiệm mô hình sâu hơn (MLP, Deep Ensemble).

## 👨‍💻 Thành viên nhóm

- **Lê Hồng Sơn** - Leader - [GitHub](https://github.com/lesondowski)
- **Văn Hoàng Như Ý** - [GitHub](https://github.com/VanHoangNhuY)
- **Nguyễn Hoàng Thanh Phương** - [GitHub](https://github.com/NHTPhuong35)
- **Đỗ Hữu Lộc** - [GitHub](https://github.com/dohuuloc2k5)

## 🛠️ Công nghệ và thư viện sử dụng
- Python 3.x
- pandas, numpy – xử lý dữ liệu
- scikit-learn – mô hình ML truyền thống
- lightgbm – mô hình boosting
- seaborn, matplotlib – trực quan hóa dữ liệu
- Jupyter Notebook – thử nghiệm mô hình

## 📌 Cách chạy dự án

## Ghi chú note

### Tạo nhánh mới

- Mỗi thành viên tạo nhánh riêng để thực hiện công việc:
  > `git checkout -b feature-username`

### Thực hiện thay đổi & cam kết

- Sau khi hoàn thành tính năng, commit code:

  > `git add .`

  > `git commit -m "Thêm tính năng A"`

### Đẩy nhánh lên GitHub

> `git push origin feature-username`
