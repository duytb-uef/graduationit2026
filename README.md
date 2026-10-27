# THIỆP MỜI TỐT NGHIỆP HUTECH 2026

Website thiệp mời tốt nghiệp trực tuyến của **Trần Bảo Duy**, được xây dựng để giới thiệu thông tin buổi lễ, cho phép khách mời xác nhận tham dự và gửi lời chúc, đồng thời hỗ trợ quản lý dữ liệu khách mời và tạo Memory Album.

- **Tác giả:** Trần Bảo Duy
- **Website cá nhân:** https://tranbaoduy.netlify.app/
- **Năm:** 2026
- **Ngôn ngữ giao diện:** Tiếng Việt

---

## 1. Tổng quan

Dự án là website tĩnh gồm các trang HTML, CSS và JavaScript. Giao diện được thiết kế theo phong cách lễ tốt nghiệp với tông màu vàng gold, hiệu ứng chuyển động, phông chữ tùy chỉnh và âm thanh.

Các chức năng lưu trữ dữ liệu sử dụng **Supabase**. Khả năng đọc hoặc cập nhật dữ liệu phụ thuộc vào cấu hình kết nối và chính sách quyền truy cập của dự án Supabase.

## 2. Chức năng chính

### Trang mở đầu — `index.html`

- Giới thiệu thiệp mời tốt nghiệp HUTECH 2026.
- Hiển thị hiệu ứng nền và các hiệu ứng chuyển động.
- Hiển thị thông tin thời gian sự kiện được cấu hình trong mã nguồn.
- Có luồng mở thiệp và phát âm thanh theo tương tác của người dùng.
- Có cơ chế ghi nhớ trạng thái/tên khách trên trình duyệt để hỗ trợ lời chào khi quay lại, tùy trạng thái đã lưu.

### Trang thiệp mời — `thiep.html`

- Hiển thị nội dung và thiết kế thiệp mời.
- Hỗ trợ khách nhập tên và xác nhận thông tin tham dự.
- Cung cấp khu vực gửi lời chúc.
- Sử dụng JavaScript để xử lý tương tác và kết nối chức năng dữ liệu.
- Có các hiệu ứng giao diện và tài nguyên hình ảnh, phông chữ, âm thanh.

### Trang quản trị — `admin.html`

- Phục vụ việc xem và quản lý dữ liệu khách mời/lời chúc theo các chức năng đã triển khai.
- Có các chức năng tạo hình ảnh phục vụ chia sẻ.
- Hỗ trợ tạo **Memory Album** để lưu giữ lời chúc và kỷ niệm tốt nghiệp.

> Lưu ý: Việc một chức năng hoạt động đầy đủ phụ thuộc vào mã nguồn hiện tại, tài nguyên đi kèm và cấu hình Supabase. Cần kiểm thử trên môi trường thực tế trước khi sử dụng chính thức.

## 3. Công nghệ và thư viện

| Công nghệ / thư viện | Vai trò |
| --- | --- |
| HTML5 | Cấu trúc các trang web |
| CSS3 | Giao diện, bố cục, hiệu ứng và khả năng thích ứng màn hình |
| JavaScript | Xử lý tương tác, trạng thái khách và các chức năng của trang |
| Supabase JavaScript SDK | Kết nối dịch vụ cơ sở dữ liệu Supabase |
| Google Fonts và phông chữ cục bộ | Hiển thị kiểu chữ cho giao diện |
| QRCode.js | Hỗ trợ tạo mã QR tại các khu vực sử dụng thư viện |
| html2canvas | Hỗ trợ kết xuất giao diện thành hình ảnh |

Các thư viện bên ngoài có thể được tải qua CDN nên môi trường chạy cần có kết nối Internet để tải những tài nguyên đó.

## 4. Cấu trúc thư mục

Các tệp chính của dự án:

```text
THIEPMOI/
├── index.html             # Trang mở đầu
├── thiep.html             # Trang thiệp mời
├── admin.html             # Trang quản trị và Memory Album
├── guest-db.js            # Các hàm làm việc với dữ liệu khách mời
├── supabase-schema.sql    # SQL tạo/cấu hình cấu trúc dữ liệu và chính sách truy cập
├── README.md              # Tài liệu dự án
├── assets/
│   └── fonts/             # Phông chữ tùy chỉnh
├── images/                # Tài nguyên hình ảnh
├── music/
│   └── background.mp4     # Tài nguyên âm thanh/video nền
└── .git/                  # Dữ liệu quản lý phiên bản Git (nếu có)
```

Thư mục thực tế có thể có thêm tệp hoặc tài nguyên khác. Không xóa hay đổi tên tài nguyên đang được tham chiếu trong HTML/CSS/JavaScript nếu chưa cập nhật các đường dẫn tương ứng.

## 5. Cách chạy dự án trên Windows

### Cách 1: Chạy bằng máy chủ HTTP cục bộ (khuyến nghị)

Nên dùng máy chủ HTTP thay vì chỉ mở trực tiếp tệp HTML bằng đường dẫn `file://`, vì một số chức năng tải tài nguyên, thư viện hoặc kết nối dịch vụ có thể hoạt động khác nhau tùy môi trường.

1. Mở thư mục dự án trong File Explorer:

   `C:\Users\ADMIN\OneDrive\Desktop\THỰC TẬP\THIEPMOI`

2. Mở Terminal hoặc Command Prompt tại thư mục này.
3. Nếu máy đã cài Python, chạy:

   ```powershell
   py -m http.server 8000
   ```

