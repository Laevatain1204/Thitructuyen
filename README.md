# 📝 Thi Trực Tuyến — Đánh Giá Năng Lực

Hệ thống thi trực tuyến hiện đại, được build bằng **React + TypeScript + Tailwind CSS**.

## 🚀 Deploy lên GitHub Pages

### Cách 1 — Dùng thư mục `dist` (nhanh nhất)

1. Upload toàn bộ nội dung thư mục `dist/` lên repository
2. Vào **Settings → Pages → Branch**: chọn `main`, thư mục `/` (root)
3. Truy cập tại: `https://<username>.github.io/<repo-name>/`

### Cách 2 — Build từ source code

```bash
# Cài đặt dependencies
pnpm install   # hoặc npm install

# Chạy local
pnpm dev

# Build production
pnpm build

# Thư mục dist/ chứa file để deploy
```

## 📁 Cấu trúc dự án

```
exam-online/
├── index.html              # Entry point
├── src/
│   ├── App.tsx             # Root component + routing
│   ├── types.ts            # TypeScript types
│   ├── store.ts            # Data layer (localStorage)
│   ├── exportExcel.ts      # Xuất kết quả CSV/Excel
│   └── components/
│       ├── LandingPage.tsx      # Trang chủ + khẩu hiệu
│       ├── LoginPage.tsx        # Đăng nhập / Đăng ký SV
│       ├── RoomsPage.tsx        # Chọn & tìm kiếm phòng thi
│       ├── ExamPage.tsx         # Giao diện làm bài thi
│       ├── ResultPage.tsx       # Kết quả sau khi nộp
│       ├── AdminLoginPage.tsx   # Đăng nhập giảng viên
│       └── AdminDashboard.tsx   # Quản lý phòng thi + kết quả
├── dist/                   # ✅ Build output — dùng để deploy
│   ├── index.html
│   └── assets/
│       ├── index-*.js      # JS bundle
│       └── index-*.css     # CSS bundle
└── vite.config.ts
```

## 🔑 Tài khoản demo

| Vai trò | Thông tin đăng nhập |
|---------|-------------------|
| **Sinh viên** | Mã SV: `SV001` / Mật khẩu: `123456` |
| **Admin** | Mật khẩu: `admin2024` |

## 📦 Phòng thi mẫu

| Mã phòng | Tên | Mật khẩu |
|----------|-----|---------|
| `TOAN101` | Toán Cao Cấp A1 | `1234` |
| `LY201` | Vật Lý Đại Cương | *(không cần)* |
| `CNTT301` | Lập Trình Hướng Đối Tượng | `cntt2024` |

## ✨ Tính năng

- **Sinh viên:** Đăng nhập · Chọn phòng thi · Làm bài trắc nghiệm ABCD · Đồng hồ đếm ngược · Đánh dấu câu · Xem kết quả chi tiết
- **Admin:** Tạo/sửa/xoá phòng thi · Soạn câu hỏi · Xem điểm tất cả SV · Xuất Excel
- **Bảo mật:** Chấm điểm không để lộ đáp án cho client · Phòng thi có mật khẩu

## 🛠 Tech Stack

- React 18 + TypeScript
- Tailwind CSS
- Vite
- localStorage (không cần backend)
