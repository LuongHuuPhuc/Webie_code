# HTML là gì ? #
HTML (HyperText Markup Language) là ngôn ngữ đánh dấu dùng để xây dựng cấu trúc cho một trang web. HTML dùng các thẻ (tag) để phân chia và tổ chức nội dung văn bản (văn bản, hình ảnh, video, liên kết,...)

## Cấu trúc cơ bản của một file HTML ##
```html 
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>Trang của tôi</title>
</head>
<body>
  <h1>Xin chào!</h1>
  <p>Đây là trang web hiển thị dữ liệu từ ESP32</p>
</body>
</html>
```

## Các thẻ HTML phổ biến ##
|Thẻ|Chức năng| 
|---|---------|
|<!DOCTYPE html>| Khai báo kiểu tài liệu HTML5|
|`<html>`| Thẻ bao toàn bộ trang|
|`<head>`| Chứa thông tin meta, tiêu đề <title>, CSS, script|
|`<title>`| Tiêu đề tab trình duyệt |
|`<meta charset="UTF-8">`|Khai báo bảng mã UTF-8 (hỗ trợ tiếng Việt)|
|`<body>`|Phần hiển thị chính của trang (nội dung người dùng nhìn thấy)|

### 1. Các thẻ văn bản ###
|Thẻ|Chức năng|
|---|---------|
|`<h1>` đến `<h6>`| Tiêu đề văn bản từ lớn đến nhỏ|
|`<p>`|Đoạn văn|
|`<br>`|Xuống dòng|
|`<hr>`|Kẻ đường ngang|
|`<strong>` hoặc `<b>`|In đậm|
|`<em>` hoặc `<i>`|In nghiêng|
|`<span>`| Nội dung nhỏ, để định dạng một phần nội dung|
|`<div>`|Khối nội dung (phân vùng giao diện)|

### 2. Liên kết và ảnh ###
|Thẻ|Chức năng|
|---|---------|
|`<a href="...">`|Tạo liên kết|
|`<img src="..." alt="...">`| Hiển thị hình ảnh|

### 3. Biểu mẫu (Form) nhập liệu ###
|Thẻ|Chức năng|
|---|---------|
|`<form>`| Khung biểu mẫu|
|`<input>`| Nhập liệu (text, number,...)|
|`<textarea>`|Nhập nội dung dài|
|`<button>` hoặc `<input type="submit">`|Nút gửi dữ liệu|

Ví du:
```html
<form>
  <label for="temp">Nhiệt độ:</label>
  <input type="text" id="temp">
</form>
```

### 4. Thẻ giao diện nâng cao ###
|Thẻ|Chức năng|
|---|---------|
|`<table>`|Bảng dữ liệu|
|`<ul>/<ol>`|Danh sách (unordered/ordered)|
|`<li>`|Mỗi mục trong danh sách|
|`<script>`|Dùng để nhúng Javascript|
|`<style>`|Dùng để viết CSS nội trang|

## Các thuộc tính chung cho mọi thẻ HTML ## 
|Thuộc tính| Mô tả|
|----------|------|
|`id`| Định danh duy nhất cho một phần tử|
|`class`| Nhóm các phần tử để áp dụng CSS hoặc JS|
|`style`|Viết CSS trực tiếp từ trong phần tử|
|`title`| Hiển thị chú thích khi rê chuột|
|`hidden`|Ẩn phần tử khỏi hiển thị|
|`data-*`|Tạo thuộc tính tùy chỉnh (custom data)|

### 1. Thuộc tính thẻ `<input>`, `<textarea>`, `<select>` ###
| Thuộc tính     | Mô tả                                                |
| -------------- | ---------------------------------------------------- |
| `type`         | Loại ô nhập (text, password, checkbox,...)           |
| `value`        | Giá trị mặc định hoặc hiện tại                       |
| `name`         | Tên dùng để gửi dữ liệu khi submit                   |
| `placeholder`  | Gợi ý nội dung nên nhập                              |
| `required`     | Bắt buộc phải nhập                                   |
| `readonly`     | Chỉ đọc, không cho chỉnh sửa                         |
| `disabled`     | Vô hiệu hóa trường nhập                              |
| `maxlength`    | Số ký tự tối đa cho phép                             |
| `min`, `max`   | Giới hạn giá trị số/ngày                             |
| `checked`      | Checkbox/Radio được chọn mặc định                    |
| `autocomplete` | Cho phép trình duyệt gợi ý nội dung đã nhập trước đó |

### 2. Thuộc tính thẻ `<a>` (liên kết) ###
| Thuộc tính | Mô tả                                                        |
| ---------- | ------------------------------------------------------------ |
| `href`     | Đường dẫn URL đến nơi muốn chuyển                            |
| `target`   | Mở liên kết ở đâu (`_blank`, `_self`, ...)                   |
| `download` | Tải file thay vì mở nó                                       |
| `rel`      | Quan hệ giữa trang hiện tại và trang liên kết (SEO, bảo mật) |

### 3. Thuộc tính `<img>`, `<video>`, `<audio>` ###
| Thuộc tính        | Mô tả                                   |
| ----------------- | --------------------------------------- |
| `src`             | Đường dẫn file                          |
| `alt`             | Mô tả ảnh (dành cho SEO và khi ảnh lỗi) |
| `width`, `height` | Kích thước                              |
| `controls`        | Hiện điều khiển (cho video/audio)       |
| `autoplay`        | Tự động chạy                            |
| `loop`            | Phát lại liên tục                       |
| `muted`           | Bật tắt âm thanh                        |

### 4. Thuộc tính `<form>`, `<button>` ###
| Thuộc tính      | Mô tả                                      |
| --------------- | ------------------------------------------ |
| `action`        | URL nơi dữ liệu form sẽ gửi đến            |
| `method`        | Cách gửi dữ liệu (`GET` hoặc `POST`)       |
| `enctype`       | Kiểu mã hóa dữ liệu (dùng khi upload file) |
| `target`        | Mở kết quả gửi ở đâu                       |
| `type` (button) | `submit`, `reset`, `button`                |

### 5. Thuộc tính sự kiện ###
| Thuộc tính                  | Mô tả                   |
| --------------------------- | ----------------------- |
| `onclick`                   | Khi click vào           |
| `onchange`                  | Khi giá trị thay đổi    |
| `oninput`                   | Khi nhập dữ liệu        |
| `onmouseover`, `onmouseout` | Khi rê chuột vào/ra     |
| `onkeydown`, `onkeyup`      | Khi nhấn/phát hành phím |

Ví dụ: 
```html
<input 
  id="email" 
  class="form-control" 
  name="email" 
  type="email" 
  placeholder="Nhập email của bạn" 
  required 
  maxlength="50">
```
## MẸO: ##
* HTML chỉ xây dựng khung cho trang web
* Để làm đẹp -> Dùng CSS (`<style>`)
* Để có chức năng kết nối MQTT socket -> Dùng Javascript (`<script>`)
