Chương 1.
## Kết quả trải nghiệm trò chơi Can't Unsee
<img width="3068" height="1648" alt="screenshot_1767597951" src="https://github.com/user-attachments/assets/1eadfcc0-6734-4b9f-a61a-9fc79d707858" />
- Điểm đạt được: **5780**
- Xếp hạng: **Beginner**
- Thời gian hoàn thành: **00:06:34**

Ảnh trên minh họa kết quả hoàn thành trò chơi *Can't Unsee*, được sử dụng làm ví dụ minh họa giao diện và kết quả người dùng.







# 📊 Bài tập thực hành kiểm thử với JUnit

## Chủ đề: Phân tích dữ liệu điểm số học sinh

---

## 🎯 Mục tiêu học tập

Bài tập này giúp sinh viên:

* Hiểu và **viết kiểm thử tự động bằng JUnit 5** cho chương trình Java.
* Rèn luyện kỹ năng **phân tích yêu cầu, xử lý dữ liệu đầu vào không hợp lệ**.
* Biết cách **tổ chức project**, làm việc với **GitHub Issues – Commit – README**.
* Bước đầu **khai thác AI tạo sinh** (như ChatGPT) để hỗ trợ lập trình và kiểm thử.

---

## 📌 Mô tả bài toán

Xây dựng chương trình Java để phân tích điểm số học sinh, bao gồm:

* Đếm số học sinh đạt loại **Giỏi** (điểm ≥ 8.0)
* Tính **điểm trung bình hợp lệ**

📌 **Quy ước dữ liệu hợp lệ**:

* Điểm hợp lệ nằm trong khoảng **0 → 10**
* Điểm < 0 hoặc > 10 được xem là **dữ liệu sai và bị bỏ qua**
* Nếu danh sách rỗng → trả về **0**

---

## 🧱 Cấu trúc dự án

```text
unit-test/
│
├── src/
│   └── StudentAnalyzer.java
│
├── test/
│   └── StudentAnalyzerTest.java
│
└── README.md
```

---

## 🧩 Mô tả lớp `StudentAnalyzer`

### 1️⃣ countExcellentStudents

```java
public int countExcellentStudents(List<Double> scores)
```

**Chức năng**:

* Đếm số học sinh có điểm **≥ 8.0**

**Yêu cầu xử lý**:

* Bỏ qua điểm < 0 hoặc > 10
* Nếu danh sách rỗng → trả về 0

---

### 2️⃣ calculateValidAverage

```java
public double calculateValidAverage(List<Double> scores)
```

**Chức năng**:

* Tính điểm trung bình của các điểm hợp lệ

**Yêu cầu xử lý**:

* Chỉ tính các điểm từ 0 → 10
* Nếu không có điểm hợp lệ → trả về 0

---

## 🧪 Kiểm thử đơn vị với JUnit 5

### 🎯 Mục tiêu kiểm thử

* Đảm bảo các phương thức hoạt động đúng trong mọi tình huống
* Phát hiện lỗi logic sớm trong quá trình phát triển

### 📂 Lớp kiểm thử

`StudentAnalyzerTest.java`

### ✅ Các nhóm test case

#### 1️⃣ Trường hợp bình thường

* Danh sách có cả điểm hợp lệ và không hợp lệ
* Danh sách toàn bộ điểm hợp lệ

#### 2️⃣ Trường hợp biên

* Danh sách rỗng
* Danh sách chỉ chứa 0 hoặc 10

#### 3️⃣ Trường hợp dữ liệu sai

* Có điểm < 0
* Có điểm > 10

---

### 🔎 Ví dụ test case

```java
@Test
public void testCountExcellentStudents() {
    StudentAnalyzer analyzer = new StudentAnalyzer();
    assertEquals(2, analyzer.countExcellentStudents(
        Arrays.asList(9.0, 8.5, 7.0, 11.0, -1.0)
    ));
    assertEquals(0, analyzer.countExcellentStudents(Collections.emptyList()));
}
```

---

## ▶️ Hướng dẫn chạy chương trình

### 🔧 Yêu cầu môi trường

* **Java JDK 8+**
* IDE: IntelliJ IDEA / Eclipse / VS Code
* **JUnit 5 (JUnit Jupiter)**

---

### ▶️ Cách chạy test

#### Cách 1: Chạy trong IDE

* Mở file `StudentAnalyzerTest.java`
* Chuột phải → **Run Test**

#### Cách 2: Chạy bằng Maven (nếu có)

```bash
mvn test
```

---

## 🐙 Quản lý công việc với GitHub Issues

### 📌 Danh sách Issues

| Issue | Tên                             | Mô tả                               |
| ----- | ------------------------------- | ----------------------------------- |
| #1    | Viết hàm countExcellentStudents | Đếm học sinh giỏi, validate dữ liệu |
| #2    | Viết hàm calculateValidAverage  | Tính trung bình điểm hợp lệ         |
| #3    | Viết test cho 2 hàm             | Dùng JUnit kiểm thử đầy đủ          |
| #4    | Viết README.md                  | Mô tả bài toán & hướng dẫn          |

---

## 📝 Quy ước commit message

Ví dụ:

```text
feat: implement countExcellentStudents() #1
test: add unit tests for StudentAnalyzer #3
docs: update README with instructions #4
```

📌 Có thể dùng:

* `fixes #1`
* `closes #2`

➡️ Issue sẽ **tự động đóng** khi merge vào nhánh chính






