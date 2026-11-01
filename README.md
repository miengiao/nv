# Lịch Công Việc Miền – bản GitHub Pages

Giao diện chạy trên GitHub Pages (nhanh, có link riêng, nhận thông báo, cài ra màn hình chính).
Dữ liệu và xử lý vẫn ở Google Apps Script + Google Sheet.

## Cài đặt (làm 1 lần)
1. **Apps Script**: dán `Code.gs` + `Index.html` mới nhất → Lưu → chạy `setup` 1 lần →
   **Triển khai → Quản lý tùy chọn triển khai → ✎ → Phiên bản mới → Triển khai**.
   (Thực thi dưới dạng: *Tôi* · Ai có quyền truy cập: *Bất kỳ ai*.) Copy link kết thúc bằng `/exec`.
2. Mở file `index.html` trong thư mục này, tìm dòng
   `<meta name="api-url" content="DAN_LINK_EXEC_VAO_DAY">` → thay `DAN_LINK_EXEC_VAO_DAY` bằng link `/exec`.
3. **GitHub**: tạo kho mới (VD `lich-cv-mien`, để *Public*) → **Add file → Upload files** → kéo thả cả 6 file:
   `index.html`, `manifest.webmanifest`, `sw.js`, `icon-192.png`, `icon-512.png`, `README.md` → **Commit**.
4. Kho → **Settings → Pages** → Source: *Deploy from a branch* → Branch `main` / `(root)` → **Save**.
   Sau 1–2 phút có link dạng `https://<tên-tài-khoản>.github.io/lich-cv-mien/`.
5. (Tuỳ chọn) Tên miền riêng: Settings → Pages → Custom domain (VD `lich.tenmien.vn`),
   rồi vào Tenten tạo bản ghi **CNAME** `lich` → `<tên-tài-khoản>.github.io`.

## Lưu ý
- **Khi sửa code**: Code.gs → chỉ cần *Phiên bản mới* (link `/exec` giữ nguyên nếu sửa trong "Quản lý tùy chọn triển khai").
  Index.html → upload lại `index.html` lên GitHub (nhớ giữ dòng api-url).
- **Thông báo**: bấm 🔕 trên đầu app để bật. Android/máy tính: báo khi app đang mở hoặc chạy nền.
  iPhone (iOS 16.4+): phải **Chia sẻ → Thêm vào MH chính**, mở app từ biểu tượng rồi mới bật được.
- **Camera góc siêu rộng**: app tự chọn ống kính 0.5x nếu điện thoại cho phép web dùng; nếu không, dùng camera thường.
  Trình duyệt không mở được camera thì app chuyển sang camera của máy.
- Kho GitHub công khai chỉ chứa giao diện; mật khẩu, PIN, dữ liệu đều nằm trong Sheet/Apps Script.
