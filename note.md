# class grid
- width: 1200px // Đối với những thẻ có class grid sẽ có chiều dài 1200px
- max-width: 100% // Đối với những thẻ có kích thước nhỏ hơn 1200px thì max-width sẽ giảm kích thước của grid xuống bằng với kích thước của màn hình

# Thẻ Span
- Sinh ra chỉ để có thể CSS cho 1 thằng khác

# Căn giữa
- margin: 0 auto // Tự động căn giữa khối với này khi nằm trong khối khác

- Căn giữa thẻ h3 thì dùng line-height bằng với chiều cao của thẻ chứa h3

- text-align: center // Nó sẽ căn giữa chữ bên trong thẻ đó
    // text-align: center / không có nghĩa là nó chỉ căn text không

- Căn giữa sử dụng thuộc tính flex
    // sử dụng display: flex cho thẻ cha
    // set margin: auto cho thẻ con muốn căn giữa

- Căn phải icon: có thể sử dụng text-align: right 

/*Căn giữa icon bằng transform*/
    position: absolute;
    content: "";
    top: 50%;
    left: 4px;
    border: 4px solid;
    transform: translateY(calc(-50% - 1px));
    border-color: transparent transparent transparent var(--primary-color);


# grid__row
- những thẻ nằm tong class này sẽ nằm trên cùng 1 hàng ngang

# Bem
- Block Element Modifier(những phần tử con thuộc khối và modifier bổ sung cho phần tử con)

# Dựng khung web
    // background-image: linear-gradient(0, color.., color..) Dải màu chuyển làm header
    // separate (phân cách)
        - ::after(Làm dấu gạch)
        - Sau thẻ li 
            1. top: 50% của thể li
            2. transform: translateY(-50%); // trừ 50% kích thước chiều cao của chính nó
    // Đối với các thẻ hover có thuộc tính transform
    transform: translateY(-1px); / sẽ dịch lên trên 1px

# Cách xử lí image đối với hình quá lớn và chỉ nhìn thấy có 1 góc của image
// Đối với image được sử dụng bằng style inline thì cách xử lí :
    ->  padding-top: 100%; 
        background-repeat: no-repeat;
        background-size: cover; 
        background-position: center;

        or background-size: contain; // đối với ảnh nhỏ

# Nhúng Font icons
// :hover // rgba(255,255,255, .7) [màu xám]

# CSS not cursor pointer
// cursor: text
// cursor: default / hình con trỏ chuột

# Note Thẻ img
// Nếu thẻ img để trực tiếp sử dụng display: flex thì thẻ img thành flex-item(khi đó ảnh sẽ bị méo)

# First-child / Last-child
- CSS cho 2 item trong cùng một thẻ với 2 attribute khác nhau ta sử dụng first child / last child cho thẻ chứa nó.

# Pesudo element
// ::before
// ::after

# Keyframes
// Animation: cho phép tạo ra những chuyển động animation 
    // ease: chuyển động từ từ
    // ease-in: chậm rồi nhanh
// Transform: scale()
    // Độ phóng to thu nhỏ

// Thuộc tính định được tâm của việc transform
    // transform-origin (https://developer.mozilla.org/en-US/docs/Web/CSS/transform-origin)
    // Tâm sẽ dịch chuyển theo trục X

// Animation phải cho vào thẻ con chứa các item muốn hiển thị kiểu animation, chứ không phải thẻ cha của nó

# Animation
- Khai báo will-change: opacity, transform // giúp tối ưu chuyển động của thẻ chứa animation hơn
# visibility
- Với thuộc tính hidden: ẩn đi layout những vẫn còn tồn tại ở đó

# Tổ hợp phím
- shift + alt + ->

# object-fit
- Có tính chất giống background-size

# base modal 
// Cách để tạo 1 modal
    1. Cần 1 lớp modal để chiếm hết màn hình 
    2. Cần 1 lớp overlay để có thể phủ mờ mờ nhìn xuyên qua 

// overlay: là 1 lớp phủ màu đen

// Để modal chiếm hết màn hình dùng position: fixed

// Trong trường hợp này lấy position: absolute cho modal__overlay được hiểu là con của modal, lấy modal làm gốc tọa độ chính(để làm lớp phủ overlay)
    .modal{
        position: fixed;
        top: 0;
        right: 0;
        bottom: 0;
        left: 0;
        display: flex;
    }

    .modal__overlay{
        position: absolute;
        width: 100%;
        height: 100%;
        background-color: rgba(0, 0, 0, .4)
    }

