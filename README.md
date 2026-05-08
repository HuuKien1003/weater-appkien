Flutter Weather Application – Lab 4
👨‍🎓 Thông Tin Sinh Viên
Họ và tên: Hồ LÊ Hữu Kiên
MSSV: 2224802010285
🎬 Video Demo & Thuyết Trình

🔗 Link Drive báo cáo:
Xem Video Demo

Video bao gồm phần giới thiệu cấu trúc project, giải thích source code và demo các chức năng chính của ứng dụng khi chạy trên thiết bị thực tế.

📱 Tổng Quan Dự Án

Ứng dụng Flutter Weather App được xây dựng nhằm phục vụ yêu cầu của bài Lab 4 với mục tiêu tạo ra một ứng dụng dự báo thời tiết hiện đại, trực quan và hoạt động ổn định trên nền tảng Flutter.

Ứng dụng sử dụng dữ liệu thời tiết thời gian thực thông qua API từ OpenWeatherMap, đồng thời hỗ trợ:

Lấy vị trí hiện tại bằng GPS
Hiển thị thông tin thời tiết theo khu vực
Cache dữ liệu offline
Tối ưu trải nghiệm người dùng khi mất kết nối mạng
🗂️ Kiến Trúc & Tổ Chức Source Code

Project được chia thành nhiều module riêng biệt để dễ quản lý và mở rộng:

lib/models/

Chứa các model dùng để ánh xạ dữ liệu JSON từ API sang object Dart.

lib/services/

Xử lý các tác vụ liên quan đến dữ liệu và hệ thống:

weather_service.dart → Gọi API thời tiết
location_service.dart → Lấy tọa độ GPS và xin quyền truy cập vị trí
storage_service.dart → Lưu cache bằng SharedPreferences
lib/providers/

Quản lý trạng thái ứng dụng bằng Provider giúp UI cập nhật dữ liệu linh hoạt.

lib/screens/

Chứa các màn hình chính:

Home Screen
Search Screen
Forecast Screen
lib/widgets/

Bao gồm các widget tái sử dụng:

Current Weather Card
Hourly Forecast
Weather Detail Item
Search Bar
...
📦 Các Package Được Sử Dụng

Một số thư viện chính được tích hợp trong project:

provider → Quản lý state hiệu quả
http → Kết nối và lấy dữ liệu từ REST API
geolocator & geocoding → Hỗ trợ GPS và xử lý địa chỉ
shared_preferences → Lưu dữ liệu cục bộ
flutter_dotenv → Ẩn API Key và tăng tính bảo mật khi upload source code
⚙️ Hướng Dẫn Chạy Ứng Dụng

Để chạy project thành công, thực hiện các bước sau:

Clone source code về máy
Đảm bảo đã cài Flutter SDK
Đổi tên file:
.env.example ➜ .env
Thêm API Key vào file .env:
OPENWEATHER_API_KEY=186fe3b5f726d7ea6086929a26a9af0c
Cài dependencies:
flutter pub get
Khởi chạy ứng dụng:
flutter run
