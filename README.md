# Hướng dẫn cài đặt và chạy dự án (Quick Start Guide)

Dưới đây là các bước đơn giản nhất để khởi động dự án:

## 1. Khởi tạo Môi trường (.env)

Đảm bảo bạn đã có các file cấu hình môi trường:

- **Backend**: Kiểm tra file `backend/.env`. Nếu chưa có, hãy tạo mới dựa trên thông tin sau:
  ```env
  DB_HOST=db
  DB_PORT=3307
  DB_USER=weconnect_user
  DB_PASSWORD=weconnect_pass_2024
  DB_NAME=weconnect
  SECRET_KEY=cde27db045c47d33eae575896076d9fafa1e063ac0b9343cadcc7a77fc3ae8d8
  ```
- **Frontend**: Kiểm tra file `frontend/.env`. Đảm bảo có dòng:
  ```env
  VITE_API_URL=http://localhost:8000
  ```

## 2. Chạy Docker (Database & Backend)

Mở terminal tại thư mục gốc của dự án (`itss-nhat-1`) và chạy:

```bash
# Khởi động database và backend
docker compose up -d
```

*Lưu ý: Đợi một lát để database khởi tạo xong (lần đầu sẽ chạy các file SQL trong `database/init`).*

## 3. Chạy Frontend

Mở một terminal mới và di chuyển vào thư mục frontend:

```bash
cd frontend

# Cài đặt thư viện (nếu là lần đầu)
pnpm install

# Chạy ở chế độ phát triển
pnpm dev
```

Sau khi chạy xong, bạn có thể truy cập giao diện tại địa chỉ hiển thị trong terminal (thường là `http://localhost:5173`).

---
**Thông tin truy cập mặc định:**
- Frontend: `http://localhost:5173`
- Backend API: `http://localhost:8000`
- Database (MySQL): Port `3307`

---

## 4. Tài khoản mẫu

Tất cả tài khoản dùng mật khẩu chung: **`Password@123`**

| Email | Vai trò | Trạng thái | Ghi chú |
|---|---|---|---|
| `nguyen.tuan@gmail.com` | USER | Đã xác thực | Học N3 |
| `tran.linh@gmail.com` | USER | Đã xác thực | Học N4 |
| `pham.anh@gmail.com` | USER | Đã xác thực | Level N2 |
| `le.mai@gmail.com` | USER | **Chưa xác thực** | Dùng để test OTP |
| `hoang.duc@gmail.com` | USER | Đã xác thực | Level N1 |
| `organizer.han@weconnect.vn` | ORGANIZER | Đã xác thực | Tổ chức sự kiện HN |
| `organizer.minh@weconnect.vn` | ORGANIZER | Đã xác thực | Tổ chức sự kiện HCM |

---

## 5. Danh sách chức năng (Feature Checklist)

Dưới đây là danh sách các tính năng được phát triển dựa trên [tài liệu đặc tả](dac_ta.md), sắp xếp theo đúng ID:

- [x] ID 1: **Thiết kế cơ sở dữ liệu**
- [x] ID 2: **Thiết lập môi trường phát triển**
- [x] ID 3: **Đăng ký tài khoản**
- [x] ID 4: **Đăng nhập**
- [x] ID 5: **Quên mật khẩu**
- [x] ID 6: **Quản lý hồ sơ**
- [-] ID 7: **Quản lý & Thống kê sự kiện**
- [ ] ID 9: **Tìm kiếm người dùng**
- [ ] ID 16: **Lọc kết quả tìm kiếm**
- [ ] ID 10: **Gửi lời mời kết bạn**
- [ ] ID 11: **Quản lý lời mời kết bạn**
- [ ] ID 12: **Quản lý bạn bè & huỷ kết bạn**
- [ ] ID 15: **Gợi ý kết bạn**
- [ ] ID 17: **Sự kiện & Trò chơi**
- [ ] ID 18: **Thiết lập hạ tầng WebSocket**
- [ ] ID 13: **Nhắn tin / Gọi điện / Dịch tin nhắn**
- [ ] ID 8: **Tích hợp API bên thứ 3 (OTP & Dịch thuật)**
- [ ] ID 14: **Chuyển đổi ngôn ngữ**

