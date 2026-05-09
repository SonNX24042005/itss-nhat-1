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
