                                                Bắt đầu

------------------------------------------------------------------------------------------------------------------
-- Cấu trúc file html
    -thẻ html chứa toàn bộ nội dung trang web, mỗi file html chỉ có 1 thẻ html
    -cấu trúc cơ bản sẽ có head và body
------------------------------------------------------------------------------------------------------------------

                                                Làm quen với html

-----------------------------------------------------------------------------------------------------------------
-- Các thẻ thông dụng
    h1 -> h6:(heading) các tiêu đề nhỏ dần
    p(paragraph): đoạn văn
    img: hình ảnh (src: source ảnh, alt: xử lí khi ảnh bị lỗi)
    a(anchor): link 1 liên kết tới trang khác
    ul(unordered list)/ol, li(list item) : hiển thị dạng danh sách
    table: bảng
        thead(table head): phần đầu bảng (thẻ <th> các cột)
        tbody(table body): phần thân (thẻ <tr> các dòng, hàng, chứa các thẻ <td> chứa thông tin tương ứng với các
                                                                                                    thẻ <th> )
    input: các ô nhập
            text: nhập text
            check box: chọn
            radio: chọn 1
    button: nút
    div: tạo một khối bao quanh các phân tử khác
    Attribute: thuộc tính của thẻ html và nằm trong thẻ mở
-----------------------------------------------------------------------------------------------------------------

                                                Làm quen với CSS

------------------------------------------------------------------------------------------------------------------
-- Sử dụng CSS trong HTML
3 cách:
    internal: bên trong => viết vào file html: sử dụng 1 cặp thẻ style
    external: viết file bên ngoài và link vào
    inline: viết trong 'thẻ mở' sử dụng attributes style
-----------------------------------------------------------------------------------------------------------------

 - ID và Class
    Sử dụng attribute ID để định danh thẻ, cấu hình css bằng #[ID]
    Sử dụng attribute Class để chỉ tới 1 lớp, cấu hình css bằng .[Class]
-----------------------------------------------------------------------------------------------------------------

-- CSS selector: chọn ra thẻ cần CSS theo mong muốn
.class1: chọn các thẻ có class1
.class1.class2: chọn các thẻ có cả class1 và class2
.class1 .class2: chọn thẻ có class2 và là con của thẻ có class1
*: chọn tất cả các thẻ
element (h1,h2,p,...): chọn các thẻ h1, h2,p, ...
elemet.class: chọn các thẻ có class này
element1, element2: chọn các thẻ có element1 và element2
element element: chọn các thẻ element1 nằm trong thẻ element2
element, class: chọn các thẻ element và class này
.class1 > .class2: class2 là "con trực tiếp" của class1
.class1 + .class2: class2 nằm "ngay đằng sau" class1
.class1 ~ .class2: class2 nằm "sau" thẻ class1
-----------------------------------------------------------------------------------------------------------------

-- Độ ưu tiên
- internal/ external: gọi sau => mới hơn => được ưu tiên
1000 - inline: 
100  - #id:
10   - .class:
1    - tag:
=>nhiểu điểm hơn thì được ưu tiên hơn
     - equal specificity: khi mà cùng cách gọi thì cái nào mới hơn => được chọn
                     khi mà sử dụng cả ID hoặc class để gọi hoặc ... thì số điểm cộng cho nhau
0    - universal selector anh inherited: phổ cập(universal): sử dụng thẻ *{} để tạo thuộc tính cho tất cả các thẻ
                                         kế thừa(inherited): thừa hưởng thuộc tính
max  - !important: được ưu tiên nhất, có thể sử dụng cho cả inline                                            
----------------------------------------------------------------------------------------------------------------- 

-- sử dụng biến trong CSS
    --[tên biến]: thuộc tính vd color, font, font-size,...
- dùng :root => sử dụng trong toàn file css
- khi không dùng root mà chỉ khai báo bth ví dụ
h1{
    --[tên biến]: ... 
}
=> chỉ sử dụng được trong h1
- để sử dụng biến: dùng var
h1{
    color: var(--[tên biến])
}
-----------------------------------------------------------------------------------------------------------------

