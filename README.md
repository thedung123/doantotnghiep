# 👟 Website Bán Giày Dép – Thanh Toán PayPal (Laravel Project)

Dự án là một hệ thống Thương mại điện tử án giày dép (E-Commerce Web Application) 

---

## 📖 1. Giới thiệu dự án
Hệ thống được thiết kế tối ưu hóa quy trình kinh doanh trực tuyến và nâng cao trải nghiệm mua sắm.
* **Mục tiêu:** Tạo kênh bán hàng trực tuyến mượt mà, tăng tỷ lệ chuyển đổi và cung cấp công cụ thống kê trực quan cho chủ shop.
* **Đối tượng sử dụng:**
    * **Khách hàng (Customer):
    * **Quản trị viên (Admin/Staff)

---

## ⚙️ 2. Công nghệ sử dụng
### **Back-end**
* **Ngôn ngữ:** PHP 7.x
* **Framework:** Laravel 
* **Database:** MySQL


### **Front-end**
* **Nền tảng:** HTML5, CSS3, JavaScript.
* **Framework:** Bootstrap  
* **Thư viện:** 

### **Kỹ thuật đặc biệt**

* **AJAX:** Cập nhật giỏ hàng/yêu thích không tải lại trang.
* **Data Visualization:** Chart.js

---

## 📥 3. Hướng dẫn cài đặt
### **Bước 1: Import Database**
1. Truy cập `localhost/phpmyadmin`.
2. Tạo database mới tên là: **Giay**
3. Chọn tab **Import** -> Chọn file `.sql` kèm theo -> Nhấn **Go**.

### **Bước 2: Cấu hình .env**
1. Sao chép file `.env.example` thành `.env`.
2. Cấu hình thông tin Database:
   ```env
   DB_DATABASE=Giay
   DB_USERNAME=root
   DB_PASSWORD=
### **Bước 3: Chạy lệnh hệ thống**
Mở Terminal tại thư mục dự án và chạy:

Bash
1. composer install
2. php artisan key:generate
3. php artisan serveserve
### **Bước 4: Truy cập**
Website: http://127.0.0.1:8000

Admin: Thêm /admin vào sau đường dẫn (ví dụ: http://127.0.0.1:8000/admin).

⭐ 4. Các chức năng chính
Phía Khách Hàng
Tài khoản: Đăng ký, Đăng nhập, Đổi mật khẩu, Quản lý hồ sơ.

Mua sắm: Tìm kiếm (Full-text search), So sánh giá, Giỏ hàng, Yêu thích (Wishlist).

Thanh toán: Đặt hàng và tích hợp thanh toán qua PayPal.

Tương tác: Đánh giá sản phẩm sau khi mua, xem lịch sử mua hàng.

Phía Admin
Quản lý hàng hóa: Danh mục, Sản phẩm (thêm ảnh, khóa/mở bán).

Marketing: Quản lý mã giảm giá (Coupon), Quản lý Banner quảng cáo.

Vận hành: Quản lý khách hàng/nhân viên, Duyệt đơn hàng, In hóa đơn.

Báo cáo (Dashboard): Thống kê doanh thu (biểu đồ cột), Thống kê danh mục (biểu đồ tròn), Theo dõi người dùng online.

Dữ liệu: Xuất báo cáo ra file Excel.

📂 5. Cấu trúc thư mục chính
app/: Chứa Models, Controllers, Middleware (Logic chính).

database/: Chứa Migrations, Seeders (Cấu trúc DB).

public/: Chứa các file tĩnh (CSS, JS, Images) và file index.php.

resources/views/: Giao diện Blade template.

routes/: Định nghĩa các đường dẫn (web.php, api.php).

.env: Cấu hình môi trường.

🔄 6. Mô hình hoạt động (MVC)
Dự án tuân thủ nghiêm ngặt mô hình Model - View - Controller:

Model: Tương tác và xử lý dữ liệu từ MySQL.

View: Hiển thị giao diện người dùng qua Blade engine.

Controller: Tiếp nhận yêu cầu, xử lý logic và điều phối dữ liệu.

Luồng chạy hệ thống:
Browser ➔ Routing ➔ Middleware ➔ Controller ➔ Model ➔ View ➔ Browser (HTML)
