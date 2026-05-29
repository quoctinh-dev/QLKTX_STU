# 🏢 HỆ THỐNG QUẢN LÝ KÝ TÚC XÁ - ĐỒ ÁN THỰC TẬP TỐT NGHIỆP

Hệ thống Quản lý Ký túc xá (QL_KTX_STU) là sản phẩm thuộc báo cáo **Thực tập tốt nghiệp Chuyên ngành Công nghệ Thông tin** tại trường Đại học Công nghệ Sài Gòn (STU). 

Dự án được xây dựng nhằm mục đích bước đầu số hóa quy trình quản lý vận hành nội trú sinh viên, giải quyết bài toán cốt lõi về tối ưu hóa không gian lưu trú thông qua việc quản lý chi tiết đến từng sơ đồ giường trong phòng, tiếp nhận đơn đăng ký trực tuyến và đồng bộ kênh thông báo giữa Ban quản lý và Sinh viên.

---

## 🛠️ Công nghệ Sử dụng & Kiến trúc

Hệ thống được phát triển dựa trên các công nghệ tiêu chuẩn, đảm bảo tính tổ chức dữ liệu chặt chẽ và giao diện trực quan:

*   **Backend Framework:** Laravel 12 (PHP 8.2+) áp dụng kiến trúc MVC tiêu chuẩn.
*   **Database:** MySQL 8.0 (Thiết kế chuẩn hóa các mối quan hệ cấu trúc phòng ở và danh sách sinh viên).
*   **Frontend Ecosystem:** Blade Template, Tailwind CSS, Vite.
*   **DevOps / CI/CD:** GitHub Actions (Cấu hình tự động hóa quy trình kiểm thử và FTP Deploy).

---

## ✨ Các Tính năng Hiện tại của Hệ thống (Current Features)

### 1. Phân hệ Quản trị (Admin Dashboard)
*   **Quản lý Phòng ở (Room Management):** Khởi tạo danh mục phòng, cấu hình phân loại phòng (phòng nam, phòng nữ) và cập nhật trạng thái phòng.
*   **Quản lý Sơ đồ Giường (Bed Management):** Quản lý chi tiết vị trí giường trong từng phòng, thiết lập số lượng giường tối đa nhằm kiểm soát chính xác sức chứa và tỷ lệ lấp đầy.
*   **Xử lý Đơn Đăng ký (Registration Processing):** Tiếp nhận danh sách đơn đăng ký nội trú của sinh viên trực tuyến, phê duyệt và điều phối sinh viên vào đúng vị trí phòng/giường còn trống.
*   **Hệ thống Thông báo (Announcement System):** Soạn thảo và phát hành các thông báo chung (nội quy, lịch sinh hoạt, thông tin khẩn cấp) đến toàn thể sinh viên nội trú.

### 2. Phân hệ Sinh viên (Student Portal)
*   **Đăng ký Nội trú (Online Registration):** Sinh viên gửi yêu cầu đăng ký ở ký túc xá trực tuyến thông qua hệ thống thay vì làm thủ tục giấy truyền thống.
*   **Nhận Thông báo (Notification Feed):** Kênh hiển thị toàn bộ các thông báo, bảng tin mới nhất từ Ban quản lý ký túc xá theo thời gian thực.

---

## 🚀 Định hướng Phát triển Kế tiếp (Future Roadmap)
*   Tích hợp phân hệ Quản lý và tính hóa đơn dịch vụ định kỳ (Điện, Nước, Internet).
*   Xây dựng hệ thống tiếp nhận phản ánh sự cố cơ sở vật chất (Ticket Support System) cho sinh viên.
*   Phát triển biểu đồ thống kê chuyên sâu phục vụ công tác báo cáo doanh thu và mật độ sinh viên nội trú.

---

## 📁 Cấu trúc Thư mục Dự án (Standard Laravel Layout)

Dự án tuân thủ nghiêm ngặt cấu trúc thư mục gốc của Laravel để dễ dàng bảo trì và phát triển:

```text
QL_KTX_STU/
├── app/
│   ├── Http/Controllers/   # Xử lý logic điều hướng và nghiệp vụ hệ thống
│   ├── Models/             # Định nghĩa cấu trúc dữ liệu và mối quan hệ Eloquent ORM
│   └── Providers/          # Cấu hình các dịch vụ cốt lõi của hệ thống
├── bootstrap/              # Khởi tạo và tối ưu hóa hiệu năng ứng dụng
├── config/                 # Chứa toàn bộ các tệp cấu hình (App, Database, Mail...)
├── database/
│   ├── migrations/         # Mã nguồn khởi tạo tự động các bảng trong MySQL
│   └── seeders/            # Dữ liệu mẫu (Seed Data) phục vụ mục đích kiểm thử
├── public/                 # Thư mục gốc chứa file index.php và tài nguyên tĩnh công khai
├── resources/
│   ├── views/              # Giao diện hệ thống dựng bằng Blade Template (Admin/Student)
│   └── css/ & js/          # Các tệp mã nguồn Frontend (Tailwind CSS, JavaScript)
├── routes/                 # Định nghĩa toàn bộ các tuyến đường (Routes) giao diện web
├── storage/                # Lưu trữ logs hệ thống, bộ nhớ đệm và tệp tin tải lên
├── tests/                  # Thư mục chứa các tệp kiểm thử tự động (Unit/Feature Test)
├── artisan                 # Công cụ dòng lệnh mạnh mẽ của Laravel CLI
├── composer.json           # Quản lý các thư viện PHP phụ thuộc
└── package.json            # Quản lý các công cụ và thư viện Frontend

# 🚀 Hướng dẫn Cài đặt & Chạy Dự án trên Local

## Bước 1: Tải mã nguồn về máy

```bash
git clone https://github.com/quoctinh-dev/QLKTX_STU.git
cd QLKTX_STU
```

---

## Bước 2: Cài đặt các thư viện PHP và Frontend

```bash
composer install
npm install
npm run build
```

---

## Bước 3: Cấu hình môi trường hệ thống

Sao chép file cấu hình mẫu:

```bash
cp .env.example .env
```

Mở file `.env` và cập nhật thông tin kết nối cơ sở dữ liệu MySQL:

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=ten_database_cua_ban
DB_USERNAME=root
DB_PASSWORD=your_password
```

---

## Bước 4: Khởi tạo khóa ứng dụng và dữ liệu hệ thống

Tạo Application Key:

```bash
php artisan key:generate
```

Thực hiện Migration và Seed dữ liệu mẫu:

```bash
php artisan migrate --seed
```

---

## Bước 5: Khởi chạy hệ thống

```bash
php artisan serve
```

Sau khi khởi động thành công, truy cập hệ thống tại:

```text
http://127.0.0.1:8000
```

---

# 🔐 Tài khoản Đăng nhập Thử nghiệm

Hệ thống được cung cấp sẵn dữ liệu mẫu để kiểm thử nhanh các chức năng hiện có.

| Vai trò   | Email                                         | Mật khẩu |
| --------- | --------------------------------------------- | -------- |
| Admin     | [admin@test.com](mailto:admin@test.com)       | 123456   |
| Sinh viên | [sinhvien@test.com](mailto:sinhvien@test.com) | 123456   |

---

# 📋 Yêu cầu Hệ thống

* PHP 8.2 trở lên
* Composer
* Node.js & NPM
* MySQL Server
* Git

---

# 🤝 Thành viên Thực hiện

### Nguyễn Quốc Tịnh

* GitHub: https://github.com/quoctinh-dev

### Nguyễn Châu Triệu Vỹ

**Trường:** Đại học Công nghệ Sài Gòn (STU)

---

# 📄 Giấy phép

Dự án được phát triển phục vụ mục đích học tập, nghiên cứu và thực hiện đồ án tốt nghiệp tại Đại học Công nghệ Sài Gòn (STU).