-- các đơn vị sử dụng trong CSS (CSS units)
- sử dụng để tùy chỉnh kích thước các đối tượng hiển thị trên web
- 2 nhóm: tuyệt đối (absolute units) và tương đối (relative units)
- absolute units
    - px, pt, cm, mm, inch, pc
- relative units
    - %: phụ thuộc vào thẻ chứ nó ví dụ thẻ body, ...
    - rem: phụ thuộc vào kích thước của thuộc tính đó trong thẻ HTML (ví dụ đang sử dụng thuộc tính font-size thì
     nó sẽ phụ thuộc vào thuộc tính font size trong thẻ html)
    - em: phụ thuộc vào kích thước của thuộc tính đó trong thẻ gần nhất thẻ gần nhất
    - viewport: vw và vh: w - width, h - height: phụ thuộc vào kích thước màn hình (chiếm bao nhiêu phần của màn hình)
-----------------------------------------------------------------------------------------------------------------

-- thuộc tính margin
- thuộc tính này thường được đặt sẵn là 8px trên các trình duyệt vì vậy gây nên các khoảng trắng giữa các thẻ,
- để reset lại thuộc tính này ta dùng cú pháp như sau: sử dụng * selector vì nó tác động lên mọi thẻ
*{
    margin: 0;
}
- tương tự như vậy với thuộc tính padding
-----------------------------------------------------------------------------------------------------------------

-- Sử dụng % với height
- % phụ thuộc vào thuộc tính đó được khai báo ở thẻ cha, tức là khi thẻ con đặt height = 50% thì height thẻ con sẽ
phụ thuộc vào thẻ cha, thế nhưng, khi thẻ cha không có height thì % sẽ không có tác dụng, ngoài ra, khi thẻ cha có 
height = auto (tức là độ cao sẽ thay đổi tùy theo nội dung bên trong, khi nội dung tăng thì nó tăng, giảm thìu nó 
sẽ giảm theo) thì thẻ con cũng sẽ có thuộc tính height = auto chứ không bằng %.
- khi thuộc tính height không được khai báo cũng có nghĩa là thuộc tính đó là auto
------------------------------------------------------------------------------------------------------------------

-- Sử dụng rem
- rem là giá trị phụ thuộc vào thuộc tính đó được khai báo trong thẻ html, ví dụ như font-size: 1rem, font-size được
mặc định ở trong thẻ HTML là 16px thì 1rem lúc nào là 16px, 2rem là 32px.
- khi giá trị của thuộc tính trong thẻ html bị thay đổi thì các giá trị của thuộc tính đó được khai báo bằng rem cũng
sẽ thay đổi theo.
=> nên sử dụng rem cho font-size: khi gia giảm thì chỉ cẩn thay đổi ở 1 nơi đó là tại thẻ html còn nếu sử dụng px thì
khi cần thay đổi sẽ phải thay đổi ở nhiều nơi gây mất thời gian, bất tiện. Có thể sử dụng % như là một mẹo của rem vì
100% cũng là 1 rem.
------------------------------------------------------------------------------------------------------------------

-- một số hàm CSS
  - hàm rgb(): trộn màu
  ex: brackground: rgb(0,0,0)
  - hàm rgba(): trộng màu nhưng có thể nhìn xuyên qua xuống layer dưới
  - hàm calc(): tính toán (có thể cộng giá trị tương đối và tuyệt đối)
  - hàm attr(): lấy giá trị của attribute.
  ex: href = ...com.vn
  => content: "("attr(href)")" thì content = ...com.vn
------------------------------------------------------------------------------------------------------------------

-- CSS pseudo classes: lớp giả
(cấu trúc :+[tên])
    -:root: cặp thẻ HTML
    -:hover: chỉ được kích hoạt khi di chuột lên
    -:active: chỉ được kích hoạt khi bấm chuột vào
    -:first-child: select đứa con đầu tiên
    -:last-child: select đứa con cuối cùng
------------------------------------------------------------------------------------------------------------------

