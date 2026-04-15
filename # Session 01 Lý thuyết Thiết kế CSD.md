# Session 01: Lý thuyết Thiết kế CSDL & ERD

## Lesson 01: Cơ sở dữ liệu (Database)
- Khái niệm cơ bản
  - Dữ liệu (Data): Các thông tin thô, sự kiện, con số chưa qua xử lý
  - Cơ sở dữ liệu (Database): Tập hợp dữ liệu được tổ chức có cấu trúc, có liên quan logic và lưu trữ trên máy tính
- Lợi ích của CSDL
  - Giảm thiểu sự dư thừa dữ liệu (Data redundancy)
  - Đảm bảo tính nhất quán (Consistency)
  - Chia sẻ dữ liệu dễ dàng cho nhiều người dùng cùng lúc
  - Tăng cường bảo mật và toàn vẹn dữ liệu
- Các mô hình CSDL phổ biến
  - Mô hình phân cấp (Hierarchical): Cấu trúc hình cây (Cha - con)
  - Mô hình mạng (Network): Dữ liệu liên kết dạng đồ thị/lưới
  - Mô hình quan hệ (Relational - RDBMS): Phổ biến nhất, lưu trữ dạng bảng (Dòng & Cột)
  - Mô hình hướng đối tượng (Object-Oriented): Lưu trữ dữ liệu dưới dạng đối tượng (như lập trình OOP)

## Lesson 02: Hệ quản trị CSDL MySQL
- Hệ quản trị CSDL (DBMS)
  - Định nghĩa: Phần mềm giúp tạo lập, quản lý và kiểm soát truy cập vào Database
  - Chức năng: Lưu trữ, truy xuất, bảo mật và sao lưu dữ liệu
- MySQL là gì?
  - Là một Hệ quản trị CSDL quan hệ (RDBMS)
  - Đặc điểm: Mã nguồn mở (Open-source), hiệu năng cao, cộng đồng lớn
  - Kiến trúc: Hoạt động theo mô hình Client - Server
- Công cụ thao tác
  - CLI (Command Line Interface): Thao tác bằng giao diện dòng lệnh
  - GUI (Graphical User Interface): Thao tác bằng giao diện đồ họa (VD: MySQL Workbench, DBeaver, Navicat...)

## Lesson 03: Xây dựng mô hình quan hệ thực thể (ERD)
- Khái niệm ERD
  - Là bản vẽ mô hình trực quan thể hiện cấu trúc logic của cơ sở dữ liệu
  - Là cầu nối giao tiếp giữa người thiết kế, lập trình viên và khách hàng
- Thành phần chính của ERD
  - Thực thể (Entity): Đối tượng thực tế cần quản lý (VD: Học sinh, Sản phẩm). Ký hiệu: Hình chữ nhật
  - Thuộc tính (Attribute): Thông tin, đặc điểm của thực thể (VD: Tên, Tuổi). Ký hiệu: Hình Oval/Ellipse
  - Khóa chính (Primary Key - PK): Thuộc tính định danh duy nhất cho mỗi bản ghi (VD: Mã HS, Số CCCD)
  - Khóa ngoại (Foreign Key - FK): Thuộc tính dùng để liên kết các thực thể với nhau
  - Mối quan hệ (Relationship): Sự tương tác, liên kết giữa các thực thể. Ký hiệu: Hình thoi
- Các loại quan hệ (Cardinality)
  - 1-1 (One to One): 1 đối tượng A liên kết với đúng 1 đối tượng B (VD: 1 Người - 1 Hộ chiếu)
  - 1-N (One to Many): 1 đối tượng A liên kết với nhiều đối tượng B (VD: 1 Lớp học - Nhiều Học sinh)
  - N-N (Many to Many): Nhiều đối tượng A liên kết với nhiều đối tượng B (VD: Sinh viên - Môn học)

## Lesson 04: Ngôn ngữ SQL trong CSDL
- Tổng quan về SQL
  - SQL (Structured Query Language): Ngôn ngữ truy vấn mang tính cấu trúc
  - Chức năng: Giao tiếp, thao tác và quản trị dữ liệu bên trong các RDBMS
- Phân loại các nhóm lệnh SQL chính
  - DDL (Data Definition Language) - Định nghĩa cấu trúc
    - CREATE: Tạo mới Database, Bảng (Table)
    - ALTER: Chỉnh sửa cấu trúc bảng (thêm, sửa kiểu dữ liệu, xóa cột)
    - DROP: Xóa hoàn toàn bảng hoặc cấu trúc Database
  - DML (Data Manipulation Language) - Thao tác dữ liệu
    - SELECT: Truy vấn, lọc và lấy dữ liệu ra để xem
    - INSERT: Thêm bản ghi (dòng dữ liệu) mới vào bảng
    - UPDATE: Cập nhật, sửa đổi dữ liệu đã tồn tại
    - DELETE: Xóa bản ghi trong bảng
  - DCL (Data Control Language) - Điều khiển dữ liệu
    - GRANT: Cấp quyền truy cập cho User
    - REVOKE: Thu hồi quyền của User
  - TCL (Transaction Control Language) - Quản lý giao dịch
    - COMMIT: Xác nhận và lưu vĩnh viễn các thay đổi
    - ROLLBACK: Hoàn tác, hủy bỏ các thay đổi (thường dùng khi có lỗi)