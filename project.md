# Xây dựng 1 website
1. Phân tích: `Giao diện`
2. Dựng nền móng - dựng base
3. Xây dựng từng thành phân theo phân tích
4. Hoàn thiện

## Phân tích 
1. Những thành phần thường gặp trên giao diện 1 web
- Header
- Banner: ảnh, băng quảng cáo đặt ở 1 nơi nào đó trong web
- Navigation: phần điều hướng, nằm ở trong đa số các trang liên quan
=> Nhấn vào để hướng đến trang khác. `VD: nút trang chủ, ...`
- Breadcrumb: thanh cho biết đang ở đâu. `VD: Trang chủ > Bài học > HTML - CSS`
- Sidebar: một thanh đặt ở 1 phía màn hình => chứa bất cứ thứ gì bao gồm cả các navigation phụ
           cũng có thể thu gọn lại cho dễ nhìn. VD: `tab của Edge`
- Slider: thanh trượt (có thể là bất cứ nội dung gì)
- Content: nội dung trong trang web
- Footer

## Thực hành
 https://fullstack.edu.vn/external-url?continue=https%3A%2F%2Fwww.w3schools.com%2Fw3css%2Ftryw3css_templates_band.htm
1. Phân tích
- Header
- Slider (hình ảnh tự động thay đổi / tự động trượt)
- Content
  - Giới thiệu (about)
  - Tour
  - Contact
  - Image
- Footer

2. Dựng base (tham khảo)
- Đặt tên: đơn giản, dễ tìm kiếm
- Tạo file index.html
- Tạo thư mục assets (chứa file tĩnh): img: chứa ảnh, chứa CSS: style.css 
- Link file css vào html
- Nhấn ! -> tab để tạo nhanh cấu trúc file html
- link -> tab -> gắn link file css vào phần header của file html  
- reset lại CSS
  - *{}
  - padding: 0
  - margin: 0
  - box-sizing: border-box
- tạo thẻ div lớn chứa các thành phần chính: nên dùng class, có thể tên là main, app, ...
- tạo các thành phần chính: có thể dùng id

3. CSS cơ bản
- Câu hỏi: 
  - vị trí
  - kích thước
  - màu sắc
  - kiểu chữ
- làm từ ngoài vào trong, từ trên xuống dưới => cho tiện
- 