-- CSS pseudo elements: phần tử giả
(before và after luôn sử dụng với content)
    -:before và :after => before sẽ luôn đứng trước các thẻ và after luôn đứng sau
    ex: sử dụng after
    .container::after{
        content: "";
        display: block; //khai báo dạng block
        width: 150px;
        height: 100px;
        background-color: yellow;
    }
    -:first-letter => css chữ đầu tiên
    -:first-line => css dòng đầu tiên (dùng <br/> để xuống dòng trong đoạn văn bản)
    -:selection => css khi được chọn vào (bôi đen)
------------------------------------------------------------------------------------------------------------------

                                                Đệm - viền - lề

------------------------------------------------------------------------------------------------------------------
-- padding (lớp đệm) trong CSS
    - nằm ngay bên ngoài lớp content
    - có thể cấu hình (đệm thêm, chêm thêm) bằng cách padding-top/bottom/right/left: 10px ...
    - có thể thêm vào cả 4 hướng như sau: padding: 10px (vào 1 giá trị)
    - có thể thêm vào trên, dưới và trái phải như sau: padding: 10px 10px (vào 2 giá trị)
    - có thể thêm vào như sau: padding: 10px 12px 8px => bên trên, trái - phải và bên dưới (3 giá trị)
    - có thể thêm cả 4 bằng cách: padding: 10px 11px 12px 13px (trên, phải, dưới, trái (kim đồng hồ)) (4 giá trị)
------------------------------------------------------------------------------------------------------------------

-- border (đường viền) trong css
    - lớp viền ngoài cùng ôm một element (kí hiệu nét liền) => nằm ngay bên ngoài padding
    - có thể cấu hình độ dày (border-width, border-top-width: giống như padding), kiểu (border-style), màu (border-color)

=> cả padding và border đều tăng tổng kích thước của element lên
    - viết gọn lại: border: 10px solid #333
    - viết gọn lại nhưng chỉ xét 1 hướng: border-top: ...
------------------------------------------------------------------------------------------------------------------

-- margin (lề) trong css
    - có tác dụng tạo ra khoảng cách giữa 2 element
    - cú pháp giống như padding.
------------------------------------------------------------------------------------------------------------------

-- thuộc tính box-sizing
    - giúp rút ngắn thời gian chỉnh sửa
    - box-sizing: border-box
    - hoạt động: chiều ngang = kích thước content + padding + border, từ đó tựu động tính toán
------------------------------------------------------------------------------------------------------------------

                                                Thuộc tính tạo nền

------------------------------------------------------------------------------------------------------------------

-- thuộc tính background-image
    - background-image: url()
    - background-size: => có thuộc tính lặp lại => nếu độ lớn k đủ thì sẽ lặp lại ảnh => dùng 100% => chiều ngang 100%
    và chiều dọc tự động, auto auto : có thể bị tràn
    => để không bị lặp => background-repeat: no-repeat;

    - để sử dụng nhiều hình ảnh để làm nền => background-image: url(), url() => ảnh nào viết trước thì nằm trên
    - thuộc tính linear-gradient() => tạo ra dài màu chuyển đều đặn
    - có thể kết hợp dải màu chuyển và hình ảnh qua dải màu trong suốt: rgba()
    - có thể dùng tính chất lặp lại để tạo ra các giao diện đẹp bằng các hình ảnh lặp lại
    - lặp lại theo chiều dọc: repeat-y, lặp lại theo chiều ngang: repeat-x
------------------------------------------------------------------------------------------------------------------

-- thuộc tính background-size với cover và contain
    - contain: lấy kích thước dài nhất max(dài, ngang) mà đảm bảo không bị che khuất => có thể bị hở ra khoảng trắng
    - cover: lấy kích thước dài nhất max(dài, ngang) mà không quan tâm có bị che khuất hay không => không chấp nhận
    bị hở ra khoảng trắng
------------------------------------------------------------------------------------------------------------------