# Color rgba
// Màu nhìn xuyên được là màu rgba
// transparent: màu trong suốt

# Z-index
- Thẻ nào có thuộc tính z-index cao nhất thì thẻ đó nằm ở vị trí cao nhất 

# Cách tạo thẻ input 
 
- policy: chính sách

// Sử dụng 1 lớp giả để focus vào thẻ input làm lúc ấn vào sẽ đổi màu viền của thẻ input đó
    // .auth-form__input:focus {
            border-color: #888;
        }


# Bỏ viền border
// outline: none

# min-width
// Chiều dài tối thiểu 
// Đặt thuộc tính này cho thẻ và nếu có chữ ở trong thì khi sau này nếu chữ có dài ra thì không bị lỗi

# Css two button cách xa nhau ra
// Dịch sang trái sử dụng FLex 
    // justify-content: flex-end

# CSS màu cho thẻ svg
// Sử dụng fill color

# Tư duy làm header__search
// Không cần đo chiều dài của thanh search là bởi vì logo shoppe đã có chiều dài cố định và shopee cart có chiều dài cố định thì khi đó thannh search sẽ kế thừa chiều dài còn lại 

// Ta chỉ việc thêm flex: 1 (Để nó có thể co dãn chiều dài lúc thêm shopee cart)

// Flex: 1 / Chính là flex-row: 1 nó sẽ kế thừa chiều ngang theo trục man axis / flex: 1 không đảm nhiệm việc tăng kích thước của trục cross axis
    //height: 100% / Chiều dọc cross axis nên không kế thừa chiều dọc
    // .header__search-input-wrap{
        flex: 1;
        height: 100%;
    }

# Thẻ li chọc ra ngoài thẻ ul ta sử dụng
// 1.overflow: hidden
// 2. Sử dụng pesudo element
    first-child, last-child
# Cách tạo cầu nối( sử dụng lớp giả) / pesudo element
// after / before
// Ex:
        .header__search-option::after{
            content: "";
            display: block;
            width: 100%;
            height: 10px;
            background-color: red;
            position: absolute;
            top: -10px;
            left: 0;
        }

// /*======Create arrow======*/
    / Ex: Nút nhọn
            .header__cart-list::after{
                content: "";
                position: absolute;
                right: 3px;
                top: -26px;
                border-width: 16px 20px;
                border-style: solid;
                border-color: transparent transparent var(--white-color) 
            }

# Lớp giả 
// CSS cho phần tử thứ n
    :nth-child(..)
    Ex: CSS cho thằng con thứ 2 -> :nth-child(2)

# set width của 1 hình ảnh
// Cho 1 thẻ div bao thẻ img và 1 class cho img, khi đó ta set width: 100% cho class img thì nó sẽ nằm gọn trong thẻ đó

# Color(xuyên qua)
// rgba(0, 0, 0, .2) / box-shadow

# Fix error padding 
// Nếu 1 thẻ không ăn thuộc tính padding thì có thể là do thẻ chưa có display: block or inline-block

# Hover
// Khi hover vào user thì hiện ra menu
// Hover vào thẻ cha để hiện ra thẻ con
    .header__navbar-user:hover .header__navbar-user-menu{
        display: block;
    }

# Note logo link
// Đối với những trình duyệt cũ thì khi bỏ logo vào thẻ a thì thường có xuất hiện gạch chân 

# Dịch sang phải của trang
// home-filter__page 
    margin-left: auto;

# Làm chuyển động / transition
// transition: right linear 0.1s;

// Để khai báo trình duyệt tối ưu animation transform, ta có thuộc tính will-change: transform 

# Xử lí thẻ h có chữ quá dài / cách để cắt dòng
    overflow: hidden;
    display: block;
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-line-clamp: 2;

# Độ ưu tiên đối với những thẻ không ghi đè được 
// Ex: 
    i.home-product-item__like-icon-fill{
        display: none;
    }


# Hiện thanh scroll
// cart-list: giới hạn chiều cao
              set overflow-y: auto
/*========== Responsive ===========*/
# Size of one column
// 8.33333333%
100/12 * cột

# Column luôn luôn nằm trong row

# Làm ô tìm kiếm dùng thẻ label

# transition (-delay ,-duration ,-timing...) để khai báo animation sẽ hoạt động như thế nào (linear ,easer-in, easer-out...)

# Muốn hiển thị 5 sản phẩm trên cùng 1 hàng ngang ở trên mobile
12 cột chia cho 5 sản phẩm : 12/5 = 2.4 thì 1 cột có tỉ lệ 2.4%