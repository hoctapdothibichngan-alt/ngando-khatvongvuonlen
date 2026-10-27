# SỐNG — Chạm Vào Những Ngày Lưng Chừng

Website tạp chí đời sống chậm (Editorial Slow-Living Journal) dành cho những lát cắt cuộc sống hàng ngày: vui bình dị, buồn man mác, trầm ngâm chiều muộn, triết lý sâu sắc và những điểm chạm của **"tuổi lưng chừng"**.

## 1. Cấu trúc thư mục

```text
song-website/
├── index.html                 # Trang chính với đầy đủ các khu vực và Reading Modal
├── css/
│   └── style.css              # Hệ thống thiết kế Editorial, bảng màu Giấy ấm / Đêm trầm
├── js/
│   └── app.js                 # Cấu hình SITE_CONFIG, dữ liệu dự phòng, bộ lọc, modal, canvas, localStorage
├── data/
│   └── posts.json             # 8 bài tản văn hoàn chỉnh, 5 điểm chạm lưng chừng, 12 thẻ triết lý
├── assets/
│   └── images/                # Bộ ảnh nghệ thuật chủ đề Sống chậm
└── README.md                  # Tài liệu hướng dẫn vận hành & xuất bản GitHub Pages
```

## 2. Hướng dẫn cá nhân hóa thông tin tác giả

Mở file `js/app.js`, tại ngay những dòng đầu tiên trong đối tượng `SITE_CONFIG`:

```javascript
const SITE_CONFIG = {
  ownerName: "Tên hoặc Bút danh của bạn",
  ownerRole: "Người ghi chép những lát cắt tuổi lưng chừng",
  ownerBio: "Đôi dòng giới thiệu về bạn...",
  ownerAvatar: "",
  contactEmail: "emailcuaban@gmail.com",
  socialFacebook: "https://facebook.com/...",
  socialZalo: "https://zalo.me/..."
};
```
*(Nếu bạn để trống các trường liên hệ, website sẽ tự động ẩn nút liên kết để tránh lỗi đường dẫn trống).*

## 3. Hướng dẫn chạy thử trên máy tính

- **Cách 1 (Mở trực tiếp):** Nhấp đúp vào `index.html` để mở ngay trên trình duyệt (nhờ cơ chế dữ liệu dự phòng `FALLBACK_DATA` tích hợp sẵn).
- **Cách 2 (Chạy qua Local Server):** Mở Terminal tại thư mục `song-website` và chạy:
  ```bash
  python -m http.server 8000
  ```
  Sau đó truy cập `http://localhost:8000`.

## 4. Hướng dẫn xuất bản miễn phí lên GitHub Pages

1. Đăng nhập vào GitHub và tạo một Repository mới (ví dụ: `song-journal`).
2. Tải toàn bộ các file và thư mục trong `song-website` lên Repository.
3. Vào mục **Settings** → **Pages** → dưới phần **Branch**, chọn nhánh `main` (thư mục `/root`) và bấm **Save**.
4. Chờ khoảng 1–2 phút, website của bạn sẽ hoạt động tại địa chỉ `https://<ten-tai-khoan>.github.io/song-journal/`.
