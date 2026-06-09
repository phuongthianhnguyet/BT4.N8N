# BT4.N8N

<p align="center">

![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge\&logo=docker\&logoColor=white)
![N8N](https://img.shields.io/badge/n8n-EA4B71?style=for-the-badge\&logo=n8n\&logoColor=white)
![WordPress](https://img.shields.io/badge/WordPress-21759B?style=for-the-badge\&logo=wordpress\&logoColor=white)
![Telegram](https://img.shields.io/badge/Telegram-26A5E4?style=for-the-badge\&logo=telegram\&logoColor=white)
![Gemini](https://img.shields.io/badge/Google_Gemini-8E75FF?style=for-the-badge\&logo=google-gemini\&logoColor=white)

</p>

---

> [!NOTE]
> **Mục tiêu bài tập:** Triển khai hệ thống WordPress bằng Docker, tích hợp N8N, Telegram Bot và Google Gemini AI để tự động hóa quá trình tạo và đăng bài lên website.

# 📑 Mục lục

* [Khởi chạy tất cả services ở chế độ nền](#-khởi-chạy-tất-cả-services-ở-chế-độ-nền)
* [Kiểm tra trạng thái các service](#-kiểm-tra-trạng-thái-các-service)
* [Thêm Tunnel cho n8n và php](#-thêm-tunnel-cho-n8n-và-php)
* [Cài đặt Wordpress](#-cài-đặt-wordpress-đã-làm-ở-bài-tập-3)

  * [Trang admin](#1-trang-admin---wordpress)
  * [Trang phpmyadmin](#2-trang-phpmyadmin)
  * [Tạo 2 bài viết thủ công](#3-tạo-2-bài-viết-thủ-công-trong-wordpress)
* [Cấu hình N8N](#-cấu-hình-n8n)

  * [Tạo tài khoản và Activate License](#bước-1-tạo-tài-khoản-và-activate-license)
  * [Tạo Telegram Bot](#bước-2-tạo-telegram-bot)
  * [Lấy API KEY](#bước-3--lấy-api-key)
* [Chỉnh sửa Workflow](#-chỉnh-sửa-workflow)
* [Đăng bài](#-đăng-bài)
* [Nhận xét](#-nhận-xét)
* [Khó khăn và Quá trình khắc phục](#-khó-khăn-và-quá-trình-khắc-phục)
* [Bài học và Kiến thức tích lũy](#-bài-học-và-kiến-thức-tích-lũy)

---

# 🚀 Khởi chạy tất cả services ở chế độ nền

```bash
docker compose up -d
```

# 📋 Kiểm tra trạng thái các service

```bash
docker compose ps
```

<img width="1898" height="330" alt="image" src="https://github.com/user-attachments/assets/315eac40-48b0-4cc9-ba54-9eb51ce5a5a6" />

<img width="1900" height="671" alt="image" src="https://github.com/user-attachments/assets/9b6b46ff-9690-4a44-bdeb-7f96cfe81dbf" />

---

# 🌐 Thêm Tunnel cho n8n và php

## Kết quả

<img width="1917" height="955" alt="image" src="https://github.com/user-attachments/assets/c542864d-edbb-4765-8d0a-8c18cf4ee661" />

---

# 📝 Cài đặt Wordpress (đã làm ở bài tập 3)

## 1. Trang admin - WordPress

<img width="1920" height="1024" alt="image" src="https://github.com/user-attachments/assets/731dabac-cadc-489d-9293-350cebaf2c82" />

## 2. Trang phpmyadmin

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/190f4648-7f16-41e0-8e41-401b20c56f39" />

## 3. Tạo 2 bài viết thủ công trong WordPress

Sau khi cài đặt WordPress thàng công, tiến hành tạo nội dung bằng cách sử dụng Custom HTML Block trong trình soạn thảo.

### Cách sử dụng Custom HTML Block

* Truy cập trang quản trị WordPress.
* Chọn Post -> Add New Post để tạo post
* Trong trình chỉnh sửa:

  * Nhấn dấu "+"
  * Tìm kiếm Custom HTML
  * Chọn block Custom HTML
  * Nhập mã HTML trực tiếp vào block
  * Có thể nhấn Preview để xem trước nội dung hiển thị
  * Nhấn Publish để xuất bản

<img width="1920" height="1062" alt="image" src="https://github.com/user-attachments/assets/0de049d5-4f66-40ac-bab6-456102f4366e" />

---

### Trang 1. Giới thiệu bản thân

Tạo 1 page với tiêu đề:

**Giới thiệu bản thân**

<img width="1920" height="911" alt="image" src="https://github.com/user-attachments/assets/4e909846-773e-42d6-859e-cc556758d763" />

<img width="1915" height="880" alt="image" src="https://github.com/user-attachments/assets/aa786582-cbf1-4915-bdce-c19676ec0d39" />

---

### Trang 2. Tạo bài viết giới thiệu về kiến thức em đã học được ở môn Phát triển ứng dụng với mã nguồn mở

<img width="1920" height="897" alt="image" src="https://github.com/user-attachments/assets/7c7caf59-a85f-4b30-a7e4-e47779940d7e" />

<img width="1919" height="891" alt="image" src="https://github.com/user-attachments/assets/c03e3721-5e21-4e98-9908-9e308b5fb7cb" />

<img width="1919" height="900" alt="image" src="https://github.com/user-attachments/assets/252f9ae7-3bce-4a6c-8fc7-130f77de86d6" />

---

# ⚙️ Cấu hình N8N

## Bước 1 Tạo tài khoản và Activate License

### Tạo tài khoản admin

* Truy cập: https://n8n.phuonganhnguyet.id.vn
* Điền đủ thông tin

<img width="1917" height="976" alt="image" src="https://github.com/user-attachments/assets/7f76aa5b-728e-4bf3-b13d-42ea6031f19f" />

* Chọn Send me a License key -> điền thông tin -> Submit
* Tạo tài khoản thành công

<img width="1907" height="952" alt="image" src="https://github.com/user-attachments/assets/9e544153-1b3b-4a0f-81b5-fce9b0618de3" />

* Kiểm tra email để lấy License Key

<img width="1920" height="897" alt="image" src="https://github.com/user-attachments/assets/9c792d36-4ef3-45de-a9eb-b194569fd447" />

### Activate License

Setting -> Usage and Plan -> Enter activation key -> Paste key -> activate

Thông báo thành công:

> "Your Registered Community Edition has been successfully activated."

<img width="1902" height="989" alt="image" src="https://github.com/user-attachments/assets/13501297-bcd8-4d9c-bbc8-166c82c0280b" />

---

## Bước 2 Tạo Telegram Bot

> [!TIP]
> Token Telegram Bot là thông tin nhạy cảm, không nên đưa lên repository công khai.

* Mở Telegram → tìm kiếm @BotFather → bắt đầu chat
* Gõ lệnh /newbot
* Đặt tên bot (vd: Bot_Wordpress)
* Đặt username bot (phải kết thúc bằng bot, vd: anhnguyet_wp_bot)
* Copy Token được cấp (dạng: 1234567890:AAxxxxxxxxxxxxxx)

<img width="1470" height="960" alt="image" src="https://github.com/user-attachments/assets/c61cf07c-52e5-44c3-ad2e-54978e7d7300" />

* Bot vừa tạo

<img width="1919" height="900" alt="image" src="https://github.com/user-attachments/assets/ade55642-da30-4e84-a88a-3c02b7679454" />

<img width="1915" height="884" alt="image" src="https://github.com/user-attachments/assets/e8537bb3-cec2-45a3-94d2-268cdbe4231e" />

---

## Bước 3 – Lấy API KEY

> [!IMPORTANT]
> API Key chỉ hiển thị một lần. Cần lưu trữ cẩn thận ngay sau khi tạo.

* Truy cập https://aistudio.google.com => https://aistudio.google.com/api-keys
* Đăng nhập / Đăng ký tài khoản
* Vào API Keys → Create new API key
* Copy API Key (chỉ hiển thị một lần)

<img width="1916" height="906" alt="image" src="https://github.com/user-attachments/assets/0ce37b8d-ef46-46d8-b243-08875c6031dd" />

<img width="1920" height="859" alt="image" src="https://github.com/user-attachments/assets/19c97af3-c782-49bc-a0a4-6230e7d302a8" />

---

# 🔄 Chỉnh sửa Workflow

<img width="1919" height="942" alt="image" src="https://github.com/user-attachments/assets/5b50d256-355b-44b0-82a4-79e9e79c7dc3" />

<img width="1920" height="957" alt="image" src="https://github.com/user-attachments/assets/46966031-5505-46b0-95dd-cf0bcf01be45" />

<img width="1920" height="1024" alt="image" src="https://github.com/user-attachments/assets/d535b6ac-ea21-417c-8b11-3527e64026db" />

<img width="1919" height="970" alt="image" src="https://github.com/user-attachments/assets/1ffa95a5-59ac-4ad3-badc-85575502aa47" />

<img width="1917" height="1073" alt="image" src="https://github.com/user-attachments/assets/8ffd241a-2964-4489-9b18-405938edd0cd" />

---

# 📤 Đăng bài

* Gửi nội dung trang muốn tạo

<img width="1242" height="2688" alt="image" src="https://github.com/user-attachments/assets/3ee5483e-eed8-4e10-8357-9d8575763fb5" />

* Trên trang Wordpress

<img width="1919" height="908" alt="image" src="https://github.com/user-attachments/assets/a80cd1eb-5039-41b2-9857-7b3254cc3616" />

---

# 📊 Nhận xét

## Kết quả đã đạt

> [!SUCCESS]
> Hệ thống đã được triển khai thành công và hoạt động ổn định.

* Xây dựng thành công hệ thống tự động hóa: Thiết lập hoàn chỉnh một quy trình vận hành khép kín (workflow) từ khâu tiếp nhận thông tin, xử lý dữ liệu bằng trí tuệ nhân tạo (AI) cho đến khâu tự động xuất bản thành phẩm lên nền tảng website.

* Tối ưu hóa quy trình vận hành: Hệ thống hiện tại đã đạt được sự ổn định cao, loại bỏ hoàn toàn các bước thao tác thủ công. Luồng dữ liệu giữa các nền tảng trung gian được kết nối đồng bộ và phản hồi theo thời gian thực (realtime).

---

## Khó khăn và Quá trình khắc phục

> [!WARNING]
> Trong quá trình triển khai đã gặp nhiều vấn đề liên quan đến hạ tầng mạng và xác thực dịch vụ.

* Sự cố kết nối hệ thống: Trong giai đoạn đầu cấu hình, dự án gặp một số trở ngại liên quan đến việc thiết lập đường dẫn, phân giải tên miền (domain) và cấu hình mạng khiến các nền tảng chưa thể giao tiếp được với nhau.

* Lỗi xác thực và phân quyền API: Quá trình tích hợp các dịch vụ bên thứ ba (AI và nền tảng Web) ban đầu bị từ chối do mã khóa bảo mật (API Key) chưa hợp lệ hoặc cơ chế phân quyền tài khoản (Authentication) chưa được thiết lập đúng cách.

---

## Bài học và Kiến thức tích lũy

> [!NOTE]
> Đây là những kiến thức và kinh nghiệm thực tế thu được sau khi hoàn thành bài tập.

* Tư duy tự động hóa quy trình (Automation): Hiểu rõ cách thức thiết kế, xây dựng và quản lý một luồng công việc tự động; biết cách liên kết nhiều công cụ độc lập thành một hệ sinh thái thống nhất.

* Kỹ năng làm việc với API và Webhook: Nắm vững cơ chế truyền tải dữ liệu giữa các ứng dụng, cách quản lý mã xác thực bảo mật và cách bắt các sự kiện tự động trong môi trường mạng.

* Khai thác và ứng dụng Trí tuệ nhân tạo: Tích lũy được kinh nghiệm thực tế trong việc ứng dụng Generative AI vào công việc thay vì chỉ tra cứu thông thường, biết cách định hình dữ liệu đầu ra của AI để phục vụ cho các bài toán kỹ thuật thực tế.

---

<p align="center">
<b>Hoàn thành bài tập BT4.N8N</b><br>
Docker • WordPress • N8N • Telegram Bot • Google Gemini AI
</p>
