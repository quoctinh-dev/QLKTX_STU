# HỆ THỐNG QUẢN LÝ KÝ TÚC XÁ (QLKTX_STU)

## Giới thiệu

Hệ thống Quản lý Ký túc xá (QLKTX_STU) là dự án được phát triển במסגרת báo cáo Thực tập tốt nghiệp chuyên ngành Công nghệ Thông tin tại Trường Đại học Công nghệ Sài Gòn (STU).

Hệ thống được xây dựng nhằm hỗ trợ công tác quản lý ký túc xá thông qua việc số hóa quy trình đăng ký nội trú, quản lý phòng ở, quản lý giường nằm và trao đổi thông tin giữa Ban quản lý với sinh viên. Dự án hướng đến việc nâng cao hiệu quả quản lý, giảm thiểu thao tác thủ công và tập trung hóa dữ liệu sinh viên nội trú.

---

## Công nghệ sử dụng

### Backend

* Laravel 12
* PHP 8.2+

### Frontend

* Blade Template
* Tailwind CSS
* Vite

### Cơ sở dữ liệu

* MySQL 8.0

### Công cụ phát triển

* Git
* GitHub Actions

---

## Chức năng hệ thống

### Phân hệ Quản trị viên

* Quản lý phòng ở.
* Quản lý giường trong từng phòng.
* Tiếp nhận và xử lý đơn đăng ký nội trú.
* Phân bổ sinh viên vào phòng và giường phù hợp.
* Quản lý thông báo và bảng tin.

### Phân hệ Sinh viên

* Đăng ký nội trú trực tuyến.
* Theo dõi các thông báo từ Ban quản lý.
* Xem thông tin lưu trú cá nhân.

---

## Hướng dẫn cài đặt

### 1. Tải mã nguồn

```bash
git clone https://github.com/quoctinh-dev/QLKTX_STU.git
cd QLKTX_STU
```

### 2. Cài đặt thư viện

```bash
composer install
npm install
npm run build
```

### 3. Cấu hình môi trường

Sao chép tệp cấu hình:

```bash
cp .env.example .env
```

Cập nhật thông tin kết nối cơ sở dữ liệu trong tệp `.env`:

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=your_database_name
DB_USERNAME=root
DB_PASSWORD=your_password
```

### 4. Khởi tạo hệ thống

Tạo khóa ứng dụng:

```bash
php artisan key:generate
```

Thực hiện migration và seed dữ liệu:

```bash
php artisan migrate --seed
```

### 5. Khởi chạy ứng dụng

```bash
php artisan serve
```

Truy cập hệ thống tại:

```text
http://127.0.0.1:8000
```

---

## Tài khoản thử nghiệm

| Vai trò       | Email                                         | Mật khẩu |
| ------------- | --------------------------------------------- | -------- |
| Quản trị viên | [admin@test.com](mailto:admin@test.com)       | 123456   |
| Sinh viên     | [sinhvien@test.com](mailto:sinhvien@test.com) | 123456   |

---

## Yêu cầu hệ thống

* PHP 8.2 trở lên
* Composer
* Node.js
* NPM
* MySQL 8.0
* Git

---

## Nhóm thực hiện

* Nguyễn Quốc Tịnh
* Nguyễn Châu Triệu Vỹ

**Trường Đại học Công nghệ Sài Gòn (STU)**

---

## Bản quyền

Dự án được phát triển phục vụ mục đích học tập, nghiên cứu và thực hiện báo cáo Thực tập tốt nghiệp tại Trường Đại học Công nghệ Sài Gòn.
