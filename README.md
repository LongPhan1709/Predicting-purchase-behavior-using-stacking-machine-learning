# 📊 Dự đoán Hành Vi Mua Sắm Trực Tuyến bằng Stacking Ensemble Learning
## 📝 Giới thiệu
Hành vi mua sắm trực tuyến ngày càng phức tạp, đòi hỏi các mô hình học máy có độ chính xác cao để dự đoán khả năng mua hàng của khách hàng. Dự án này sử dụng Stacking Ensemble Learning để tối ưu hóa khả năng dự báo dựa trên bộ dữ liệu Online Shoppers Purchasing Intention Dataset.

## 🎯 Mục tiêu
- Nghiên cứu các yếu tố ảnh hưởng đến quyết định mua sắm trực tuyến.
- Xây dựng mô hình học máy để dự đoán khách hàng có khả năng mua hàng.
- So sánh hiệu suất giữa mô hình Stacking và các mô hình cơ sở khác.
## 🛠️ Công nghệ & Phương pháp
- Ngôn ngữ: Python 🐍
- Thư viện: Scikit-learn, Pandas, NumPy, Matplotlib, Seaborn
- Phương pháp chính:
  - EDA (Khám phá dữ liệu): Trực quan hóa và xử lý dữ liệu.
  - SMOTE: Giải quyết mất cân bằng dữ liệu.
  - Stacking Ensemble Learning: Kết hợp nhiều mô hình để nâng cao độ chính xác.
  - Mô hình cơ sở: KNN, Decision Tree, SVM, Naive Bayes.
  - Mô hình cấp 1: Hồi quy logistic.
## 📂 Dữ liệu
Bộ dữ liệu được lấy từ UCI Machine Learning Repository với 12,330 quan sát và 18 biến, bao gồm:
- Biến định lượng: Thời gian trên các trang web, tỷ lệ thoát, giá trị trang,...
- Biến phân loại: Tháng, hệ điều hành, trình duyệt, khu vực, loại lưu lượng,...
## 🏗️ Quy trình Xây dựng Mô hình
1. Khám phá dữ liệu (EDA): Trực quan hóa và kiểm tra dữ liệu.
2. Xử lý dữ liệu: Chuẩn hóa, mã hóa biến phân loại, xử lý dữ liệu mất cân bằng bằng SMOTE.
3. Huấn luyện mô hình:
    - Cấp 0: KNN, Decision Tree, SVM, Naive Bayes.  
    - Cấp 1: Hồi quy logistic tổng hợp đầu ra từ các mô hình cấp 0.
4. Đánh giá mô hình: So sánh hiệu suất giữa Stacking và các mô hình cơ sở.
## 📊 Kết quả & Đánh giá  

| Mô hình        | Độ chính xác | Precision | Recall | F1-score  |
|---------------|-------------|-----------|--------|----------|
| KNN          | 90.21%      | Thấp      | Cao    | Trung bình |
| SVM          | 79.85%      | Trung bình | Thấp   | Thấp      |
| Decision Tree| 92.18%      | Cao       | Cao    | Tốt       |
| **Stacking** | **92.37%**  | **Cân bằng** | **Tốt nhất** | **Tốt nhất** |

📌 **Mô hình Stacking đạt độ chính xác cao nhất (92.37%)**, cân bằng tốt giữa precision và recall, giúp tối ưu dự báo hành vi khách hàng.  

## 🔮 Hướng phát triển
- Cải tiến việc lựa chọn mô hình con và tối ưu hóa siêu tham số.
- Thử nghiệm với các mô hình khác như XGBoost, LightGBM.
- Ứng dụng vào các lĩnh vực khác như dự báo churn khách hàng.
