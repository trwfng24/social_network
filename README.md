# 🌐 Dự Án Mạng Xã Hội Django

## 📖 Giới thiệu

Đây là một dự án mạng xã hội được xây dựng bằng Django, cung cấp các tính năng cơ bản của một nền tảng mạng xã hội như đăng bài, nhắn tin realtime, tìm kiếm bạn bè, và quản lý hồ sơ cá nhân.

## ✨ Tính năng chính

- **Trang chủ**: Hiển thị các bài đăng và tương tác từ người dùng
- **Nhắn tin realtime**: Chat trực tiếp giữa các người dùng sử dụng WebSocket
- **Tìm kiếm bạn bè**: Tìm kiếm và kết nối với người dùng khác
- **Đăng nhập/Đăng ký**: Hệ thống xác thực người dùng
- **Hồ sơ cá nhân**: Quản lý thông tin cá nhân và bài đăng
- **Bình luận**: Tương tác với bài đăng thông qua hệ thống bình luận

## 🛠️ Công nghệ sử dụng

- **Backend**: Django 4.x
- **Database**: SQLite3 (có thể cấu hình PostgreSQL/MySQL cho production)
- **Frontend**: HTML, CSS, JavaScript
- **Realtime**: Django Channels cho WebSocket
- **Authentication**: Django's built-in authentication system

## 📁 Cấu trúc dự án

```
myproject/
├── home/                 # Ứng dụng chính (trang chủ, bài đăng, bình luận)
├── realtime/             # Ứng dụng chat realtime
├── myproject/            # Cấu hình Django chính
├── static/               # Static files (CSS, JS)
├── Templates/            # HTML templates
├── media/                # Media files (avatars, posts, comments)
├── db.sqlite3            # Database SQLite
└── manage.py             # Django management script
```

## 🚀 Cài đặt và chạy

### Yêu cầu hệ thống

- Python 3.8+
- Django 4.x
- Git

### Các bước cài đặt

1. **Clone repository:**

   ```bash
   git clone https://github.com/trwfg24/social_network.git
   cd SocialNetwork_Django
   ```

2. **Tạo virtual environment:**

   ```bash
   python -m venv venv
   source venv/bin/activate  # Trên Windows: venv\Scripts\activate
   ```

3. **Cài đặt dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

4. **Chạy migrations:**

   ```bash
   python manage.py migrate
   ```

5. **Tạo superuser (tùy chọn):**

   ```bash
   python manage.py createsuperuser
   ```

6. **Chạy server:**

   ```bash
   python manage.py runserver
   ```

7. **Truy cập ứng dụng:**
   Mở trình duyệt và truy cập: `http://127.0.0.1:8000`

## 🔧 Cấu hình

### Database

Mặc định sử dụng SQLite. Để sử dụng database khác, chỉnh sửa `myproject/settings.py`:

```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',  # hoặc mysql
        'NAME': 'your_db_name',
        'USER': 'your_db_user',
        'PASSWORD': 'your_db_password',
        'HOST': 'localhost',
        'PORT': '5432',
    }
}
```

### Static Files

Trong production, cấu hình static files:

```bash
python manage.py collectstatic
```

## 📝 Sử dụng

1. **Đăng ký tài khoản** hoặc đăng nhập nếu đã có
2. **Tạo bài đăng** trên trang chủ
3. **Tìm kiếm bạn bè** và kết nối
4. **Chat realtime** với bạn bè
5. **Quản lý hồ sơ** cá nhân

## 🎥 Demo

![Trang chủ](img/FireShot%20Capture%20024%20-%20Younity%20-%20Kết%20nối%20mọi%20lúc%20-%20[127.0.0.1].png)

![Chat](img/Screenshot%202025-10-27%20122823.png)

## 🤝 Đóng góp

1. Fork dự án
2. Tạo branch mới (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Tạo Pull Request

## 👥 Tác giả

- **Tên tác giả**: Trường Nguyễn
- **Email**: [truongnc1602@gmail.com]

