# TÀI LIỆU CĂN CỨ LIVE CODE HTML5 THUẦN (THEO 5 SLIDE MẪU)
**Học phần:** Lập Trình Web PHP (`IN4502N`) — **Chương 2: HTML**  
**File khung gõ trên VS Code:** [`khung_live_code.html`](./khung_live_code.html)  
**File đối chiếu đã code xong:** [`khung_live_code_da_code.html`](./khung_live_code_da_code.html)  
**Ảnh minh họa đi kèm:** [`logo_php.png`](./logo_php.png)

---

## 1. Chia đều 5 nhóm thẻ thông dụng thành 2 phần cân bằng (~38 dòng vs ~36 dòng)

| Phần trình bày | Mục trên Slide | Các thẻ sử dụng | Số dòng code | Trọng tâm giải thích khi demo |
| :--- | :--- | :--- | :---: | :--- |
| **Phần 1** *(Nửa đầu)* | **Mục 1:** Thẻ Tiêu Đề & Định Dạng Văn Bản | `<h1>`, `<h2>`, `<h3>`, `<hr>`, `<p>`, `<strong>`, `<em>`, `<u>`, `<br>` | ~14 dòng | Phân cấp tiêu đề `h1`–`h3`, đường kẻ `<hr>`, định dạng chữ và xuống dòng `<br>` |
| **Phần 1** *(Nửa đầu)* | **Mục 2:** Nhóm Thẻ Danh Sách (Lists) | `<h4>`, `<ul>`, `<ol>`, `<li>` | ~13 dòng | So sánh `<ul>` (không thứ tự) và `<ol>` (đánh số thứ tự 1, 2, 3) |
| **Phần 1** *(Nửa đầu)* | **Mục 3:** Thẻ Liên Kết & Đa Phương Tiện | `<a href="..." target="_blank">`, `<img src="logo_php.png" alt="..." width="100">`, `<audio controls>`, `<source>` | ~11 dòng | Mở trang mới với `target="_blank"`, thẻ tự đóng `<img>`, phát âm thanh `<audio>` |
| **Phần 2** *(Nửa sau)* | **Mục 4:** Nhóm Thẻ Bảng Biểu (Tables) | `<table border="1">`, `<tr>`, `<th>`, `<td>`, `rowspan="2"`, `colspan="3"`, `align="center"` | ~20 dòng | Bảng Thời khóa biểu, gộp 2 hàng dọc (`rowspan`) và gộp 3 cột ngang (`colspan`) |
| **Phần 2** *(Nửa sau)* | **Mục 5:** Nhóm Thẻ Biểu Mẫu (Forms) | `<form action="xuly.php" method="POST">`, `<label>`, `<input type="email\|password">`, `<select>`, `<option>`, `<button type="submit">` | ~16 dòng | Cốt lõi PHP: `action`, `method="POST"`, thuộc tính `name`, `placeholder`, `required` |

---

## 2. Gợi ý gõ tắt Emmet trên VS Code cho 5 mục

> Mở [`khung_live_code.html`](./khung_live_code.html) trên VS Code (bật **File → Auto Save**), chạy **Live Server** (`Alt + L`, `Alt + O`) bên phải màn hình, rồi đặt con trỏ dưới từng comment tương ứng và gõ:

| Mục | Chuỗi gõ tắt Emmet (gõ xong bấm `Tab` / `Enter`) | Kết quả sinh ra tự động |
| :--- | :--- | :--- |
| **Mục 1 (Tiêu đề & Văn bản)** | `h1+h2+h3` rồi `hr` rồi `p` | Tạo nhanh 3 mức tiêu đề, đường kẻ ngang và đoạn văn |
| **Mục 2 (Danh sách)** | `h4+ul>li*3` và `h4+ol>li*3` | Tạo ngay tiêu đề `<h4>` kèm danh sách 3 mục `<li>` |
| **Mục 3 (Link & Media)** | `a[target=_blank]` rồi `img[src=logo_php.png width=100]` rồi `audio[controls]>source` | Tạo nhanh thẻ liên kết, thẻ ảnh và trình phát audio |
| **Mục 4 (Bảng biểu)** | `table[border=1]>tr*4` | Tạo nhanh bảng có viền với 4 hàng `<tr>` |
| **Mục 5 (Biểu mẫu)** | `form[action=xuly.php method=POST]` rồi `select[name=role]>option*2` | Tạo form gửi POST tới `xuly.php` và hộp chọn 2 vai trò |

