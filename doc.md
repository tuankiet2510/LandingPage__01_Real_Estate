Làm phần Neo header Neo phần chứa nabvar cách top 1 khoảng x px , khi kéo hết x px , phần chứa nav bar sẽ dính cứng trên top màn hình Dùng thuộc tính position sticky thay vì fixed vì fixed không được linh hoạt như sticky

Với sticky set top:0 khi kéo hết khoảng cách x px sẽ loại bỏ được khoảng không gian chiều cao x px Với fixed sẽ phải neo 1 khoảng từ navbar lên đỉnh => tốn nhiều không gian hơn

Vấn đề : Nếu thẻ cha được set height , khi cuộn thẻ con fixed quá thẻ cha , thẻ cha và thẻ con fixed sẽ biến mất ⇒ chỉ có thể neo được trong kích thước thẻ cha => Đưa thẻ nav ra khỏi header để ở main vì header có height 100vh , khi cuộn khỏi phần vh đầu tiền navbar cũng sẽ biến mất => Tạo fixed-header ở main chứa navbar , đổi tên header ban đầu thành hero'

Tạo favicon bằng favicon generator Tạo href cho các link tới các favicon Tại file manifest.json , sửa lại thành đường dẫn tuyệt đối "src":"\/android-icon-36x36.png" => "src":"/assets/img/favicon/android-icon-72x72.png"

## Responsive

Trên tablet & Mobile

### Header

- Giữ nguyên button sign in sign up , ẩn phần menu
- Đưa logo ra giữa , góc trái thêm 1 button 3 gạch ngang để click vào hiển thị menu
- Khi bấm vào logo sẽ có 1 overlay position fix nhìn xuyên qua chứa menu navbar nằm dọc dùng Drawer Menu (Menu trượt) bên trái. Bố cục nên như sau:

Tablet & Mobile:

Bên trái (Left): Đặt nút Toggle (Hamburger icon - 3 gạch). Khi bấm vào, menu sẽ trượt ra từ cạnh trái màn hình.

Ở giữa (Center) hoặc Bên phải (Right): Đặt Logo "Besnik.". (Thường ở Mobile, đặt Logo ở giữa nhìn sẽ cân đối hơn).

Bên phải (Right - Tùy chọn): Nếu còn chỗ (đặc biệt là Tablet), bạn có thể giữ lại nút "Sign Up" (nhỏ gọn) hoặc icon "User". Nếu không, hãy đưa toàn bộ "Sign In / Sign Up" vào bên trong Drawer Menu (thường đặt ở dưới cùng của menu trượt).

### Hero

A. Giao diện Mobile (Điện thoại) Trên mobile, màn hình hẹp và dài, chuyển từ bố cục ngang (Horizontal) sang bố cục dọc (Vertical/Stack).

Thứ tự sắp xếp (Order):

Info (Text + CTA) lên trên: Đây là quy tắc quan trọng "Content First". Người dùng cần đọc được tiêu đề ("Discover a place...") và biết trang web nói về gì ngay lập tức. Nếu để ảnh to lên trước, người dùng phải cuộn xuống mới thấy chữ, tỉ lệ thoát trang sẽ cao.

Hero-img xuống dưới: Ảnh minh họa sẽ nằm ngay dưới nút "More About Us".

Chi tiết căn chỉnh (Alignment):

Text: Nên chuyển sang Căn giữa (Center Align). Tiêu đề, đoạn mô tả và nút bấm nên nằm giữa màn hình để tạo sự cân đối trên thiết bị di động.

Button: Nút "More About Us" nên để chiều rộng lớn hơn (hoặc full-width có padding) để dễ bấm bằng ngón tay cái.

Image: Vì ảnh ngọn hải đăng khá cao, cân nhắc thu nhỏ tỉ lệ (scale down) một chút để người dùng vẫn nhìn thấy một phần của ảnh ngay khi vào trang mà không cần cuộn quá nhiều.