-- thuộc tính background-origin
    - xác định ảnh đổ vào từ lớp nào => hiểu là ảnh bao gồm các lớp nào
        - background-origin: padding-box => ảnh bao gồm từ lớp padding và content, tương tự với border box và content box
------------------------------------------------------------------------------------------------------------------

-- thuộc tính background-position
    - giúp tùy chỉnh vị trí hình ảnh nền trong CSS
    - các giá trị: top right => dính sang bên trên, phải, tương tự với dưới trái, ...
                   center => căn giữa => 50px => cách lề 50px và căn giữa
                   kết hợp: top 20px right 20px => cách trên 20px và phải 20px
                   20px 50px: cách theo chiều ngang và chiều dọc => có thể coi điểm góc màn hình trên bên trái là điểm gốc O
                   trong trục tọa độ Oxy từ đó tinh chỉnh 
------------------------------------------------------------------------------------------------------------------

-- cú pháp shorthand cho background
    - có thể gộp tất cả img, repeat, size, origin trong background:
    backgound: url() no-repeat center/contain => phải sử dụng chéo phải ở trước thuộc tính background-size
------------------------------------------------------------------------------------------------------------------

                                Thuộc tính vị trí

------------------------------------------------------------------------------------------------------------------                   

-- CSS position relative: thuộc tính tương đối
    - phụ thuộc vào chính nó, lấy chính vị trí đang đứng làm gốc tọa độ
    VD: h1{
        position: ralative; => vị trí đang đứng làm gốc
        top: 100px; => cách vị trí ban đầu 100px về phía dưới
    }
------------------------------------------------------------------------------------------------------------------

-- CSS position absolute: thuộc tính vị trí tuyệt đối
    - phụ thuộc vào thẻ cha gần nhất có thuộc tính position và chọn đó làm gốc tọa độ
------------------------------------------------------------------------------------------------------------------

-- CSS position fixed: 
    - dùng để cấu hình header/thông báo/... di chuyển theo lăn chuột => đứng yên trên màn hình
    - gắn với trên cùng, dưới cùng: top: 0; bottom: 0;
------------------------------------------------------------------------------------------------------------------

-- CSS position sticky:
    - bình thường có thể nằm ở 1 vị trí tùy chỉnh nhưng khi kéo tới vị trí đó thì có thể di chuyển
    - không hỗ trợ trên IE và trên Opera mini
------------------------------------------------------------------------------------------------------------------

                                Tricks and tips

------------------------------------------------------------------------------------------------------------------

-- Các cách căn giữa trong CSS
    - theo chiều ngang: text-align: center => có tính thừa kế (cha có thì con có)
    - theo chiều dọc: line-height: px => chỉnh thuộc tính này có chiều cao bằng thẻ cha thì nó sẽ căn giữa
    => có thể dùng biến để ko phải sửa nhiều
    VD: box{
        --height: 100px;
        height: var(--height);
    }
    h1{
        line-height: var(--height);
    }
    - display: flex ở thẻ cha, margin: auto ở thẻ con => căn giữa các item
    - align-items: center => căn giữa theo chiều cao
    - justify-content: center => căn giữa theo chiều cao, nhiều item nhưng liên nhau
                        space - between => cách nhau ra
    - sử dụng position:
    .box{
        position: relative;
    }
    h1{
        position: absolute;
        top: 50%; => cách top 50% chiều cao thẻ cha là thẻ box, nên sử dụng % để tiện nếu thay đổi chiều của thẻ cha
        transform: translateY(-50%); => vì cách như vậy không bao gồm cỡ chữ => lố xuống 1 đoạn => dùng 
                    translateY để dịch lên 1 đoạn bằng 50% kích cỡ bản thân content.
    }

------------------------------------------------------------------------------------------------------------------

-- ảnh dự phòng:
    - nên đặt vào trong src code.
    - sử dụng:
    cho thẻ img
    <img oneerror= "this.src = '...'" src = " " > => oneerror: khi mà có lỗi
    cho background
    div{
        background: url(),url() no-repeat /100%
    }
    => khi mà url đầu bị lỗi thì url thứ 2 sẽ hiển thị