---

## 3. Code căn cứ — Phần 1 (Mục 1, Mục 2, Mục 3)

### Mục 1: Thẻ Tiêu Đề & Định Dạng Văn Bản
```html
        <!-- 1. Cấp độ tiêu đề h1 -> h6 -->
        <h1>Tiêu đề H1 (Lớn nhất)</h1>
        <h2>Tiêu đề H2 (Nhỏ hơn)</h2>
        <h3>Tiêu đề H3 (Nhỏ vừa)</h3>

        <!-- 2. Đường kẻ phân cách -->
        <hr>

        <!-- 3. Đoạn văn và định dạng chữ -->
        <p>
            Đây là chữ <strong>in đậm</strong>,
            chữ <em>in nghiêng</em>, và chữ <u>gạch chân</u>.
            <br>
            Dòng này đã được ngắt xuống hàng bằng thẻ br.
        </p>
```

### Mục 2: Nhóm Thẻ Danh Sách (Lists)
```html
        <!-- 1. Danh sách không thứ tự (ul) -->
        <h4>Kỹ Năng Cần Học:</h4>
        <ul>
            <li>HTML5 Markup</li>
            <li>CSS3 Styling</li>
            <li>Lập trình Web PHP</li>
        </ul>

        <!-- 2. Danh sách có thứ tự (ol) -->
        <h4>Các Bước Thực Hiện:</h4>
        <ol>
            <li>Dựng khung HTML</li>
            <li>Trang trí bằng CSS</li>
            <li>Xử lý backend PHP & MySQL</li>
        </ol>
```

### Mục 3: Thẻ Liên Kết & Đa Phương Tiện
```html
        <!-- 1. Thẻ siêu liên kết (Link) -->
        <a href="https://dthu.edu.vn" target="_blank">
            Cổng thông tin ĐH Đồng Tháp →
        </a>

        <!-- 2. Thẻ hình ảnh (tự đóng) -->
        <img src="logo_php.png"
             alt="Logo PHP"
             width="100">

        <!-- 3. Thẻ phát âm thanh -->
        <audio controls>
            <source src="podcast.mp3" type="audio/mpeg">
        </audio>
```

---

## 4. Code căn cứ — Phần 2 (Mục 4, Mục 5)

### Mục 4: Nhóm Thẻ Bảng Biểu (Tables)
```html
        <!-- Bảng thời khóa biểu (rowspan & colspan) -->
        <table border="1">
            <tr>
                <th>Thứ</th>
                <th>Môn học</th>
                <th>Phòng</th>
            </tr>
            <tr>
                <!-- rowspan: Gộp 2 hàng dọc -->
                <td rowspan="2">Thứ Hai</td>
                <td>Lập trình Web PHP</td>
                <td>Lab 03</td>
            </tr>
            <tr>
                <td>Cơ sở dữ liệu MySQL</td>
                <td>Lab 01</td>
            </tr>
            <tr>
                <!-- colspan: Gộp 3 cột ngang -->
                <td colspan="3" align="center">Ghi chú: Lớp học cả ngày</td>
            </tr>
        </table>
```

### Mục 5: Nhóm Thẻ Biểu Mẫu (Forms)
```html
        <!-- form gửi dữ liệu sang file xuly.php qua POST -->
        <form action="xuly.php" method="POST">

            <label>Email đăng nhập:</label>
            <input type="email" name="user_email"
                   placeholder="name@dthu.edu.vn" required>

            <label>Mật khẩu:</label>
            <input type="password" name="user_pass" required>

            <label>Vai trò:</label>
            <select name="role">
                <option value="sv">Sinh viên</option>
                <option value="gv">Giảng viên</option>
            </select>

            <button type="submit">Đăng Nhập</button>
        </form>
```

---

