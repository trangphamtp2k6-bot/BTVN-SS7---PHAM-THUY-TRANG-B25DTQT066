# BÁO CÁO PHÂN TÍCH ĐỘ NHẠY CỦA TỶ LỆ HỦY BÀN VÀ CHÍNH SÁCH ĐẶT CỌC

**Doanh nghiệp nghiên cứu:** Pizza 4P's (Chi nhánh Phan Kế Bính)
**Người thực hiện:** Trưởng nhóm Phân tích Doanh thu Nhà hàng (Revenue Management Lead)
**Mã học phần:** BI301 - S07

## PHẦN 1: LƯỢNG HÓA TỔN THẤT TÀI CHÍNH DO NO-SHOW HIỆN TẠI

Hiện tượng No-show (đặt bàn nhưng không đến và không báo trước) gây ra tổn thất kép cho nhà hàng: vừa mất doanh thu từ khách đặt trước, vừa làm lãng phí cơ hội phục vụ khách vãng lai (Walk-in) do phải giữ bàn trống trung bình $30$ phút. 

Dựa trên dữ liệu mỗi tối cuối tuần, chúng ta lượng hóa tổn thất như sau:

*   **Tổng số lượt đặt bàn:** $150$ lượt.
*   **Số lượng bàn No-show:** $150 \times 18\% = 27$ bàn.
*   **Số lượng bàn thực tế phục vụ (Show-up):** $150 - 27 = 123$ bàn.

**Tổn thất doanh thu trực tiếp từ No-show:**
$$
\text{Tổn thất} = \text{Số bàn No-show} \times \text{Giá trị trung bình/bàn} = 27 \times 1,200,000 = 32,400,000 \text{ VNĐ}
$$

**Doanh thu hiện tại từ khách đặt bàn:**
$$
\text{Doanh thu hiện tại} = 123 \times 1,200,000 = 147,600,000 \text{ VNĐ}
$$

*Nhận xét:* Việc mất đi hơn $32$ triệu VNĐ mỗi tối cuối tuần chỉ vì khách hàng không xuất hiện là một sự lãng phí công suất cực kỳ nghiêm trọng, đặc biệt trong bối cảnh nhà hàng phải từ chối tới $45$ lượt khách vãng lai do lầm tưởng rằng đã hết bàn.

---

## PHẦN 2: PHÂN TÍCH ĐỘ NHẠY KỊCH BẢN ÁP DỤNG ĐẶT CỌC

Giả định nhà hàng áp dụng chính sách bắt buộc đặt cọc trực tuyến $200,000$ VNĐ/bàn. Theo khảo sát độ nhạy, điều này tạo ra một rào cản nhỏ khiến tổng lượng đặt bàn giảm $10\%$, nhưng lại đóng vai trò như một cam kết tài chính mạnh mẽ, kéo tỷ lệ No-show xuống chỉ còn $2\%$.

**1. Biến động lượng khách đặt bàn:**
*   **Số bàn đặt trước mới:** $150 \times (100\% - 10\%) = 135$ bàn.
*   **Số bàn No-show mới:** $135 \times 2\% = 2.7 \approx 3$ bàn.
*   **Số bàn đặt trước thực tế đến (Show-up):** $135 - 3 = 132$ bàn.

**2. Giải phóng công suất cho khách vãng lai (Walk-in):**
Trước đây, nhà hàng bị "khóa" $150$ bàn cho khách đặt trước. Khi áp dụng đặt cọc, lượng đặt bàn giảm xuống $135$, giúp nhà hàng giải phóng ngay lập tức $15$ bàn ngay từ đầu ca.
Với nhu cầu từ $45$ khách Walk-in bị từ chối mỗi tối, nhà hàng hoàn toàn có thể lấp đầy $15$ bàn trống này ngay lập tức.

