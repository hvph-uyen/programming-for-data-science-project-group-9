## Shark Incident Analysis in Australia

### 1. Project Overview & Team Info
---
#### Project: Shark Incidents Analysis in Australia (2025)

Phân tích các sự kiện tấn công cá mập tại Úc nhằm tìm ra xu hướng theo thời gian, địa điểm, loài cá mập, hoạt động của nạn nhân và mức độ nghiêm trọng nhằm đưa ra cảnh báo kịp thời.

#### Team members:

1. Trần Minh Trọng - 23120100
2. Hàn Vũ Phương Uyên - 23120106
3. Phạm Hương Trà - 23120177

### 2. Dataset Source & Description
---
- Bộ dữ liệu: [Australian Shark-Incident Database (ASID)](https://taronga.org.au/conservation-and-science/australian-shark-incident-database). Ghi nhận các sự cố giữa cá mập và con người tại Úc, bao gồm các vụ tấn công, va chạm hoặc cố gắng cắn.

- Tổ chức quản lý và thu thập: Taronga Conservation Society Australia, phối hợp với Flinders University và NSW Department of Primary Industries. Thời gian thu thập kéo dài từ 1791 đến hiện tại, được cập nhật theo từng năm.

- Bộ dữ liệu được chia sẻ công khai theo giấy phép mở thông qua GitHub của ASID ([GitHub – AustralianSharkIncidentDatabase](https://github.com/cjabradshaw/AustralianSharkIncidentDatabase)).

- Người sử dụng được phép dùng cho mục đích học thuật, nghiên cứu và các phân tích khoa học. Khi sử dụng hoặc trích dẫn cần ghi rõ nguồn gốc: "Australian Shark-Incident Database, Taronga Conservation Society Australia". Không có giới hạn thương mại cụ thể nhưng phải đảm bảo giữ nguyên tính toàn vẹn nội dung và ghi nhận nguồn theo quy định.

### 3. Research Questions
---
1. Xu hướng phân bố các vụ tấn công cá mập tại Úc thay đổi như thế nào theo thời gian và không gian?

    Mục đích: xác định xem sự gia tăng các vụ tấn công là do sự mở rộng hoạt động của con người sang các vùng biển mới hay do thay đổi hành vi của cá mập theo mùa

2. Có mối liên hệ nào giữa loài cá mập và mức độ nghiêm trọng của chấn thương không?

    Mục đích: xác định mức độ nguy hiểm thực tế của từng loài

3. Độ sâu tại vị trí xảy ra sự cố ảnh hưởng như thế nào kiểu hành vi tấn công của cá mập?

    Mục đích: hiểu rõ chiến thuật săn mồi của cá mập trong các môi trường độ sâu khác nhau

4. Số lượng cá mập tham gia có ảnh hưởng đến đối tượng bị cắn hoặc mức độ nghiêm trọng không?

    Mục đích: hiểu rõ hơn về động cơ của các cuộc tấn công hiếm gặp liên quan đến nhiều cá mập

5. Giới tính của nạn nhân và tính chất của vụ tấn công có mối liên hệ như thế nào?

    Mục đích: xác định xem yếu tố rủi ro đến từ hành vi chủ động khiêu khích của con người hay do ngẫu nhiên, và liệu có sự khác biệt về giới trong hành vi này

6. Liệu độ tuổi và giới tính của nạn nhân có ảnh hưởng đến khả năng bị tấn công bởi các loài cá mập cụ thể không?

    Mục đích: tìm hiểu xem liệu các loài cá mập khác nhau có xu hướng "chọn" mục tiêu dựa trên kích thước (liên quan đến tuổi) hoặc hành vi đặc thù của nhóm nhân khẩu học hay không

7. Có thể phân nhóm các vụ tấn công thành các mẫu hình (patterns) riêng biệt dựa trên sự kết hợp của nhiều yếu tố (như vị trí, độ sâu, hoạt động, loài cá mập, ...) không?

    Mục đích: tìm thấy pattern xuất hiện vụ tấn công 
### 4. Key Findings Summary
---
### 5. File Structure Explanation ( if chia )
---
### 6. How to run instructions
---
Install dependencies: `pip install -r requirements.txt`

Run notebook: `notebooks/shark_analysis.ipynb`
### 7. Dependencies List
---