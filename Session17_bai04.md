# Bài 4: Quản lý Môi trường Trình duyệt cho Dev

## Phần 1: So sánh Incognito vs Dedicated Profile

| Tiêu chí | Incognito Mode | Dedicated Profile |
|---|---|---|
| **Cách ly dữ liệu** | Tách khỏi cửa sổ thường, nhưng các cửa sổ ẩn danh dùng chung phiên nên không đăng nhập 2 tài khoản song song được | Mỗi profile có dữ liệu riêng (cookie, cache, extension), cách ly hoàn toàn, chạy song song được |
| **Lưu giữ trạng thái** | Đóng là mất sạch (cookie, session, bookmark, extension mặc định tắt) | Giữ bookmark, đăng nhập, extension, cài đặt; đồng bộ được |
| **Hiệu suất** | Mở nhanh nhưng phải đăng nhập/cấu hình lại mỗi lần | Thiết lập một lần, dùng lâu dài; tốn thêm RAM |

| | Ưu điểm | Nhược điểm |
|---|---|---|
| **Incognito** | Mở nhanh, không để lại dấu vết, tốt để test trạng thái chưa đăng nhập | Mất bookmark, không test song song nhiều tài khoản, phải đăng nhập lại |
| **Dedicated Profile** | Cách ly thật sự, giữ bookmark/extension lâu dài, test nhiều tài khoản cùng lúc | Cần thiết lập ban đầu, tốn RAM, dễ nhầm profile nếu không đặt tên/màu |

## Phần 2: Mô hình 3 Profile (Personal - Work - Sandbox)

| Profile | Mục đích | Nội dung |
|---|---|---|
| **Personal** | Việc cá nhân | Gmail, mạng xã hội, bookmark cá nhân |
| **Work** | Dự án LMS | GitHub, Jira, **bookmark tài liệu kỹ thuật**, DevTools |
| **Sandbox** | Kiểm thử | **Tài khoản test LMS** (admin, giảng viên, học viên), tắt Sync |

### Vì sao tối ưu hơn Ẩn danh

1. **Hết đăng xuất/đăng nhập:** tài khoản cá nhân và test nằm ở hai profile khác nhau, mở song song.
2. **Không mất bookmark:** profile Work lưu vĩnh viễn trên ổ đĩa.
3. **Test nhiều vai trò cùng lúc:** mỗi profile giữ một phiên riêng.
4. **An toàn:** không lẫn tài khoản thật với tài khoản test, extension cài riêng từng profile.
5. **Tái lập lỗi dễ:** Sandbox giữ cấu hình ổn định.

Incognito vẫn dùng làm công cụ phụ để test nhanh trạng thái guest hoặc loại trừ lỗi cache/extension.

**Kết luận:** Dùng 3 Profile làm môi trường chính, Incognito làm công cụ bổ trợ.