**3. Tính toán lại doanh thu trong kịch bản mới:**
*   Doanh thu từ khách đặt bàn (đã đến): $132 \times 1,200,000 = 158,400,000$ VNĐ.
*   Doanh thu từ phí đặt cọc của khách No-show (bị giữ lại): $3 \times 200,000 = 600,000$ VNĐ.
*   Doanh thu từ khách Walk-in lấp vào chỗ trống: $15 \times 1,200,000 = 18,000,000$ VNĐ.

$$
\text{Tổng doanh thu mô phỏng} = 158,400,000 + 600,000 + 18,000,000 = 177,000,000 \text{ VNĐ}
$$

**Bảng so sánh hiệu quả tài chính:**

| Chỉ tiêu | Không đặt cọc (Hiện tại) | Có đặt cọc (Mô phỏng) | Chênh lệch |
| :--- | :--- | :--- | :--- |
| Số bàn đặt trước | $150$ | $135$ | $-15$ |
| Tỷ lệ No-show | $18\%$ | $2\%$ | $-16\%$ |
| Số bàn No-show | $27$ | $3$ | $-24$ |
| Khách Walk-in phục vụ thêm | $0$ | $15$ | $+15$ |
| **Tổng doanh thu ước tính** | $\mathbf{147,600,000 \text{ VNĐ}}$ | $\mathbf{177,000,000 \text{ VNĐ}}$ | $\mathbf{+29,400,000 \text{ VNĐ}}$ |

---

## PHẦN 3: KẾT LUẬN VÀ ĐỀ XUẤT CHÍNH SÁCH ĐẶT BÀN THÔNG MINH

### Kết luận từ mô hình phân tích độ nhạy
Mặc dù chính sách đặt cọc gây ra tâm lý e ngại ban đầu làm giảm $10\%$ tổng lượng khách đặt trước, nhưng nhờ triệt tiêu được tỷ lệ No-show "ảo" (giảm từ $18\%$ xuống $2\%$), nó đã giúp tinh lọc nhóm khách hàng có ý định dùng bữa thực sự. Quan trọng hơn, việc này giúp khôi phục công suất bị lãng phí để đón nhóm khách Walk-in đang có sẵn nhu cầu. 

Kết quả cuối cùng là **tổng doanh thu ròng mỗi tối cuối tuần tăng thêm $29,400,000$ VNĐ** (tương đương mức tăng trưởng gần $20\%$ so với hiện tại).

### Đề xuất chiến lược gửi Ban Giám đốc
Dựa trên những con số định lượng rõ ràng, tôi dứt khoát khuyến nghị Ban Giám đốc **triển khai ngay chính sách Đặt cọc giữ bàn trực tuyến**. Tuy nhiên, để tránh trải nghiệm tiêu cực cho khách hàng trung thành và đảm bảo triết lý "Delivering Wow, Sharing Happiness" của Pizza 4P's, chính sách cần được thiết kế thông minh (Smart Booking Policy) với các nguyên tắc sau:

1.  **Chỉ áp dụng vào khung giờ cao điểm:** Việc thu cọc chỉ nên kích hoạt vào các buổi tối cuối tuần (Thứ Sáu - Chủ Nhật) hoặc các ngày Lễ, Tết. Các ngày trong tuần có thể giữ nguyên chính sách không cọc để khuyến khích lượt đặt bàn.
2.  **Miễn trừ cho khách hàng thân thiết:** Tích hợp hệ thống CRM để tự động miễn phí đặt cọc cho các khách hàng có hạng thành viên (ví dụ: Gold, Platinum) hoặc những người có lịch sử đến đúng hẹn $100\%$.
3.  **Trải nghiệm thanh toán liền mạch:** Sử dụng các cổng thanh toán ví điện tử (ZaloPay, MoMo) hoặc Apple Pay để quá trình quẹt thẻ giữ cọc (Pre-authorization) diễn ra trong chưa tới $10$ giây, không làm gián đoạn hành trình đặt bàn của khách. Khoản cọc sẽ tự động trừ thẳng vào hóa đơn cuối cùng.