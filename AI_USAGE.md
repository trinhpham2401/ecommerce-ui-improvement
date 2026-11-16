# AI Usage Log

## 1. Công cụ AI
- **Tên công cụ:** Google Gemini 

## 2. Mục đích sử dụng
- Hỗ trợ lên ý tưởng bố cục (layout) cho khu vực "Thẻ sản phẩm" trên giao diện điện thoại.
- Hỗ trợ viết khung mã nguồn HTML5 cơ bản và chia lưới (Grid/Flexbox) bằng CSS3 để tiết kiệm thời gian gõ code lặp lại.

## 3. Prompt đã sử dụng
- **Prompt 1 (Lên phương án):** "Tôi đang thực hiện bài tập phát triển giao diện website thương mại điện tử bằng HTML5 và CSS3. Tôi muốn cải tiến khu vực: Thẻ sản phẩm trên màn hình điện thoại. Đối tượng sử dụng: khách hàng mua sắm trực tuyến tại Việt Nam. Hãy đề xuất: 1. Bố cục giao diện, 2. Các thành phần HTML cần sử dụng, 3. Cách tổ chức CSS, 4. Cách hiển thị trên PC và Mobile. Trước tiên, hãy giải thích phương án thiết kế."
- **Prompt 2 (Tạo code):** "Dựa trên phương án đã thống nhất, hãy tạo mã HTML5 và CSS3. Yêu cầu: Có 4 sản phẩm mẫu (gồm ảnh, tên, giá, nút mua). Cấu trúc HTML rõ ràng, CSS tách file riêng. Thiết kế hiển thị 4 cột trên PC và 2 cột trên Mobile. Không dùng backend, không dùng thư viện ngoài."

## 4. Kết quả AI đề xuất
- AI đã tạo thành công cấu trúc file `index.html` với thẻ `<div class="product-card">` bọc ngoài mỗi sản phẩm.
- AI đã tạo file `style.css` sử dụng `display: grid;` để chia cột thành công (Responsive tốt trên màn hình nhỏ). 
- Tuy nhiên, phần thiết kế chi tiết chưa sát thực tế: Nút "Mua ngay" do AI sinh ra mang class `.btn-buy` có màu nền xanh dương (`blue`) và kích thước khá nhỏ, không phù hợp với nhận diện thương hiệu màu đen tối giản của Coolmate và khó bấm trên điện thoại.

## 5. Kiểm tra và điều chỉnh
- **Kiểm tra:** Tôi đã mở file `index.html` trên trình duyệt Chrome, sử dụng công cụ **Chrome DevTools (F12)**, bật chế độ **Device Toolbar** để giả lập màn hình iPhone 12 và kiểm tra lỗi UI/UX.
- **Điều chỉnh:** 
  1. Tôi đã xóa bỏ các thẻ `<p>` chứa đoạn text mô tả dài dòng do AI tự bịa ra để làm thẻ sản phẩm gọn lại.
  2. Thay link ảnh placeholder mặc định của AI bằng ảnh sản phẩm thực tế của Coolmate.
  3. Viết lại toàn bộ đoạn CSS cho nút bấm `.btn-buy` để giải quyết vấn đề khó thao tác trên Mobile.

## 6. Phần tôi hiểu và có thể giải thích
Tôi hiểu rõ cấu trúc chia lưới (Grid Layout) của file và đã trực tiếp can thiệp sửa đổi các thuộc tính CSS. Dưới đây là giải trình cho đoạn code tôi đã tự viết lại:

**Code ban đầu của AI:**
```css
.btn-buy {
  background-color: blue; 
  color: white;
  padding: 8px 15px;
}
