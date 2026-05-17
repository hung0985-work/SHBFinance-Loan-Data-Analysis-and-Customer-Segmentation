# SHBFinance Loan Data Analysis and Customer Segmentation

## 1. Tổng quan dự án

Dự án này phân tích dữ liệu khách hàng và khoản vay của SHBFinance nhằm hiểu rõ chân dung khách hàng, đặc điểm danh mục khoản vay, xu hướng thay đổi giữa năm 2022 và 2023, đồng thời phân khúc khách hàng để đề xuất chiến lược tăng trưởng khoản vay và bán chéo sản phẩm phù hợp.

Phân tích tập trung vào các nhóm thông tin chính như nhân khẩu học, hồ sơ tài chính, đặc điểm khoản vay, mục đích vay, kỳ hạn vay, lãi suất, bảo hiểm khoản vay và hành vi vay của từng nhóm khách hàng.

## 2. Bối cảnh kinh doanh

SHBFinance cần hiểu sâu hơn về khách hàng và hoạt động cho vay để cải thiện hiệu quả kinh doanh. Dữ liệu cho thấy khách hàng của công ty khá đa dạng, phần lớn thuộc nhóm thu nhập thấp đến trung bình và có nhu cầu vay phục vụ các mục đích tiêu dùng như mua sắm, phương tiện đi lại và nhà ở.

Do đó, việc phân tích dữ liệu khoản vay giúp SHBFinance nhận diện nhóm khách hàng trọng tâm, hiểu nhu cầu tài chính của từng nhóm và xây dựng các chiến lược phù hợp nhằm tăng số lượng khoản vay, tăng doanh số và cải thiện mức độ gắn kết khách hàng.

## 3. Mục tiêu phân tích

Dự án tập trung trả lời các câu hỏi chính:

- Khách hàng của SHBFinance có đặc điểm nhân khẩu học và tài chính như thế nào?
- Các khoản vay phổ biến nhất thuộc nhóm sản phẩm, mục đích vay và kỳ hạn nào?
- Danh mục khoản vay thay đổi ra sao giữa năm 2022 và 2023?
- Những nhóm khách hàng nào có hành vi vay tương đồng?
- Có thể phân khúc khách hàng thành các nhóm có ý nghĩa kinh doanh không?
- SHBFinance nên đề xuất sản phẩm và chiến lược bán hàng như thế nào cho từng nhóm khách hàng?

## 4. Phương pháp thực hiện

Dự án sử dụng các phương pháp chính sau:

### 4.1. Data Preparation

Dữ liệu được xử lý bằng cách kết hợp hai bảng chính gồm dữ liệu nhân khẩu học khách hàng và dữ liệu khoản vay. Các bước xử lý bao gồm làm sạch dữ liệu, xử lý missing values, chuyển đổi định dạng ngày, mã hóa biến phân loại và loại bỏ các cột không cần thiết.

### 4.2. Customer Analysis

Phân tích khách hàng được thực hiện dựa trên các biến như độ tuổi, tình trạng hôn nhân, trình độ học vấn, số người phụ thuộc, tỉnh/thành phố, loại hợp đồng lao động, số năm làm việc, ngành nghề, thu nhập, nguồn thu nhập, nơi ở và điểm tín dụng.

### 4.3. Loan Analysis

Phân tích khoản vay tập trung vào nhóm sản phẩm vay, mục đích vay, số tiền vay, kỳ hạn vay, lãi suất, bảo hiểm khoản vay và sự thay đổi của các chỉ số này giữa năm 2022 và 2023.

### 4.4. Customer Segmentation

Dự án sử dụng K-means clustering để phân khúc khách hàng dựa trên các biến số quan trọng như tuổi, thu nhập, số năm làm việc, số người phụ thuộc, số tiền vay và kỳ hạn vay. Số cụm tối ưu được xác định bằng Elbow Method.

### 4.5. Business Recommendation

Sau khi phân cụm, mỗi nhóm khách hàng được mô tả theo đặc điểm riêng và được đề xuất chiến lược tăng khoản vay, bán chéo và giữ chân phù hợp.

## 5. Cấu trúc file dự án

```text
SHBFinance-Loan-Analysis/
│
├── Notebook.ipynb
│   └── Notebook chính dùng để xử lý dữ liệu, phân tích khách hàng, phân tích khoản vay, phân cụm K-means và tạo các kết quả trực quan hóa.
│
└── Report.pdf
    └── Báo cáo trình bày kết quả phân tích cuối cùng, bao gồm bối cảnh kinh doanh, xử lý dữ liệu, phân tích khách hàng, phân tích khoản vay, phân khúc khách hàng và khuyến nghị.
```

