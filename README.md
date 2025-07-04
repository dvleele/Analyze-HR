HR Attrition Analysis – IBM Dataset

Mục tiêu phân tích : Phân tích dữ liệu nhân sự để xác định các yếu tố ảnh hưởng đến nghỉ việc (Attrition), từ đó đưa ra các đề xuất giữ chân nhân viên hiệu quả hơn.

---
Câu hỏi đặt ra:
1. Tỷ lệ nghỉ việc toàn công ty là bao nhiêu?
2. Phòng ban hoặc vai trò nào có tỷ lệ nghỉ cao nhất?
3. Nhân viên có đặc điểm nào thường nghỉ việc hơn? (tuổi, lương, tăng ca, khoảng cách…)
4. Nhân viên giỏi có nghỉ nhiều không?
5. Nhóm nào cần được ưu tiên giữ chân?
6. Gợi ý hành động cụ thể cho cấp quản lý?

---
Quy trình thực hiện:
1. Làm sạch dữ liệu và chuyển đổi biến Attrition thành nhị phân 0 và 1 để dễ dàng hơn trong việc xử lý
2. Phân tích sơ bộ bằng Python: heatmap, boxplot, crosstab
3. Xác định biến ảnh hưởng chính
4. Thiết kế dashboard trên Power BI
5. Gửi khuyến nghị theo insight thực tế

---
Dữ liệu:
- Nguồn: IBM HR Analytics Employee Attrition & Performance Dataset
- Số lượng: 1.470 dòng, 35 cột
- Loại dữ liệu: Snapshot (thời điểm), không phải dữ liệu chuỗi thời gian
- Một số biến quan trọng:
  - Attrition: Tình trạng nghỉ việc (Yes/No)
  - Age, MonthlyIncome, DistanceFromHome, OverTime
  - Department, JobRole, JobLevel, YearsAtCompany

---
Công cụ sử dụng:
- Python (pandas, seaborn, matplotlib) – Xử lý và khám phá dữ liệu ban đầu
- Power BI – Phân tích và trực quan hóa
- DAX – Tạo các Measure tính toán

---

Dashboard

![HR_DASHBOARD](https://github.com/user-attachments/assets/7812aefc-47ae-4c9e-85f8-ded9b33d2225)


> Xem toàn bộ dashboard trong [Dashboard.pbix](Dashboard.pbix)

---

Insight :
- Tỷ lệ nghỉ việc toàn công ty: 16.12%
- Nhân viên có tăng ca nghỉ việc cao gấp 3 lần nhóm không tăng ca
- Nhóm Sales và nhân viên cấp thấp có tỷ lệ nghỉ cao nhất
- Nhân viên <30 tuổi và lương <4000 USD có xu hướng nghỉ nhiều
- Khoảng cách xa nơi làm việc (Distance > 10km) làm tăng tỷ lệ nghỉ

---

Đề xuất :
- Tăng đãi ngộ cho nhân viên cấp thấp (Vì đây là nhóm nghỉ nhiều nhất)
- Rà soát và giảm tăng ca. Vì tăng ca là nguyên nhân cao dẫn đến nghỉ việc
- Thiết kế lộ trình thăng tiến rõ ràng cho nhân viên trẻ, giúp nhân viên có cái nhìn khách quan và định hướng lâu dài về công việc của mình
- Xem xét tăng lương cơ bản ở nhóm thu nhập thấp vì nhóm này có xu hướng nghỉ việc cao hơn 
- Hỗ trợ giao thông hoặc chi phí di chuyển đến nơi làm việc cho các nhân viên nhà ở xa công ty

#powerbi #data-analytics #python
 
