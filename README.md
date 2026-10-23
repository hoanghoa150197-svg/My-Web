# My Web Ecosystem — Dark Navy PWA

Bản đổi giao diện từ `index.html` do người dùng cung cấp. Giữ nguyên JavaScript quản lý ứng dụng, danh mục, tìm kiếm, import/export JSON và khóa `localStorage` `my-web-ecosystem-v1`.

## Triển khai GitHub Pages

1. Giải nén ZIP và tải **các file bên trong** lên thư mục gốc repository.
2. Vào Settings → Pages → Deploy from a branch → main / (root).
3. Mở URL GitHub Pages bằng HTTPS. Khi cập nhật, ghi đè các file cũ, nhất là `sw.js`.
4. Nếu giao diện chưa đổi, đóng và mở lại ứng dụng hoặc tải lại trang khi có mạng.

## Cài đặt

- Android/Chrome: menu → Install app / Add to Home screen.
- iPhone/Safari: Share → Add to Home Screen.
- Máy tính/Chrome/Edge: biểu tượng cài đặt trên thanh địa chỉ (nếu được hỗ trợ).

## Dữ liệu và ngoại tuyến

Dữ liệu ứng dụng lưu tại `localStorage` theo **origin và đường dẫn website hiện tại**; việc thay URL hoặc xóa dữ liệu trình duyệt có thể làm mất dữ liệu. Nên dùng Sao lưu JSON thường xuyên, đặc biệt trước khi thay đổi repo/domain. Nhập JSON sẽ **thay thế** dữ liệu hiện tại. Service Worker cache giao diện và các tài nguyên cùng website để mở ngoại tuyến sau lần tải đầu tiên. Các website bên ngoài mà thẻ ứng dụng liên kết đến **không được cache** và thường cần Internet. Không có đồng bộ giữa các thiết bị.
