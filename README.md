Chương 1
Kết quả trải nghiệm trò chơi Can't Unsee
<img width="3068" height="1648" alt="screenshot_1767597951" src="https://github.com/user-attachments/assets/1eadfcc0-6734-4b9f-a61a-9fc79d707858" />

Điểm đạt được: 5780

Xếp hạng: Beginner

Thời gian hoàn thành: 00:06:34

Ảnh trên minh họa kết quả hoàn thành trò chơi Can't Unsee, được sử dụng làm ví dụ minh họa cho giao diện và kết quả của người dùng.

CHƯƠNG 2: KIỂM THỬ ĐƠN VỊ VỚI JUNIT (10/01/2026)
1. Thông tin chung
Yêu cầu: Viết Unit Test cho chương trình phân tích điểm học sinh.
Công cụ thực hiện: VS Code, Java, Maven, JUnit 4.13.2.
2. Cấu trúc dự án
unit-test/
├── src/
│   └── StudentAnalyzer.java      # Mã nguồn chính (Chức năng)
├── test/
│   └── StudentAnalyzerTest.java  # Mã nguồn kiểm thử (Test Cases)
├── pom.xml                       # Cấu hình thư viện Maven
└── README.md                     # File báo cáo này
3. Mô tả bài toán
Xây dựng lớp StudentAnalyzer để phân tích điểm số học sinh với yêu cầu xử lý dữ liệu chặt chẽ (Validate dữ liệu đầu vào).

Các chức năng đã cài đặt:
countExcellentStudents(List<Double> scores)

Mục tiêu: Đếm số lượng học sinh đạt loại Giỏi (Điểm >= 8.0).
Logic xử lý: Duyệt qua danh sách, tự động bỏ qua các điểm số không hợp lệ (nhỏ hơn 0 hoặc lớn hơn 10).
calculateValidAverage(List<Double> scores)

Mục tiêu: Tính điểm trung bình cộng của cả lớp.
Logic xử lý: Chỉ cộng tổng các điểm hợp lệ (0-10). Trả về 0.0 nếu danh sách rỗng để tránh lỗi chia cho 0.
4. Thiết kế kiểm thử (Test Cases)
Sử dụng JUnit 4 để viết các kịch bản kiểm thử tự động trong file StudentAnalyzerTest.java:

ID	Kịch bản (Scenario)	Dữ liệu đầu vào (Input)	Mong đợi (Expected)	Ghi chú
#1	Dữ liệu hỗn hợp	9.0, 8.5, 7.0, -1.0	Đếm giỏi: 2	Bỏ qua điểm lỗi -1.0
#2	Danh sách rỗng	Empty List	Trả về 0	Kiểm tra độ ổn định
#3	Dữ liệu biên	8.0	Đếm giỏi: 1	Kiểm tra toán tử >=
#4	Tính trung bình	9.0, 8.5, 7.0	Kết quả: ~8.167	Sai số cho phép 0.01
5. Hướng dẫn chạy (How to run)
Mở thư mục dự án bằng VS Code.
Đợi Maven tải thư viện JUnit (trong file pom.xml).
Mở file test/StudentAnalyzerTest.java.
Nhấn nút Play (▶) màu xanh bên cạnh tên Class hoặc tên hàm để chạy test.