## 5. Toàn bộ mã nguồn hoàn chỉnh (khớp 100% với `khung_live_code_da_code.html`)

```html
<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Demo Các Thẻ HTML Thông Dụng - Chương 2</title>
</head>
<body>

    <!-- ================= 1. THẺ TIÊU ĐỀ & ĐỊNH DẠNG VĂN BẢN ================= -->
    <div>
        <!-- 1. Cấp độ tiêu đề h1 -> h6 -->
        <h1>Tiêu đề H1 (Lớn nhất)</h1>
        <h2>Tiêu đề H2 (Nhỏ hơn)</h2>
        <h3>Tiêu đề H3 (Nhỏ vừa)</h3>

        <!-- 2. Đường kẻ phân cách -->
        <hr>

        <!-- 3. Đoạn văn và định dạng chữ -->
        <p>
            Đây là chữ <strong>in đậm</strong>,
            chữ <em>in nghiêng</em>, và chữ <u>gạch chân</u>.
            <br>
            Dòng này đã được ngắt xuống hàng bằng thẻ br.
        </p>
    </div>

    <hr>

    <!-- ================= 2. NHÓM THẺ DANH SÁCH (LISTS) ================= -->
    <div>
        <!-- 1. Danh sách không thứ tự (ul) -->
        <h4>Kỹ Năng Cần Học:</h4>
        <ul>
            <li>HTML5 Markup</li>
            <li>CSS3 Styling</li>
            <li>Lập trình Web PHP</li>
        </ul>

        <!-- 2. Danh sách có thứ tự (ol) -->
        <h4>Các Bước Thực Hiện:</h4>
        <ol>
            <li>Dựng khung HTML</li>
            <li>Trang trí bằng CSS</li>
            <li>Xử lý backend PHP & MySQL</li>
        </ol>
    </div>

    <hr>

    <!-- ================= 3. THẺ LIÊN KẾT & ĐA PHƯƠNG TIỆN ================= -->
    <div>
        <!-- 1. Thẻ siêu liên kết (Link) -->
        <a href="https://dthu.edu.vn" target="_blank">
            Cổng thông tin ĐH Đồng Tháp →
        </a>

        <!-- 2. Thẻ hình ảnh (tự đóng) -->
        <img src="logo_php.png"
             alt="Logo PHP"
             width="100">

        <!-- 3. Thẻ phát âm thanh -->
        <audio controls>
            <source src="podcast.mp3" type="audio/mpeg">
        </audio>
    </div>

    <hr>

    <!-- ================= 4. NHÓM THẺ BẢNG BIỂU (TABLES) ================= -->
    <div>
        <!-- Bảng thời khóa biểu (rowspan & colspan) -->
        <table border="1">
            <tr>
                <th>Thứ</th>
                <th>Môn học</th>
                <th>Phòng</th>
            </tr>
            <tr>
                <!-- rowspan: Gộp 2 hàng dọc -->
                <td rowspan="2">Thứ Hai</td>
                <td>Lập trình Web PHP</td>
                <td>Lab 03</td>
            </tr>
            <tr>
                <td>Cơ sở dữ liệu MySQL</td>
                <td>Lab 01</td>
            </tr>
            <tr>
                <!-- colspan: Gộp 3 cột ngang -->
                <td colspan="3" align="center">Ghi chú: Lớp học cả ngày</td>
            </tr>
        </table>
    </div>

    <hr>

    <!-- ================= 5. NHÓM THẺ BIỂU MẪU (FORMS) ================= -->
    <div>
        <!-- form gửi dữ liệu sang file xuly.php qua POST -->
        <form action="xuly.php" method="POST">

            <label>Email đăng nhập:</label>
            <input type="email" name="user_email"
                   placeholder="name@dthu.edu.vn" required>

            <label>Mật khẩu:</label>
            <input type="password" name="user_pass" required>

            <label>Vai trò:</label>
            <select name="role">
                <option value="sv">Sinh viên</option>
                <option value="gv">Giảng viên</option>
            </select>

            <button type="submit">Đăng Nhập</button>
        </form>
    </div>

</body>
</html>
```
