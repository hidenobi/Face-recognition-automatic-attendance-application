# Face-recognition-automatic-attendance-application

## Mục lục
1. Mô tả chung
2. Quy trình hoạt động
3. Các tính năng bổ sung



## 1. Mô tả chung:

Mục tiêu: Xây dựng một ứng dụng điểm danh tự động bằng cách sử dụng công nghệ nhận diện khuôn mặt. Ứng dụng sẽ sử dụng camera để chụp ảnh người dùng, sau đó so sánh với cơ sở dữ liệu khuôn mặt đã được lưu trữ để xác định danh tính và thực hiện việc điểm danh.
Công nghệ:
YOLO: Sử dụng để phát hiện khuôn mặt trong hình ảnh.
FaceNet: Trích xuất các đặc trưng đặc trưng của khuôn mặt (embedding) để so sánh với cơ sở dữ liệu.
TensorFlow: Framework để xây dựng và huấn luyện các mô hình deep learning.
TensorFlow Lite: Chuyển đổi mô hình sang định dạng nhẹ để triển khai trên các thiết bị di động.
## 2. Quy trình hoạt động:

### 2.1. Thu thập dữ liệu:
Chuẩn bị một dataset gồm các hình ảnh khuôn mặt của từng người cần điểm danh. Mỗi người cần có nhiều hình ảnh ở các góc độ, ánh sáng khác nhau để đảm bảo độ chính xác.
Huấn luyện mô hình:
YOLO: Huấn luyện mô hình YOLO để phát hiện khuôn mặt trong hình ảnh.
FaceNet: Huấn luyện mô hình FaceNet để trích xuất các đặc trưng khuôn mặt.
### 2.2. Xây dựng ứng dụng:
Sử dụng TensorFlow để xây dựng một ứng dụng (ví dụ bằng Python) kết hợp cả YOLO và FaceNet.
Khi ứng dụng chạy, camera sẽ liên tục chụp ảnh.
YOLO sẽ phát hiện các khuôn mặt trong hình ảnh.
FaceNet sẽ trích xuất đặc trưng của khuôn mặt đã phát hiện và so sánh với cơ sở dữ liệu.
Nếu tìm thấy một khuôn mặt khớp, ứng dụng sẽ hiển thị tên của người đó và ghi nhận thông tin điểm danh.
### 2.3. Chuyển đổi sang TFLite:
Chuyển đổi mô hình YOLO và FaceNet đã huấn luyện sang định dạng TensorFlow Lite để tối ưu hóa cho các thiết bị di động.
Triển khai ứng dụng:
Nhúng mô hình TFLite vào một ứng dụng di động (ví dụ Android, iOS) để chạy trên điện thoại.
## 3. Các tính năng bổ sung:

Xác thực: Sử dụng jwt để xác thực
Quản lý cơ sở dữ liệu: Xây dựng một cơ sở dữ liệu để lưu trữ thông tin về người dùng, lịch sử điểm danh, v.v.
Giao diện người dùng: Thiết kế một giao diện người dùng thân thiện để người dùng dễ dàng sử dụng.
Thông báo: Gửi thông báo khi có người điểm danh hoặc khi xảy ra lỗi.
Tính năng báo cáo: Tạo các báo cáo thống kê về việc điểm danh.
## 4. Thử nghiệm và đánh giá:

Đánh giá độ chính xác: Đánh giá độ chính xác của mô hình trên một tập dữ liệu kiểm thử.
Đánh giá tốc độ: Đo thời gian thực hiện của ứng dụng để đảm bảo đáp ứng được yêu cầu về thời gian thực.
Tối ưu hóa: Điều chỉnh các hyperparameter của mô hình và tối ưu hóa code để cải thiện hiệu suất.
## 5. Các vấn đề cần lưu ý:

Chất lượng dữ liệu: Chất lượng dữ liệu huấn luyện ảnh hưởng rất lớn đến hiệu suất của mô hình.
Ánh sáng: Ánh sáng ảnh hưởng đến việc nhận diện khuôn mặt. Cần thiết kế hệ thống chiếu sáng phù hợp.
Góc chụp: Khuôn mặt cần được chụp ở góc vuông với camera để đảm bảo độ chính xác.
Khẩu trang: Nếu yêu cầu điểm danh trong điều kiện có khẩu trang, cần điều chỉnh mô hình hoặc sử dụng các kỹ thuật đặc biệt.
Các công cụ và thư viện hỗ trợ:

TensorFlow/Keras: Để xây dựng và huấn luyện mô hình.
OpenCV: Để xử lý hình ảnh.
MobileNetSSD: Một mô hình phát hiện khuôn mặt nhẹ, có thể thay thế cho YOLO.
Scikit-learn: Để xây dựng các mô hình máy học khác.
