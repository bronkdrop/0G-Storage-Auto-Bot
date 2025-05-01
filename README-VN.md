Here is the complete **Vietnamese translation** of your updated README, including the "Last updated" section:

---

# 0G Storage Auto Bot

Bot tự động tương tác với Mạng Lưu Trữ 0G để tối đa hóa tiềm năng nhận airdrop.

## Tổng Quan

Công cụ này tự động hóa quá trình tải lên các tệp ngẫu nhiên lên Mạng Lưu Trữ 0G trên Galileo Testnet. Nó giúp người dùng tham gia các hoạt động của testnet, từ đó có thể mang lại cơ hội nhận airdrop trong tương lai.

## Tính Năng

- **Hỗ Trợ Nhiều Ví**: Thực hiện tác vụ lần lượt với nhiều khóa riêng
- **Tích Hợp Proxy**: Sử dụng proxy xoay vòng để tránh giới hạn tốc độ
- **Luân Phiên User-Agent**: Tự động thay đổi user agent cho mỗi yêu cầu
- **Thống Kê Chi Tiết**: Theo dõi các thao tác thành công và thất bại
- **Lịch Sử Giao Dịch**: Lưu lại tất cả thông tin giao dịch để tham khảo sau

## Cài Đặt

```bash
# Clone kho lưu trữ
git clone https://github.com/bronkdrop/0G-Storage-Auto-Bot.git

# Di chuyển vào thư mục
cd 0G-Storage-Auto-Bot

# Cài đặt các phụ thuộc
npm install
```

## Cấu Hình

1. Tạo tệp `.env` trong thư mục gốc chứa các khóa riêng của bạn:

```
# Cho một ví
PRIVATE_KEY=your_private_key_here

# HOẶC cho nhiều ví
PRIVATE_KEY_1=your_first_private_key
PRIVATE_KEY_2=your_second_private_key
PRIVATE_KEY_3=your_third_private_key
```

2. (Tùy chọn) Tạo tệp `proxies.txt` với mỗi proxy trên một dòng:

```
http://username:password@ip:port
http://ip:port
socks5://username:password@ip:port
```

## Cách Sử Dụng

Chạy bot bằng lệnh:

```bash
node index.js
```

Khi được yêu cầu, hãy nhập số lượng tệp bạn muốn tải lên cho mỗi ví.

## Cách Hoạt Động

1. Bot tải các khóa riêng và proxy của bạn
2. Với mỗi ví:
   - Tải hình ảnh ngẫu nhiên
   - Tính toán hash và chuẩn bị dữ liệu
   - Tải các phân đoạn tệp lên indexer của 0G
   - Gửi giao dịch blockchain để đăng ký tệp tải lên
   - Chờ xác nhận trước khi tiếp tục lần tải tiếp theo
3. Kết quả được lưu trong thư mục `results`

## Khắc Phục Sự Cố

- **Lỗi Gas**: Đảm bảo ví của bạn có đủ token testnet 0G
- **Sự Cố Mạng**: Kiểm tra kết nối internet hoặc thử sử dụng proxy
- **Lỗi RPC**: RPC của testnet có thể đang bị quá tải, hãy thử lại sau

## Tuyên Bố Miễn Trừ Trách Nhiệm

Công cụ này chỉ dành cho mục đích giáo dục và tham gia testnet. Việc sử dụng bot không đảm bảo bạn sẽ nhận được bất kỳ airdrop nào trong tương lai. Hãy luôn sử dụng các công cụ testnet một cách có trách nhiệm.

## Giấy Phép

MIT
