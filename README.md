# Phân loại chiều cao sản phẩm sử dụng vi điều khiển PIC16F887
1. Giới thiệu dự án
- Dự án nhằm xây dựng một hệ thống tự động phân loại sản phẩm dựa trên chiều cao, sử dụng vi điều khiển PIC16F887 làm bộ não trung tâm.
- Hệ thống này có thể được ứng dụng trong các nhà máy sản xuất để tự động hóa quá trình phân loại sản phẩm, tăng năng suất và giảm thiểu lỗi của con người.
2. Cấu trúc dự án
-Vi điều khiển PIC16F887: Điều khiển toàn bộ quá trình hoạt động của hệ thống.
- Cảm biến tiệm cận PNP/NPN: Phát tín hiệu cho servo hoạt động khi có sản phẩm lướt qua cảm biến, đồng thời cập nhật giá trị của chúng.
- Động cơ servo SG90: Kích hoạt khi cảm biến nhận tín hiệu để gạt sản phẩm.
- Màn hình LCD 20x4 : Hiển thị thông tin về số lượng sản phẩm đã được phân loại.
- Nguồn tổ ong 110V + hạ áp: Cung cấp điện năng cho toàn bộ hệ thống.
![image](https://github.com/user-attachments/assets/1fba2bcc-f680-4758-b27e-d01cf3ad7fb5)
3. Nguyên lý hoạt động
- Sản phẩm di chuyển trên băng tải và đi qua các cảm biến.
- Cảm biến có trên 3 mức chiều cao của sản phẩm và gửi tín hiệu về vi điều khiển.
- Vi điều khiển xử lý tín hiệu, xác định loại sản phẩm và điều khiển động cơ tương ứng để đưa sản phẩm đến vị trí phân loại.
- Màn hình LCD hiển thị số lượng sản phẩm đã được phân loại theo từng loại.
![image](https://github.com/user-attachments/assets/2ebaf696-33c3-4001-8040-bb610bc14f41)
4. Chương trình chính
- Chương trình chính có tên "TEST_LCD_SERVO_DONE" nằm bên trên, được viết bằng ngôn ngữ C dựa trên trình biên dịch MPLAB XC8 Complier.
5. Kết quả đạt được
  
  Kết quả thử nghiệm cho thấy hệ thống phân loại sản phẩm đạt được độ chính xác trung bình 90%. Tuy nhiên, vẫn còn một số yếu tố ảnh hưởng đến độ ổn định của hệ thống, bao gồm:
- Tốc độ băng tải: Tốc độ băng tải hiện tại chưa được tối ưu, dẫn đến tình trạng sản phẩm chồng chéo, gây khó khăn cho cảm biến trong việc xác định chiều cao.
- Thời gian phản hồi của servo: Thời gian servo di chuyển để đưa sản phẩm đến vị trí phân loại chưa đủ nhanh, đặc biệt khi có nhiều sản phẩm cần xử lý liên tiếp.
- Chương trình chính: Chương trình chưa có cơ chế ngắt ngoài linh hoạt để xử lý các tình huống bất thường, ví dụ như khi có quá nhiều sản phẩm cùng lúc.


