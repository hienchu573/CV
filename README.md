# Portfolio CV - Chu Thị Hiền

## Tên dự án

**Portfolio CV cá nhân của Chu Thị Hiền** - trang giới thiệu năng lực và các dự án Frontend.

## Mô tả

Website tĩnh giới thiệu cá nhân, kỹ năng, dự án tiêu biểu và thông tin liên hệ. Giao diện được thiết kế responsive để sử dụng trên điện thoại, máy tính bảng và máy tính. Dự án không có backend, không cần cơ sở dữ liệu và không cần cài thư viện.

## Chức năng

- Hiển thị phần giới thiệu và vai trò Frontend Developer.
- Điều hướng đến các mục Giới thiệu, Kỹ năng, Dự án và Liên hệ.
- Trình bày danh sách kỹ năng và các dự án mẫu.
- Hiển thị email, GitHub và LinkedIn.
- Bố cục thích ứng với kích thước màn hình khác nhau.

Các dự án Todo List, thời tiết và blog trên trang hiện là nội dung giới thiệu trong portfolio, không phải các ứng dụng độc lập có thể chạy từ website này.

## Công nghệ

- HTML5: cấu trúc nội dung và các vùng điều hướng.
- CSS3: giao diện responsive, Flexbox, CSS Grid và hiệu ứng trình bày.
- Docker/Nginx: tùy chọn để phục vụ website tĩnh trong container.

Trang hiện không sử dụng JavaScript, framework frontend hay công cụ build.

## Yêu cầu môi trường

- Windows, macOS hoặc Linux.
- Trình duyệt hiện đại như Chrome, Firefox, Edge hoặc Safari.
- Để chạy máy chủ cục bộ: Python 3 (hoặc có thể mở trực tiếp `index.html`).
- Để chạy bằng container: Docker Engine hoặc Docker Desktop đang hoạt động.
- Git chỉ cần thiết nếu tải mã nguồn bằng Git.

## Cài đặt

Tải mã nguồn về máy bằng một trong hai cách:

1. Tải ZIP của dự án và giải nén.
2. Clone repository (thay URL mẫu bằng URL repository thực tế):

```bash
git clone <URL_REPOSITORY>
cd CV-main
```

Không cần cài package hay chạy lệnh build. Đảm bảo giữ nguyên cấu trúc `index.html` và thư mục `assets/`.

## Cấu hình nội dung

Mở `index.html` và cập nhật các thông tin cá nhân, bao gồm tên, mô tả, dự án, email và liên kết GitHub/LinkedIn. Email và các URL liên hệ trong mã nguồn hiện là thông tin mẫu; hãy thay bằng thông tin thật trước khi xuất bản.

Để thay ảnh đại diện, thay `assets/img/avata.jpg` bằng ảnh của bạn hoặc cập nhật đường dẫn ảnh trong `index.html`. Chỉnh màu sắc, bố cục và breakpoint trong `assets/css/styles.css`.

Không cần tạo file `.env` hoặc cấu hình API cho phiên bản hiện tại.

## Chạy thử

### Windows

Mở PowerShell tại thư mục dự án và chạy:

```powershell
py -m http.server 8000
```

Nếu lệnh `py` không có, thử `python -m http.server 8000`. Mở [http://localhost:8000](http://localhost:8000) trong trình duyệt. Dừng máy chủ bằng `Ctrl+C`.

### macOS

Mở Terminal, chuyển đến thư mục dự án rồi chạy:

```bash
python3 -m http.server 8000
```

Mở [http://localhost:8000](http://localhost:8000). Dừng máy chủ bằng `Ctrl+C`.

### Linux

Mở Terminal, chuyển đến thư mục dự án rồi chạy:

```bash
python3 -m http.server 8000
```

Mở [http://localhost:8000](http://localhost:8000). Dừng máy chủ bằng `Ctrl+C`.

Trên cả ba hệ điều hành, có thể mở trực tiếp `index.html` bằng trình duyệt để xem trang mà không cần máy chủ cục bộ.

### Docker

Cần cài và khởi động Docker trước. Lệnh bên dưới dùng Nginx để phục vụ thư mục dự án ở cổng `8080`, không cần Dockerfile.

**Windows PowerShell** (chạy tại thư mục dự án):

```powershell
docker run --rm --name cv-portfolio -p 8080:80 --mount "type=bind,source=$($PWD.Path),target=/usr/share/nginx/html,readonly" nginx:alpine
```

**macOS/Linux** (chạy tại thư mục dự án):

```bash
docker run --rm --name cv-portfolio -p 8080:80 --mount "type=bind,source=$(pwd),target=/usr/share/nginx/html,readonly" nginx:alpine
```

Mở [http://localhost:8080](http://localhost:8080). Nhấn `Ctrl+C` để dừng và xóa container.

## Thông tin liên hệ

- **Tên:** Chu Thị Hiền
- **Email:** `hien.chu@example.com` (địa chỉ mẫu, cần cập nhật trước khi sử dụng)
- **GitHub:** [github.com/chuthihien](https://github.com/chuthihien) (liên kết mẫu)
- **LinkedIn:** [linkedin.com/in/chuthihien](https://linkedin.com/in/chuthihien) (liên kết mẫu)