## 6. Hướng dẫn đọc dự án

Dự án gồm các file chính sau:

- `Report.pdf`: Dùng để đọc nhanh toàn bộ logic phân tích, kết quả chính và khuyến nghị kinh doanh cho SHBFinance.
- `Notebook.ipynb`: Dùng để xem chi tiết quá trình xử lý dữ liệu, phân tích dữ liệu, phân cụm khách hàng bằng K-means và tạo biểu đồ phục vụ báo cáo.

## 7. Kết quả chính

Một số kết quả nổi bật của dự án:

- Khách hàng của SHBFinance chủ yếu nằm trong nhóm tuổi lao động, tập trung nhiều ở khoảng 25–40 tuổi.
- Phần lớn khách hàng có số người phụ thuộc thấp, thường từ 0 đến 1 người.
- Khách hàng chủ yếu thuộc một số nhóm nghề nghiệp và ngành nghề nhất định, cho thấy danh mục khách hàng có sự tập trung theo hồ sơ lao động.
- Các khoản vay phổ biến nhất phục vụ mục đích mua sắm, phương tiện đi lại và nhà ở.
- Lãi suất khoản vay chủ yếu nằm trong khoảng 1,9% đến 2,3% mỗi tháng, phản ánh chính sách lãi suất tương đối tiêu chuẩn.
- Số lượng khoản vay năm 2023 cao hơn năm 2022 khoảng 20%, cho thấy xu hướng tăng trưởng tích cực trong hoạt động cho vay.
- Kỳ hạn vay phổ biến nhất là 24 tháng, tiếp theo là 36 tháng và 12 tháng.
- Số tiền vay trung bình khoảng 2,54 triệu VND, cho thấy SHBFinance tập trung vào các khoản vay tiêu dùng quy mô vừa và nhỏ.
- K-means clustering xác định 5 nhóm khách hàng với đặc điểm khác nhau về tuổi, thu nhập, kinh nghiệm làm việc, số người phụ thuộc, số tiền vay và kỳ hạn vay.
- Các phân khúc khách hàng được sử dụng để đề xuất chiến lược riêng như gói vay cao cấp, khoản vay nhỏ phê duyệt nhanh, sản phẩm tài chính gia đình, bảo hiểm đi kèm và chương trình khách hàng thân thiết.

## 8. Công cụ sử dụng

Dự án sử dụng các công cụ và thư viện chính sau:

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- K-means Clustering
- Elbow Method
- Jupyter Notebook
- PowerPoint / Canva cho phần trình bày báo cáo

## 9. Hạn chế của dự án

Dự án vẫn có một số hạn chế:

- Một số cột trong dữ liệu nhân khẩu học và dữ liệu khoản vay có tỷ lệ thiếu khá cao.
- Nhiều biến phân loại được mã hóa nhưng không có mô tả nhãn rõ ràng, gây khó khăn trong việc diễn giải ý nghĩa kinh doanh.
- Dữ liệu chủ yếu phản ánh thông tin tại thời điểm khởi tạo khoản vay, chưa có đầy đủ lịch sử quan hệ khách hàng với SHBFinance.
- Dự án chưa kết hợp thêm các biến quan trọng như lịch sử trả nợ, thời gian gắn bó, tỷ lệ nợ trên thu nhập hoặc mức độ hài lòng của khách hàng.
- Phân cụm K-means giúp nhận diện nhóm khách hàng tương đồng nhưng không khẳng định quan hệ nhân quả.

## 10. Định hướng phát triển tiếp theo

Trong các phiên bản tiếp theo, dự án có thể được mở rộng theo các hướng:

- Bổ sung dữ liệu lịch sử trả nợ để đánh giá chất lượng tín dụng của từng phân khúc.
- Xây dựng mô hình dự báo khả năng khách hàng vay thêm hoặc mua sản phẩm tài chính bổ sung.
- Phát triển hệ thống gợi ý sản phẩm vay và bảo hiểm theo từng nhóm khách hàng.
- Xây dựng dashboard theo dõi danh mục khoản vay, nhóm khách hàng và hiệu quả bán chéo.
- Kết hợp thêm dữ liệu hành vi thanh toán, điểm tín dụng và mức độ tương tác để phân khúc khách hàng chính xác hơn.