4. Mở trình duyệt và truy cập:

   - Trang mở đầu: http://localhost:8000/index.html
   - Trang thiệp mời: http://localhost:8000/thiep.html
   - Trang quản trị: http://localhost:8000/admin.html

5. Để dừng máy chủ, quay lại cửa sổ Terminal và nhấn `Ctrl + C`.

Nếu lệnh `py` không hoạt động, hãy kiểm tra Python đã được cài đặt và thêm vào PATH hay chưa.

### Cách 2: Mở trực tiếp tệp HTML

Có thể mở `index.html` bằng trình duyệt để xem giao diện cơ bản. Tuy nhiên, nếu gặp lỗi tải tài nguyên, kết nối dữ liệu hoặc chức năng xuất ảnh, hãy thử chạy bằng máy chủ HTTP cục bộ và kiểm tra Console của trình duyệt.

## 6. Cấu hình Supabase

Dự án có hai tệp liên quan trực tiếp đến dữ liệu:

- **`guest-db.js`:** chứa logic kết nối và thao tác dữ liệu khách mời.
- **`supabase-schema.sql`:** mô tả cấu trúc dữ liệu và các chính sách truy cập cơ sở dữ liệu.

Khi thiết lập môi trường Supabase mới:

1. Tạo hoặc chọn dự án Supabase phù hợp.
2. Kiểm tra cấu hình URL dự án và khóa kết nối được sử dụng trong `guest-db.js`.
3. Xem lại `supabase-schema.sql` trước khi chạy SQL; chỉ áp dụng các lệnh phù hợp với môi trường cần triển khai.
4. Kiểm tra bảng, cột, quyền đọc/thêm/cập nhật/xóa và chính sách Row Level Security (RLS).
5. Chạy thử các luồng xác nhận tham dự và gửi lời chúc trên môi trường kiểm thử.
6. Kiểm tra lỗi trong Console trình duyệt và phần Logs của Supabase nếu dữ liệu không được lưu.

**Lưu ý bảo mật:**

- Không đưa khóa `service_role`, mật khẩu hoặc thông tin bí mật vào mã nguồn phía trình duyệt hay kho Git công khai.
- Khóa công khai dùng ở trình duyệt không thay thế cho việc thiết lập RLS và chính sách quyền truy cập đúng cách.
- Không mặc định rằng trang quản trị đã an toàn chỉ vì có giao diện quản trị. Cần xác minh cơ chế xác thực và quyền thao tác dữ liệu thực tế.
- Không chạy SQL thay đổi/xóa dữ liệu trên môi trường đang sử dụng nếu chưa sao lưu và xem xét tác động.

## 7. Kiểm tra trước khi triển khai

Nên kiểm tra tối thiểu các trường hợp sau trên cả máy tính và điện thoại:

- [ ] Trang `index.html` hiển thị đúng, không vỡ bố cục.
- [ ] Nút mở thiệp hoạt động và âm thanh tuân theo tương tác của người dùng.
- [ ] Trang `thiep.html` hiển thị đủ chữ, hình ảnh và phông chữ.
- [ ] Khách có thể nhập tên và thực hiện luồng xác nhận theo thiết kế.
- [ ] Lời chúc hợp lệ được lưu và hiển thị đúng.
- [ ] Xử lý lỗi rõ ràng khi Supabase mất kết nối hoặc từ chối quyền.
- [ ] Trang quản trị hiển thị dữ liệu đúng và chỉ cho phép thao tác theo quyền dự kiến.
- [ ] Chức năng tạo ảnh/Memory Album xuất được ảnh không bị thiếu hình, sai phông hoặc cắt chữ.
- [ ] Các đường dẫn tài nguyên vẫn đúng sau khi triển khai.
- [ ] Kiểm tra Console trình duyệt để phát hiện lỗi JavaScript và lỗi tải tài nguyên.

## 8. Một số lỗi thường gặp

| Hiện tượng | Hướng kiểm tra |
| --- | --- |
| Không lưu được tên hoặc lời chúc | Kiểm tra cấu hình trong `guest-db.js`, quyền bảng, RLS và lỗi trong Console |
| Dữ liệu không xuất hiện ở trang quản trị | Kiểm tra kết nối Supabase, điều kiện truy vấn và quyền đọc |
| Ảnh xuất ra bị thiếu hoặc lỗi | Kiểm tra đường dẫn ảnh, tài nguyên tải từ domain khác, CORS và Console |
| Phông chữ không hiển thị đúng | Kiểm tra tệp trong `assets/fonts/`, tên font và đường dẫn được khai báo |
| Âm thanh không tự phát | Kiểm tra chính sách autoplay của trình duyệt; ưu tiên phát sau thao tác của người dùng |
| Trang hoạt động khác nhau giữa máy tính và điện thoại | Kiểm tra responsive layout, kích thước màn hình và Console của trình duyệt |

## 9. Triển khai trực tuyến

Có thể triển khai website tĩnh trên dịch vụ phù hợp như Netlify hoặc GitHub Pages.

Trước khi triển khai:

1. Đảm bảo các tệp HTML, JavaScript và tài nguyên cần thiết nằm trong thư mục được xuất bản.
2. Kiểm tra đường dẫn tương đối của hình ảnh, phông chữ và âm thanh.
3. Cấu hình Supabase và kiểm tra quyền truy cập theo domain triển khai.
4. Kiểm thử các chức năng quan trọng trên URL thực tế sau khi deploy.
5. Không công khai thông tin bí mật trong repository.

## 10. Tác giả

**Trần Bảo Duy**

- Website cá nhân: https://tranbaoduy.netlify.app/

---

© 2026 Trần Bảo Duy. Bản quyền thuộc về tác giả.
