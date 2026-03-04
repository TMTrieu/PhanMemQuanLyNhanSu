# 📌 Phần mềm Quản lý Nhân sự

## 🎯 Giới thiệu

Phần mềm quản lý nhân sự được xây dựng bằng WinForms (C#) kết hợp DevExpress để thiết kế giao diện, và ADO.NET để truy vấn dữ liệu từ SQL Server.
Ứng dụng có chức năng quản lý thông tin nhân viên, quản lý báo cáo và hợp đồng, chấm công và tính lương.

## 🛠️ Công nghệ sử dụng

- **Ngôn ngữ:** C# (.NET Framework / WinForms)
- **UI Framework:** DevExpress WinForms Controls
- **Cơ sở dữ liệu:** Microsoft SQL Server
- **Truy vấn dữ liệu:** ADO.NET (SqlConnection, SqlCommand, SqlDataReader)
- **Mô hình kiến trúc:** 3 lớp

## ✨ Các chức năng chính

- Quản lý nhân viên (thêm, sửa, xóa, tìm kiếm)
- Quản lý phòng ban, bộ phận, chức vụ, dân tộc, tôn giáo
- Quản lý hợp đồng lao động
- Chấm công, duyệt thôi việc
- Tính lương nhân viên theo kỳ công
- Quản lý báo cáo

## 🚀 Cài đặt

### Yêu cầu

- Visual Studio 2019 hoặc mới hơn
- .NET Framework 4.7.2
- Microsoft SQL Server

### Các bước cài đặt

1.  **Clone repository:**
    ```bash
    git clone https://github.com/TMTrieu/PhanMemQuanLyNhanSu.git
    ```

2.  **Phục hồi cơ sở dữ liệu:**
    - Mở SQL Server Management Studio (SSMS).
    - Tạo một database mới với tên `QuanLyNhanSu`.
    - Mở file `database.sql` từ thư mục gốc của dự án.
    - Chạy script trong file `database.sql` để tạo các bảng và dữ liệu cần thiết cho database `QuanLyNhanSu`.

3.  **Mở dự án trong Visual Studio:**
    - Mở file `QuanLyNhanSu.sln` bằng Visual Studio.
    - Build solution để restore các packages cần thiết.

## 💻 Sử dụng

Sau khi hoàn tất các bước cài đặt, bạn có thể chạy dự án bằng cách nhấn `F5` hoặc nút `Start` trong Visual Studio.

## 📂 Cấu trúc thư mục

Dự án được xây dựng theo mô hình kiến trúc 3 lớp:

-   **`DataLayer` (DL):** Chịu trách nhiệm kết nối và truy vấn cơ sở dữ liệu. Lớp này chứa các phương thức để thực hiện các thao tác CRUD (Create, Read, Update, Delete) với database.
-   **`BusinessLayer` (BL):** Chứa các logic nghiệp vụ của ứng dụng. Lớp này xử lý các yêu cầu từ `PresentationLayer`, gọi đến `DataLayer` để truy xuất dữ liệu và thực hiện các quy tắc nghiệp vụ.
-   **`PresentationLayer` (PL):** Là lớp giao diện người dùng (WinForms). Lớp này hiển thị dữ liệu và nhận các tương tác từ người dùng, sau đó chuyển các yêu cầu xử lý cho `BusinessLayer`.
