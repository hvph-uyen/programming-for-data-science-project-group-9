# programming-for-data-science-project-group-9

## Shark Incident Analysis in Australia

### 1. Project Overview & Team Info

#### Project: Shark Incidents Analysis in Australia (2025)

Phân tích các sự kiện của tấn công cá mập tại Úc nhằm tìm ra xu hướng theo thời gian, địa điểm, loài cá mập, hoạt động của nạn nhân và mức độ nghiêm trọng nhằm làm rõ các yếu tố rủi ro liên quan đến sự kiện tấn công của cá mập, từ đó góp phần nâng cao nhận thức cộng đồng và hỗ trợ an toàn ven biển.

#### Team members:

1. Trần Minh Trọng - 23120100
2. Hàn Vũ Phương Uyên - 23120106
3. Phạm Hương Trà - 23120177

### 2. Dataset Source & Description

- Bộ dữ liệu: [Australian Shark-Incident Database (ASID)](https://taronga.org.au/conservation-and-science/australian-shark-incident-database). Ghi nhận các sự cố giữa cá mập và con người tại Úc, bao gồm các vụ tấn công, va chạm hoặc cố gắng cắn.

- Tổ chức quản lý và thu thập: Taronga Conservation Society Australia, phối hợp với Flinders University và NSW Department of Primary Industries. Thời gian thu thập kéo dài từ 1791 đến hiện tại, được cập nhật theo từng năm.

- Bộ dữ liệu được chia sẻ công khai theo giấy phép mở thông qua GitHub của ASID ([GitHub – AustralianSharkIncidentDatabase](https://github.com/cjabradshaw/AustralianSharkIncidentDatabase)).

- Người sử dụng được phép dùng cho mục đích học thuật, nghiên cứu và các phân tích khoa học. Khi sử dụng hoặc trích dẫn cần ghi rõ nguồn gốc: "Australian Shark-Incident Database, Taronga Conservation Society Australia". Không có giới hạn thương mại cụ thể nhưng phải đảm bảo giữ nguyên tính toàn vẹn nội dung và ghi nhận nguồn theo quy định.

### 3. Research Questions

1. Xu hướng phân bố các vụ tấn công cá mập tại Úc thay đổi như thế nào theo thời gian và không gian?

    Mục đích: xác định liệu sự gia tăng có liên quan đến việc mở rộng hoạt động ven biển của con người hay không.

2. Có mối liên hệ nào giữa loài cá mập và số lượng cá mập tham gia đến mức độ nghiêm trọng của chấn thương không?

    Mục đích: xác định mức độ nguy hiểm thực tế của từng loài và hiểu rõ hơn về động cơ của các cuộc tấn công hiếm gặp liên quan đến nhiều cá mập.

3. Độ sâu tại vị trí xảy ra sự cố ảnh hưởng như thế nào kiểu hành vi tấn công của cá mập?

    Mục đích: hiểu rõ chiến thuật săn mồi của cá mập trong các môi trường độ sâu khác nhau.

4. Giới tính của nạn nhân và tính chất của vụ tấn công có mối liên hệ như thế nào?

    Mục đích: xác định xem yếu tố rủi ro đến từ hành vi chủ động khiêu khích của con người hay do ngẫu nhiên, và liệu có sự khác biệt về giới trong hành vi này

5. Liệu độ tuổi và giới tính của nạn nhân có ảnh hưởng đến khả năng bị tấn công bởi các loài cá mập cụ thể không?

    Mục đích: tìm hiểu xem liệu các loài cá mập khác nhau có xu hướng "chọn" mục tiêu dựa trên kích thước (liên quan đến tuổi) hoặc hành vi đặc thù của nhóm nhân khẩu học hay không

6. Có thể phân nhóm các vụ tấn công thành các mẫu hình (patterns) riêng biệt dựa trên sự kết hợp của nhiều yếu tố (như vị trí, độ sâu, hoạt động, loài cá mập, ...) không?

    Mục đích: xác định các pattern thông qua kết hợp nhiều đặc trưng.

### 4. Key findings summary
**a. Nhân khẩu học:** Khoảng 90% nạn nhân là nam giới, nam giới có tỷ lệ các vụ tấn công do kích động cao hơn đáng kể so với nữ giới.

**b. Thời gian và không gian:** Số sự cố gia tăng mạnh từ sau năm 1900, đạt đỉnh vào mùa hè (tháng 11–2) và khung giờ 12h–18h. New South Wales (NSW) là bang ghi nhận nhiều sự cố nhất. Phần lớn vụ việc xảy ra ở vùng nước nông và gần bờ.

**c. Mức độ nghiêm trọng:** Cá mập trắng, cá mập hổ và cá mập bò gây ra hầu hết các ca thương tích nghiêm trọng. Các sự cố có hơn một cá mập làm tỷ lệ tử vong tăng lên trên 50%. Loài và kích thước cá mập là các yếu tố dự báo mạnh nhất cho kết cục tử vong. Dữ liệu cho thấy cá mập không chủ động săn người mà thường cắn do nhầm lẫn mục tiêu, phản ứng phòng vệ hoặc tiếp xúc ngẫu nhiên trong các hoạt động của con người.

**d. Phân cụm sự cố:** Phân cụm K-Means xác định 3 nhóm rủi ro:
- Rủi ro cao: Cá mập trắng lớn, tỷ lệ tử vong ~40%
- Rủi ro trung bình: Cá mập trắng/hổ kích thước trung bình, tử vong ~21.7%
- Rủi ro thấp: Cá mập thảm (wobbegong) nhỏ, tử vong ~1.6%, thường là hành vi phòng vệ

### 5. Source folder structure
```
project/
├── data/
│   └── processed/
|   |   └── SharkIncident_processed.csv
│   └── raw/
|       └── SharkIncident.csv
|
├── source.ipynb
├── requirements.txt
└── README.md
```

### 6. How to run
- Tải và giải nén file `Group_09.zip`
- Vào thư mục programming-for-data-science-project-group-9
- pip install -r requirements.txt
- Run notebook: `jupyter notebook source.ipynb`

### 7. Dependencies List
Các thư viện được sử dụng:
* pandas: Để xử lý và phân tích dữ liệu.
* numpy: Để tính toán và xử lý mảng.
* matplotlib: Để vẽ biểu đồ.
* seaborn: Thư viện trực quan hóa dữ liệu.
* scikit-learn: Thực hiện các thuật toán học máy (machine learning).
* jupyter: Để chạy các Jupyter Notebook.
