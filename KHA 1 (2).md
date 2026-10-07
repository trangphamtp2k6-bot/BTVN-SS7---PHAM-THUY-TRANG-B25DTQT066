# BÁO CÁO PHÂN TÍCH CHỈ SỐ VẬN HÀNH REVPASH VÀ CÔNG SUẤT CHỖ NGỒI
**Doanh nghiệp nghiên cứu:** Pizza 4P's (Chi nhánh Bến Thành - Thứ Bảy)
**Người thực hiện:** Chuyên viên Phân tích Hiệu suất Nhà hàng (Restaurant Performance Analyst)
**Mã học phần:** BI301 - S07

---

## PHẦN 1: TÍNH TOÁN TỶ LỆ LẤP ĐẦY CHỖ NGỒI (SEAT OCCUPANCY RATE)

Để đánh giá chính xác hiệu suất sử dụng không gian, chúng ta cần xác định lượng ghế có sẵn trong từng khung giờ (Available Seat Hours - ASH) và tỷ lệ lấp đầy thực tế.

**Các công thức áp dụng:**
*   Tổng số ghế khả dụng theo giờ: 
    $$\text{ASH} = \text{Số giờ vận hành} \times \text{Tổng số ghế khả dụng}$$
*   Tỷ lệ lấp đầy chỗ ngồi: 
    $$\text{Seat Occupancy Rate} = \left( \frac{\text{Lượt khách phục vụ}}{\text{ASH}} \right) \times 100\%$$

**Bảng tính toán Seat Occupancy Rate chi tiết:**

| Khung giờ hoạt động | Số giờ | Tổng ghế | Available Seat Hours (ASH) | Lượt khách phục vụ | Tỷ lệ lấp đầy (Occupancy Rate) |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Bữa trưa** (11h00 - 14h00) | $3$ | $120$ | $360$ | $300$ | $\mathbf{83.33\%}$ |
| **Giờ thấp điểm** (14h00 - 17h00) | $3$ | $120$ | $360$ | $72$ | $\mathbf{20.00\%}$ |
| **Bữa tối** (17h00 - 22h00) | $5$ | $120$ | $600$ | $600$ | $\mathbf{100.00\%}$ |

---

## PHẦN 2: TÍNH TOÁN CHỈ SỐ REVPASH VÀ NHẬN XÉT

Chỉ số RevPASH (Revenue Per Available Seat Hour) cho biết mỗi chỗ ngồi trong một giờ tạo ra bao nhiêu doanh thu, là thước đo cốt lõi để tối ưu hóa lợi nhuận trên chi phí mặt bằng cố định.

**Công thức áp dụng:**
$$\text{RevPASH} = \frac{\text{Tổng doanh thu ghi nhận}}{\text{Available Seat Hours}}$$

**Bảng tính toán chỉ số RevPASH:**

| Khung giờ hoạt động | Tổng doanh thu (VNĐ) | Available Seat Hours | RevPASH (VNĐ/ghế/giờ) |
| :--- | :--- | :---: | :--- |
| **Bữa trưa** | $75,000,000$ | $360$ | $\mathbf{208,333}$ |
| **Giờ thấp điểm** | $18,000,000$ | $360$ | $\mathbf{50,000}$ |
| **Bữa tối** | $180,000,000$ | $600$ | $\mathbf{300,000}$ |

### Phân tích và so sánh hiệu quả sinh lời

Dựa vào các chỉ số trên, có thể thấy rõ sự phân hóa mạnh mẽ về hiệu quả khai thác mặt bằng và khả năng sinh lời giữa các khung giờ trong ngày cuối tuần tại chi nhánh Bến Thành.

**1. Khung giờ Bữa tối (Khung giờ vàng):** 
Bữa tối đang là thời điểm mang lại hiệu suất cao nhất với Tỷ lệ lấp đầy đạt mức tuyệt đối $100\%$ và chỉ số RevPASH vô cùng ấn tượng ở mức $300,000$ VNĐ. Điều này hoàn toàn phù hợp với hành vi tiêu dùng của khách hàng Pizza 4P's: ưu tiên dùng bữa tối cuối tuần bên gia đình, bạn bè và sẵn sàng chi trả cao hơn cho các món ăn kèm, rượu vang hoặc tráng miệng, giúp gia tăng giá trị trung bình trên mỗi hóa đơn. Tuy nhiên, tỷ lệ lấp đầy $100\%$ cũng là tín hiệu cảnh báo nhà hàng có thể đang phải từ chối nhiều khách hàng do hết bàn (turnaway), gây thất thoát doanh thu tiềm năng.

**2. Khung giờ thấp điểm buổi chiều (Điểm nghẽn vận hành):** 
Trái ngược với bữa tối, giai đoạn 14h00 - 17h00 ghi nhận hiệu quả sinh lời thấp nhất. Tỷ lệ lấp đầy rơi tự do xuống chỉ còn $20\%$, kéo theo chỉ số RevPASH chạm đáy ở mức $50,000$ VNĐ (chỉ bằng $\approx 1/6$ so với bữa tối). Nguyên nhân cốt lõi là do đặc thù món ăn (Pizza/Mì Ý) thường được mặc định là món chính (main course) thay vì món ăn nhẹ buổi xế. Trong khi đó, chi phí cố định (tiền thuê mặt bằng, khấu hao, năng lượng) và một phần chi phí nhân sự vẫn phải duy trì liên tục, tạo ra gánh nặng lớn lên biên lợi nhuận của toàn bộ ngày hoạt động.

**Đề xuất chiến lược ngắn hạn:**
Sự chênh lệch lên đến $250,000$ VNĐ cho mỗi ghế/giờ giữa hai khung giờ đòi hỏi chuỗi phải có chiến lược điều tiết. Chi nhánh Bến Thành cần triển khai các chiến dịch thu hút khách vào giờ thấp điểm (ví dụ: ra mắt thực đơn "Afternoon Tea" hoặc "Dessert Combo" với các loại phô mai ngọt; ưu đãi Happy Hour cho đồ uống) nhằm tăng RevPASH ca chiều tối thiểu lên mức $100,000$ VNĐ. Đồng thời, vào bữa tối, cần tối ưu hóa quy trình phục vụ và thời gian chế biến để rút ngắn thời gian lưu lại của khách (Table Turnover Time), từ đó có thể khai thác vượt mức $100\%$ công suất nhờ quay vòng bàn nhanh.