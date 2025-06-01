# Báo cáo kiểm thử hiệu năng bằng JMeter

## Thông tin sinh viên

- Họ tên: Phạm Minh Hảo  
- MSSV: BIT220052  
- Website được kiểm thử: https://vnexpress.net

## Mô tả kịch bản kiểm thử

1. **Kịch bản 1: Cơ bản**
   - Số lượng người dùng: 10 + (52 % 10) = 12
   - Hành vi: Gửi yêu cầu GET đến trang chủ /
   - Loop Count: 5

2. **Kịch bản 2: Tải nặng**
   - Số lượng người dùng: 50 + (52 % 20) = 62
   - Ramp-up Period: 30 giây
   - Hành vi: Gửi yêu cầu GET đến / và /giai-tri

3. **Kịch bản 3: Tùy chỉnh**
   - Số lượng người dùng: 20 + (52 % 15) = 27
   - Thời gian chạy: 60 giây
   - Hành vi: Gửi yêu cầu GET đến /thoi-su và /the-gioi

## Kết quả kiểm thử

- **Kịch bản 1**:
  - Response Time trung bình: 360 ms
  - Throughput: 7 yêu cầu/giây
  - Error Rate: 0%

- **Kịch bản 2**:
  - Response Time trung bình: 744 ms
  - Throughput: 14.3 yêu cầu/giây
  - Error Rate: 0%

- **Kịch bản 3**:
  - Response Time trung bình: 324 ms
  - Throughput: 6.3 yêu cầu/giây
  - Error Rate: 0%

## Nhận xét

- Website phản hồi tương đối ổn định trong kịch bản cơ bản.
- Ở kịch bản tải nặng, có dấu hiệu tăng độ trễ khi số lượng người dùng tăng cao.
- Kịch bản tùy chỉnh chạy ổn định trong 60 giây, không có lỗi nghiêm trọng.
