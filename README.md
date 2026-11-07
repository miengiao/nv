# Lịch Công Việc Miền – bản GitHub Pages

Giao diện chạy trên GitHub Pages (nhanh, có link riêng, nhận thông báo, cài ra màn hình chính).
Dữ liệu và xử lý vẫn ở Google Apps Script + Google Sheet.

## Cài đặt (làm 1 lần)
1. **Apps Script**: dán `Code.gs` + `Index.html` mới nhất → Lưu → chạy `setup` 1 lần →
   **Triển khai → Quản lý tùy chọn triển khai → ✎ → Phiên bản mới → Triển khai**.
   (Thực thi dưới dạng: *Tôi* · Ai có quyền truy cập: *Bất kỳ ai*.) Copy link kết thúc bằng `/exec`.
2. **Gắn link máy chủ (làm 1 lần duy nhất):** trong kho GitHub bấm **Add file → Create new file**,
   đặt tên `api.txt`, nội dung chỉ 1 dòng là link `/exec` → **Commit**.
   Các lần cập nhật sau chỉ upload file mới, **không** cần dán lại link (zip không chứa api.txt nên không bị ghi đè).
3. **GitHub**: tạo kho mới (VD `lich-cv-mien`, để *Public*) → **Add file → Upload files** → kéo thả cả 6 file:
   `index.html`, `manifest.webmanifest`, `sw.js`, `icon-192.png`, `icon-512.png`, `README.md` → **Commit**.
4. Kho → **Settings → Pages** → Source: *Deploy from a branch* → Branch `main` / `(root)` → **Save**.
   Sau 1–2 phút có link dạng `https://<tên-tài-khoản>.github.io/lich-cv-mien/`.
5. (Tuỳ chọn) Tên miền riêng: Settings → Pages → Custom domain (VD `lich.tenmien.vn`),
   rồi vào Tenten tạo bản ghi **CNAME** `lich` → `<tên-tài-khoản>.github.io`.

## Lưu ý
- **Khi sửa code**: Code.gs → chỉ cần *Phiên bản mới* (link `/exec` giữ nguyên nếu sửa trong "Quản lý tùy chọn triển khai").
  Index.html → upload lại các file mới lên GitHub (api.txt giữ nguyên).
- **Thông báo**: bấm 🔕 trên đầu app để bật. Android/máy tính: báo khi app đang mở hoặc chạy nền.
  iPhone (iOS 16.4+): phải **Chia sẻ → Thêm vào MH chính**, mở app từ biểu tượng rồi mới bật được.
- **Camera góc siêu rộng**: app tự chọn ống kính 0.5x nếu điện thoại cho phép web dùng; nếu không, dùng camera thường.
  Trình duyệt không mở được camera thì app chuyển sang camera của máy.
- Kho GitHub công khai chỉ chứa giao diện; mật khẩu, PIN, dữ liệu đều nằm trong Sheet/Apps Script.
