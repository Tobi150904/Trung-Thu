# Thiệp Trung Thu — bản tĩnh (HTML/CSS/JS)

Bản sao tĩnh của https://t.dlove.vn/minhchauiu. Không gọi API, không cần backend:
toàn bộ nội dung (lời chúc, ảnh, nhạc, danh sách chữ bay) đã được ghim sẵn trong
`data/access.json`, ảnh/nhạc riêng nằm trong `media/`.

## Cách chạy

Cần một web server tĩnh (mở trực tiếp bằng file:// sẽ không chạy vì trang dùng
JavaScript module):

```bash
cd thiep-trung-thu-static
python3 -m http.server 8080
# mở http://localhost:8080
```

Hoặc upload toàn bộ thư mục lên bất kỳ hosting tĩnh nào (Netlify, Vercel,
GitHub Pages, Cloudflare Pages, hosting cPanel...). Mọi đường dẫn đều là tương
đối, nên đặt ở thư mục gốc hay thư mục con (ví dụ `tenmien.com/thiep/`) đều chạy.

## Cấu trúc

- `index.html` — trang chính; có đoạn script nhỏ chặn mọi lời gọi API và trả về
  `data/access.json`; mã thiệp được ghim sẵn nên không phụ thuộc đường dẫn.
- `assets/` — mã JS/CSS đã build, hình nền, hình thỏ, giao diện, phông chữ.
- `media/` — ảnh đôi, 6 ảnh bay và file nhạc nền.
- `data/access.json` — dữ liệu tấm thiệp (đổi chữ trong đây là đổi nội dung).

## Chỉnh sửa nội dung

Mở `data/access.json`:
- `letter.text` — nội dung lá thư
- `flyingTexts` — các câu chữ bay
- `flyingImages`, `couplePhoto` — thay bằng ảnh mới bỏ vào `media/`
- `bgMusic` — nhạc nền

## Ghi chú

- Script chống DevTools của bản gốc đã được gỡ bỏ.
- Hạn sử dụng (`expiresAt`) đã đặt tới năm 2099 để thiệp không hết hạn.
- Đây là bản sao phục vụ mục đích cá nhân/học tập; bản quyền hình ảnh, nhạc và
  mã nguồn thuộc về chủ sở hữu trang gốc.
