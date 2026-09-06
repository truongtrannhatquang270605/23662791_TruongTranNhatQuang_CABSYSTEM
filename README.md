# 23662791_TruongTranNhatQuang_CABSYSTEM
**Danh sách Stakeholders (Các bên liên quan) - Nền tảng đặt xe CAB**

| Tên | Vai trò |
| :--- | :--- |
| **Ban lãnh đạo / Ban giám đốc** | Người ra quyết định chiến lược và đầu tư nền tảng. Có nhu cầu xem các báo cáo tổng quan (doanh thu, số lượng chuyến, tỷ lệ hoàn thành/hủy, hiệu suất) và định hướng mở rộng hệ thống trong tương lai. |
| **Khách hàng** | Người dùng cuối sử dụng hệ thống để đăng ký/đăng nhập, tạo yêu cầu đặt xe, theo dõi hành trình, thanh toán cước phí và đánh giá tài xế sau chuyến đi. |
| **Tài xế** | Đối tác cung cấp dịch vụ vận chuyển. Sử dụng ứng dụng để nhận/từ chối yêu cầu đặt xe, chia sẻ vị trí liên tục và cập nhật các trạng thái của chuyến đi (đã đến, đã đón khách, hoàn thành). |
| **Nhân viên vận hành** | Quản lý dữ liệu hệ thống (khách hàng, tài xế, phương tiện). Giám sát các chuyến đi đang diễn ra, hỗ trợ xử lý ngoại lệ/lỗi và tra cứu lịch sử giao dịch thông qua phân quyền. |
| **Business Analyst (BA)** | Người phân tích và thiết kế hệ thống. Chịu trách nhiệm xác định phạm vi, quy trình nghiệp vụ, các trường hợp ngoại lệ và làm rõ các quy tắc nghiệp vụ chưa chốt (tính cước, tiêu chí ưu tiên, chính sách hủy) với các bên liên quan. |
| **Nhóm phát triển (Development Team)** | Chịu trách nhiệm thiết kế kiến trúc kỹ thuật linh hoạt, độc lập, có khả năng mở rộng cao và lập trình xây dựng nền tảng CAB dựa trên các yêu cầu đã được phân tích. |
| **Nhà cung cấp cổng thanh toán (Bên thứ 3)** | Đối tác xử lý các giao dịch thanh toán điện tử, đảm bảo tính bảo mật và toàn vẹn của dữ liệu thẻ/tài khoản mà không lưu trữ trực tiếp trên CAB. |
| **Nhà cung cấp dịch vụ thông báo (Bên thứ 3)** | Hệ thống bên ngoài hỗ trợ gửi các cập nhật thời gian thực (trạng thái chuyến đi, thanh toán) tới thiết bị của khách hàng và tài xế. |

**Ma trận Stakeholder (Power/Interest Grid) - Nền tảng CAB**

| | Mức độ quan tâm thấp (Low Interest) | Mức độ quan tâm cao (High Interest) |
| :--- | :--- | :--- |
| **Quyền lực cao<br>(High Power)** | **Giữ hài lòng (Keep Satisfied)**<br>• Nhà cung cấp cổng thanh toán<br>• Nhà cung cấp dịch vụ thông báo | **Quản lý chặt chẽ (Manage Closely)**<br>• Ban lãnh đạo / Ban giám đốc<br>• Nhóm phát triển (Development Team)<br>• Business Analyst (BA) |
| **Quyền lực thấp<br>(Low Power)** | **Theo dõi (Monitor)**<br>*(Hiện chưa có đối tượng nổi bật ở nhóm này trong phạm vi tài liệu)* | **Cung cấp thông tin (Keep Informed)**<br>• Khách hàng<br>• Tài xế<br>• Nhân viên vận hành |

**Chi tiết chiến lược tiếp cận từng nhóm:**

* **Quản lý chặt chẽ (High Power - High Interest):** Đây là nhóm quyết định sự thành bại của dự án. Ban lãnh đạo cần duyệt yêu cầu, ngân sách và theo dõi tiến độ. BA và Dev Team là nòng cốt thực thi, cần tương tác liên tục, họp bàn giao và giải quyết vấn đề kỹ thuật/nghiệp vụ hàng ngày.
* **Giữ hài lòng (High Power - Low Interest):** Các đối tác cung cấp API (thanh toán, thông báo) không quan tâm nhiều đến chiến lược kinh doanh của CAB, nhưng hệ thống phụ thuộc hoàn toàn vào dịch vụ của họ. Cần tuân thủ đúng tài liệu kỹ thuật (guidelines) của họ và duy trì kết nối ổn định.
* **Cung cấp thông tin (Low Power - High Interest):** Khách hàng, tài xế và nhân viên vận hành bị ảnh hưởng trực tiếp bởi hệ thống mới nhưng không có quyền quyết định tính năng. Cần thu thập ý kiến, đào tạo sử dụng và cập nhật thông báo rõ ràng cho họ khi hệ thống ra mắt.
* **Theo dõi (Low Power - Low Interest):** Giám sát tối thiểu. Trong tương lai có thể là các cơ quan quản lý giao thông địa phương nếu họ yêu cầu báo cáo định kỳ nhưng chưa có tác động trực tiếp ở giai đoạn hiện tại.
