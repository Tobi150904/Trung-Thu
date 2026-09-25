# Thiệp Trung Thu – bản ghép
Luồng: Source 1 (mở đầu → đom đóm → đèn ông sao) → morph 3D sang các lớp Source 2 → zoom mặt trăng → thỏ Source 1 bay đáp lên cành hoa → hiện "Ấn giữ vào mặt trăng" → toàn bộ Source 2 (thư, trái tim, nhạc).
Chạy bằng HTTP server (không mở file:// trực tiếp):  `npx serve .`  hoặc  `python3 -m http.server`
- index.html: bộ điều phối chuyển cảnh.
- s1/: Source 1 (đã cắt trước phần thư, gửi tín hiệu sang bộ điều phối, nhạc được tắt dần khi chuyển).
- s2/: Source 2 (đã bỏ 11-rabbit.webp, thay bằng thỏ tho.webp của Source 1).
