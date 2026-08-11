# Tập viết chữ Hán · Hoạt động hằng ngày

Bài tập viết chữ tương tác cho học sinh 4–10 tuổi, gồm bốn từ:

| Từ | Phiên âm | Nghĩa | Chữ cần học |
|---|---|---|---|
| 看书 | kànshū | đọc sách | 看, 书 |
| 画画 | huàhuà | vẽ tranh | 画 |
| 做饭 | zuòfàn | nấu ăn | 做, 饭 |
| 看电视 | kàn diànshì | xem ti vi | 看, 电, 视 |

Tổng cộng 7 chữ khác nhau — 看 (nhìn, xem) dùng chung cho cả 看书 lẫn 看电视. 画画 là từ có một chữ lặp lại hai lần (giống 妈妈, 爸爸), học một chữ 画 là viết được cả từ. Mỗi chữ có ba phần: xem hoạt hình bút thuận, tô theo nét mờ có chấm điểm, thi viết bằng trí nhớ. Hướng dẫn chuyển được ba ngôn ngữ Việt – Anh – Trung.

Ảnh gợi nhớ (mnemonic) minh hoạ:
- **看** (nhìn, xem): bàn tay che phía trên một con mắt — động tác nhìn xa quen thuộc.
- **书** (sách): cây bút xuyên qua chồng sách.
- **画** (vẽ, tranh): cây cọ vẽ bên khung tranh phong cảnh chia bốn ô, như một khung cửa sổ.
- **做** (làm): hai bạn nhỏ cùng giã chày vào cối — cùng nhau làm ra thứ gì đó.
- **饭** (cơm): bát cơm nóng hổi đầy ắp.
- **电** (điện): hình chữ giống hệt một tia sét ngoằn ngoèo.
- **视** (nhìn, trong 电视): bạn nhỏ chăm chú xem màn hình ti vi đã cắm điện.

## Cách dùng ba tab

- **👀 Xem mẫu** — tab mặc định khi mở mỗi chữ, xem hoạt hình bút thuận trước khi tự viết.
- **✏️ Tô nét** — mở ra là có thể tô ngay theo nét mờ, không cần bấm nút "Bắt đầu". Trượt tay theo hình mờ; sau 2 lần trượt máy tự nhấp nháy gợi ý. Nút "Làm lại" tô lại từ đầu ngay lập tức.
- **🏆 Thử tài** — không còn hình mờ, học sinh tự nhớ thứ tự nét; ô kẻ (chữ "米") được bật sẵn để dễ căn vị trí. Bấm "Bắt đầu thi" để tính giờ và số lần trượt.

看电视 có 3 chữ nên hàng nút chọn chữ con sẽ hiện đủ 3 nút; 画画 chỉ có 1 chữ nên không hiện hàng nút chọn (ẩn tự động).

Viết hoàn chỉnh xong một chữ (ở cả Tô nét lẫn Thử tài) sẽ có tiếng reo vui + hiệu ứng pháo giấy, cùng ⭐ hiện trên nút chữ đó. Nút 🔔 tắt/bật toàn bộ âm thanh.

## Màn hình tổng kết

Nút **📊 Kết quả** ở hàng tab mở bảng thống kê bất cứ lúc nào. Bảng cũng tự hiện khi học sinh viết xong cả 7 chữ.

Bảng gồm: tỉ lệ viết đúng chung, tổng số nét đúng và số lần trượt, và một dòng cho từng từ với thanh màu — xanh từ 90% trở lên, vàng từ 70%, cam nếu thấp hơn.

Cách tính: tỉ lệ = số nét viết đúng ÷ (số nét viết đúng + số lần viết trượt). Tính gộp cả phần Tô nét lẫn phần Thử tài, cộng dồn qua mọi lần luyện. Nút **Học lại từ đầu** xoá hết để bắt đầu lại (và tô nét sẽ sẵn sàng ngay).

## 1. Tải lên GitHub

Tạo một **repository mới** (khác với các bài trước). **Add file** → **Upload files** → kéo thả `index.html` và `README.md` → **Commit changes**.

## 2. Bật GitHub Pages

**Settings** → **Pages** → Source chọn **Deploy from a branch**, branch **main**, thư mục **/ (root)** → **Save**.

Chờ 1–3 phút, địa chỉ trang sẽ là `https://TEN-GITHUB.github.io/TEN-REPO/`

## 3. Nhúng vào website

```html
<iframe src="https://TEN-GITHUB.github.io/TEN-REPO/"
        width="100%" height="660" style="border:0;border-radius:16px"
        title="Tap viet chu Han - Hoat dong hang ngay"></iframe>
```

Kích thước viết thẳng trong thẻ `iframe`, không tách sang thẻ `<style>` riêng, vì ô nhúng của nhiều nền tảng sẽ xoá `<style>`. Trang bị cắt phía dưới thì tăng `height` lên 720 hoặc 800.

## Thêm từ mới

Mở `index.html`, tìm `const C={...}` ở đầu thẻ `<script>`, thêm chữ theo mẫu:

```js
"你":{p:"nǐ",
  m:{vi:"bạn, anh/chị",en:"you",zh:"你"},
  k:{vi:"...câu chuyện gợi nhớ...",en:"...",zh:"..."},
  r:{vi:["...quy tắc 1...","...quy tắc 2...","...","..."],
     en:["...","...","...","..."],
     zh:["...","...","...","..."]}},
```

Rồi thêm từ vào `const WORDS=[...]`:

```js
{w:"你", p:"nǐ", cs:["你"], m:{vi:"bạn",en:"you",zh:"你"}},
```

Thêm emoji tương ứng vào mảng `const EMOJI=[...]` (đúng thứ tự với `WORDS`), thêm ảnh gợi nhớ vào `const ART=[...]` và figure `<img id="artN" ...>` trong khối `<figure class="art">`, rồi thêm nút chọn từ vào `<div class="words">`, sao chép nút có sẵn và sửa `data-w` thành số thứ tự mới.

Không cần khai báo số nét — chương trình tự đếm từ dữ liệu nét chữ khi tải về. Ảnh gợi nhớ nên nén nhỏ (dùng định dạng `webp`, rộng khoảng 300–350px) và nhúng dạng `data:image/webp;base64,...` để file vẫn chạy được khi chỉ có một file `index.html` duy nhất, không cần tải ảnh riêng.

Muốn đổi tiếng "reo vui" khi viết xong một chữ: tìm `const YAY_B64="..."` trong `<script>`, thay bằng chuỗi base64 của file mp3/âm thanh khác.

## Lưu ý

- Máy học sinh cần Internet: dữ liệu nét chữ tải từ Hanzi Writer trên CDN.
- Nếu mạng trường chặn `cdn.jsdelivr.net` và `unpkg.com`, phần viết chữ sẽ không hiện.
- Dữ liệu nét chữ lấy từ dự án Make Me A Hanzi, giấy phép mở.
- Ảnh gợi nhớ (mnemonic) và âm thanh khi hoàn thành đã được nhúng sẵn ngay trong `index.html` (dạng base64), không cần file rời.
