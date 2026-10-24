# THIỆP MỜI TỐT NGHIỆP HUTECH 🎓

**Tác giả:** Trần Bảo Duy  
**Website cá nhân:** [https://tranbaoduy.netlify.app/](https://tranbaoduy.netlify.app/)  
**Năm thực hiện:** 2026

## 1. Giới thiệu dự án

**THIỆP MỜI TỐT NGHIỆP HUTECH** là dự án thiệp mời tốt nghiệp trực tuyến, được xây dựng nhằm giúp người dùng gửi lời mời tham dự lễ tốt nghiệp theo cách hiện đại, trực quan và dễ chia sẻ.

Dự án kết hợp giao diện thiệp mời, hiệu ứng mở thiệp, âm thanh và chức năng quản lý khách mời, góp phần tạo nên trải nghiệm đáng nhớ cho người tham dự.

## 2. Chức năng chính

- **Thiệp mời trực tuyến:** Hiển thị thông tin và giao diện thiệp mời tốt nghiệp.
- **Hiệu ứng mở thiệp:** Tạo trải nghiệm mở thiệp sinh động.
- **Âm thanh:** Phát nhạc khi người dùng mở thiệp, hỗ trợ hiệu ứng tăng và giảm âm lượng.
- **Thông tin khách mời:** Hiển thị tên và các thông tin liên quan đến buổi lễ.
- **Lời chúc:** Lưu trữ và hiển thị lời chúc của khách mời.
- **Trang quản trị:** Quản lý danh sách khách mời và thông tin liên quan.
- **Memory Album:** Tạo album lưu giữ tên khách mời và những lời chúc đáng nhớ.
- **Xuất hình ảnh:** Hỗ trợ tạo hình ảnh thiệp hoặc album để chia sẻ trên mạng xã hội.

*Các chức năng liên quan đến cơ sở dữ liệu phụ thuộc vào cấu hình và quyền truy cập của hệ thống.*

## 3. Công nghệ sử dụng

- **HTML5:** Xây dựng cấu trúc trang web.
- **CSS3:** Thiết kế giao diện, bố cục và hiệu ứng.
- **JavaScript:** Xử lý tương tác và các chức năng của ứng dụng.
- **Supabase:** Hỗ trợ cơ sở dữ liệu và lưu trữ thông tin nếu được cấu hình.
- **Google Fonts và phông chữ tùy chỉnh:** Phục vụ thiết kế giao diện và nội dung thiệp.

## 4. Cấu trúc dự án

```text
THIEPMOI/
├── index.html       # Trang giới thiệu và mở thiệp
├── thiep.html       # Giao diện thiệp mời
├── admin.html       # Trang quản trị khách mời và album
├── guest-db.js      # Xử lý dữ liệu khách mời (nếu có)
└── assets/
    └── fonts/       # Các phông chữ sử dụng trong dự án
```

*Cấu trúc trên mô tả các tệp chính; thư mục thực tế có thể chứa thêm hình ảnh, tài nguyên và tệp cấu hình.*

## 5. Hướng dẫn sử dụng

### Chạy dự án trên máy tính

1. Tải hoặc sao chép mã nguồn dự án về máy tính.
2. Mở thư mục dự án.
3. Mở `index.html` bằng trình duyệt để xem trang thiệp mời.
4. Truy cập `thiep.html` để xem giao diện thiệp.
5. Mở `admin.html` để sử dụng trang quản trị nếu đã được cấu hình quyền truy cập.

### Triển khai trực tuyến

Có thể triển khai dự án trên các nền tảng lưu trữ trang web tĩnh như Netlify hoặc GitHub Pages.

Nếu sử dụng Supabase, cần cấu hình thông tin kết nối, quyền truy cập và chính sách bảo mật phù hợp trước khi đưa dự án vào sử dụng.

## 6. Lưu ý

- Không công khai khóa bí mật hoặc thông tin xác thực của hệ thống.
- Kiểm tra các chức năng trên cả máy tính và điện thoại.
- Đảm bảo quyền truy cập cơ sở dữ liệu được thiết lập đúng.
- Kiểm tra đường dẫn hình ảnh, âm thanh và phông chữ trước khi triển khai.

## 7. Tác giả

**Trần Bảo Duy**

Website cá nhân: [tranbaoduy.netlify.app](https://tranbaoduy.netlify.app/)

---

© 2026 Trần Bảo Duy. Bản quyền thuộc về tác giả.
