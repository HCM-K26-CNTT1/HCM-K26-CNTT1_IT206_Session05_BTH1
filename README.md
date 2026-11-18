# BÀI THỰC HÀNH 1: LẬP KẾ HOẠCH TÀI CHÍNH CÁ NHÂN BẰNG CHAIN-OF-THOUGHT

## PHẦN 1. THIẾT KẾ GEMINI SKILL

### 1.1. Thông tin Skill

- Tên Skill: `financial-plan`
- Vai trò: Trợ lý chuyên lập kế hoạch tài chính cá nhân.
- Mục tiêu: Phân tích thu nhập, kiểm soát chi tiêu, thanh toán nợ và xây dựng kế hoạch tiết kiệm.
- Đầu vào: Thu nhập, thuế, chi phí cố định, khoản nợ, mục tiêu tiết kiệm.
- Đầu ra: Phân tích tính toán, bảng phân bổ ngân sách và đề xuất tài chính.

### 1.2. Nội dung Instructions

Bạn là chuyên gia hỗ trợ lập kế hoạch tài chính cá nhân. Hãy tiếp nhận dữ liệu tài chính của người dùng và xây dựng ngân sách hàng tháng một cách logic, chính xác.

Quy trình xử lý:

1. Kiểm tra tính đầy đủ và hợp lệ của dữ liệu đầu vào.
2. Tính thu nhập thực nhận sau thuế và bảo hiểm.
3. Trừ các khoản chi phí cố định bắt buộc.
4. Xác định khoản trả nợ tối thiểu và số dư còn lại.
5. Trích lập tiết kiệm tối thiểu 20% tổng thu nhập.
6. Phân bổ ngân sách còn lại theo quy tắc 50/30/20 cải tiến.
7. Kiểm tra tổng số tiền, tỷ lệ phần trăm và các ràng buộc tài chính.

Yêu cầu đầu ra:
- Phân tích các bước tính toán bằng công thức và số liệu trung gian.
- Bảng ngân sách Markdown gồm Hạng mục, Số tiền, Tỷ lệ %, Ghi chú.
- Đưa ra nhận xét và đề xuất tối ưu chi tiêu.
- Cảnh báo nếu thu nhập không đủ đáp ứng các nghĩa vụ tài chính.

## PHẦN 2. THỰC NGHIỆM PROMPT

### 2.1. Cung cấp dữ liệu đầu vào

**Prompt:**

Tôi muốn lập kế hoạch tài chính cá nhân hàng tháng. Dữ liệu gồm:
- Thu nhập: 15.000.000 VNĐ.
- Thuế và bảo hiểm: 1.000.000 VNĐ.
- Chi phí cố định: 4.000.000 VNĐ.
- Khoản nợ: 2.000.000 VNĐ.
- Mục tiêu tiết kiệm: 20% tổng thu nhập.

Hãy kiểm tra dữ liệu và xác nhận trước khi tính toán.

**Kết quả mong đợi:** AI xác nhận các khoản thu nhập, chi phí, nợ và mục tiêu tiết kiệm.

### 2.2. Tính thu nhập khả dụng

**Prompt:**

Hãy suy nghĩ từng bước một và tính toán chi tiết trước khi đưa ra quyết định. Xác định thu nhập thực nhận sau thuế, bảo hiểm và chi phí cố định. Trình bày công thức, kết quả và giải thích ý nghĩa của số tiền còn lại.

**Kết quả:**

Thu nhập ban đầu: 15.000.000 VNĐ.

Thu nhập sau thuế và bảo hiểm:

15.000.000 - 1.000.000 = 14.000.000 VNĐ.

Sau khi trừ chi phí cố định:

14.000.000 - 4.000.000 = 10.000.000 VNĐ.

Thu nhập còn lại: **10.000.000 VNĐ**.

### 2.3. Xử lý các khoản nợ

**Prompt:**

