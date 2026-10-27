# Báo cáo kiểm thử

## Thông tin chung

- **Dự án:** Portfolio CV cá nhân
- **Phiên bản:** v1.0
- **Ngày kiểm thử:** 2026-10-27
- **Phạm vi:** Kiểm tra thủ công trang tĩnh `index.html` và `assets/css/styles.css` trên trình duyệt Chromium nhúng; không kiểm thử backend hoặc triển khai production.
- **Kết quả tổng quan:** Trang hiển thị được và các nội dung chính hoạt động ở kích thước màn hình rộng và mobile. Còn tồn tại lỗi ngữ nghĩa ở phần điều hướng, liên kết mẫu và các hạng mục chưa được kiểm thử tự động.

## Minh chứng hình ảnh

Ảnh được chụp trực tiếp từ trang đang chạy trong trình duyệt và lưu trong `docs/screenshots/`.

- [Giao diện màn hình rộng](screenshots/portfolio-desktop.png)
- [Giao diện mobile (390 × 844)](screenshots/portfolio-mobile.png)

## Kết quả theo tiêu chí

### 1. Tính đúng đắn — Đạt một phần

- Trang mở được, hiển thị tiêu đề và các phần Giới thiệu, Kỹ năng, Dự án, Liên hệ.
- Có 4 thẻ dự án và 5 ảnh; tất cả ảnh tải thành công và đều có văn bản `alt`.
- Các liên kết điều hướng nội bộ có đích tương ứng trong trang.
- **Lỗi cần lưu ý:** danh sách điều hướng không nằm trong phần tử `<nav>` dù có thẻ đóng `</nav>`. Trình duyệt vẫn hiển thị danh sách, nhưng không cung cấp landmark điều hướng đúng ngữ nghĩa cho công nghệ hỗ trợ.

### 2. UI/UX — Đạt một phần

- Giao diện được kiểm tra trực quan ở màn hình rộng và mobile; nội dung, ảnh và các thẻ dự án hiển thị theo bố cục thích ứng.
- Ở mobile, các thẻ dự án xếp thành một cột và nội dung có thể cuộn dọc.
- Chưa thực hiện kiểm thử người dùng, đo độ tương phản màu theo WCAG hoặc kiểm tra bằng trình đọc màn hình. Lỗi thiếu landmark `<nav>` cũng ảnh hưởng khả năng tiếp cận.

### 3. Khả năng vận hành - xử lý lỗi — Đạt một phần

- Trang tĩnh mở trực tiếp bằng trình duyệt; các ảnh và nội dung CSS tải được trong lần kiểm tra.
- Trang không có backend, biểu mẫu gửi dữ liệu hoặc logic JavaScript cần kiểm thử luồng lỗi.
- Chưa kiểm tra tình huống máy chủ production, tài nguyên bị thiếu khi triển khai hoặc thông báo lỗi cho người dùng.

### 4. Bảo mật — Đạt một phần

- Trong phạm vi mã nguồn được kiểm tra, đây là trang tĩnh và không thấy mã JavaScript, biểu mẫu nhập liệu, thông tin xác thực hoặc kết nối API đang hoạt động.
- Chưa chạy công cụ quét lỗ hổng, kiểm thử cấu hình máy chủ, HTTPS hay security headers; kết quả này không thay thế đánh giá bảo mật chuyên sâu.
- Email và liên kết GitHub/LinkedIn là dữ liệu mẫu; các liên kết mạng xã hội và “Xem chi tiết” hiện dùng `href="#"`, cần cập nhật trước khi phát hành công khai.

### 5. Chất lượng mã nguồn — Cần cải thiện

- Cấu trúc dự án đơn giản, dùng HTML/CSS thuần, không cần dependency hoặc bước build.
- Phần điều hướng có thẻ `<nav>` đóng nhưng thiếu thẻ mở; cần sửa để bảo toàn cấu trúc HTML và landmark truy cập.
- Chưa có bộ kiểm thử tự động, kiểm tra HTML/CSS hoặc quy trình CI được xác minh trong lần kiểm thử này.

### 6. Khả năng triển khai — Đạt một phần

- Có thể phục vụ như website tĩnh; README mô tả cách chạy bằng máy chủ Python và tùy chọn Docker/Nginx.
- Chưa xác minh triển khai thực tế lên hosting, cấu hình tên miền/HTTPS, Docker image hoặc quy trình CI/CD.
- Trước khi phát hành, cần thay thông tin liên hệ mẫu và các liên kết `#` bằng địa chỉ thật.

## Phạm vi chưa kiểm thử

- Kiểm tra tự động và xác thực HTML/CSS theo chuẩn.
- Khả năng tương thích trên nhiều trình duyệt, thiết bị và trình đọc màn hình.
- Hiệu năng tải, SEO thực tế, bảo mật máy chủ và triển khai production.