Tiếp tục phân tích ngân sách. Xác định số tiền cần dành cho thanh toán nợ 2.000.000 VNĐ. Tính số dư sau khi thanh toán và kiểm tra khả năng đáp ứng nghĩa vụ tài chính.

**Kết quả:**

10.000.000 - 2.000.000 = 8.000.000 VNĐ.

Số tiền còn lại: **8.000.000 VNĐ**.

### 2.4. Thiết lập mục tiêu tiết kiệm

**Prompt:**

Tính khoản tiết kiệm tối thiểu bằng 20% tổng thu nhập ban đầu. Kiểm tra khoản tiết kiệm có đáp ứng mục tiêu hay không và tính số tiền còn lại để phân bổ.

**Kết quả:**

15.000.000 × 20% = 3.000.000 VNĐ.

8.000.000 - 3.000.000 = 5.000.000 VNĐ.

Số tiền còn lại: **5.000.000 VNĐ**.

### 2.5. Phân bổ ngân sách theo quy tắc 50/30/20 cải tiến

**Prompt:**

Phân bổ 5.000.000 VNĐ còn lại thành ba nhóm:
- 50% nhu cầu thiết yếu phát sinh.
- 30% chi tiêu linh hoạt.
- 20% quỹ dự phòng.

Tính toán chi tiết và kiểm tra tổng phân bổ.

**Kết quả:**

- Thiết yếu: 5.000.000 × 50% = 2.500.000 VNĐ.
- Linh hoạt: 5.000.000 × 30% = 1.500.000 VNĐ.
- Dự phòng: 5.000.000 × 20% = 1.000.000 VNĐ.

Tổng: 2.500.000 + 1.500.000 + 1.000.000 = 5.000.000 VNĐ.

### 2.6. Tổng hợp và kiểm tra

**Prompt:**

Tổng hợp toàn bộ kết quả thành bảng Markdown. Tính tỷ lệ từng hạng mục trên tổng thu nhập 15.000.000 VNĐ. Kiểm tra tổng ngân sách bằng 100%, không bỏ sót khoản chi nào và đưa ra đề xuất quản lý tài chính.

## PHẦN 3. KẾT QUẢ CUỐI CÙNG

| Hạng mục | Số tiền (VNĐ) | Tỷ lệ | Ghi chú |
|---|---:|---:|---|
| Thuế và bảo hiểm | 1.000.000 | 6,67% | Bắt buộc |
| Chi phí cố định | 4.000.000 | 26,67% | Sinh hoạt |
| Trả nợ | 2.000.000 | 13,33% | Thanh toán đúng hạn |
| Tiết kiệm | 3.000.000 | 20,00% | Mục tiêu tiết kiệm |
| Thiết yếu phát sinh | 2.500.000 | 16,67% | Nhu cầu thiết yếu |
| Chi tiêu linh hoạt | 1.500.000 | 10,00% | Cá nhân |
| Quỹ dự phòng | 1.000.000 | 6,66% | Dự phòng |
| **Tổng cộng** | **15.000.000** | **100%** | Cân đối |

*Các tỷ lệ được làm tròn; tỷ lệ quỹ dự phòng được điều chỉnh phần hiển thị để tổng bằng 100%.*

## PHẦN 4. ĐÁNH GIÁ VÀ ĐỀ XUẤT

### 4.1. Đánh giá

- Đã thanh toán đầy đủ khoản nợ theo dữ liệu đầu vào.
- Đạt mục tiêu tiết kiệm 20% thu nhập.
- Có quỹ dự phòng riêng để xử lý chi phí phát sinh.
- Tổng ngân sách được phân bổ đầy đủ, không vượt thu nhập.

### 4.2. Đề xuất

Nên duy trì việc ghi chép chi tiêu hàng tháng, ưu tiên thanh toán nợ đúng hạn và không sử dụng khoản tiết kiệm cho những nhu cầu không cần thiết. Khi thu nhập biến động, cần cập nhật dữ liệu để Skill tính toán lại ngân sách phù hợp.
