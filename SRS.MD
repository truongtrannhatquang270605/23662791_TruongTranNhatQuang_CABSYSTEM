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

**Biểu đồ Ma trận Stakeholder (Mermaid Quadrant Chart)**

```mermaid
quadrantChart
    title Ma trận Stakeholder (Power/Interest) - Nền tảng CAB
    x-axis Mức độ quan tâm thấp --> Mức độ quan tâm cao
    y-axis Quyền lực thấp --> Quyền lực cao
    quadrant-1 Quản lý chặt chẽ
    quadrant-2 Giữ hài lòng
    quadrant-3 Theo dõi
    quadrant-4 Cung cấp thông tin
    Ban lãnh đạo: [0.85, 0.90]
    Business Analyst: [0.80, 0.80]
    Nhóm phát triển: [0.90, 0.75]
    Cổng thanh toán: [0.25, 0.85]
    Dịch vụ thông báo: [0.35, 0.75]
    Khách hàng: [0.90, 0.30]
    Tài xế: [0.85, 0.20]
    Nhân viên vận hành: [0.70, 0.35]
```

# Business Rules – CAB System MVP

## 1. Quy tắc tài khoản và phân quyền

| Mã | Business Rule |
|---|---|
| **BR-01** | Khách hàng và tài xế phải được xác thực trước khi sử dụng các chức năng yêu cầu tài khoản. |
| **BR-02** | Chỉ người dùng có quyền phù hợp mới được thực hiện các thao tác quản trị. |
| **BR-03** | Thông tin cá nhân của khách hàng và tài xế phải được bảo vệ. |

---

## 2. Quy tắc đặt xe

| Mã | Business Rule |
|---|---|
| **BR-04** | Một yêu cầu đặt xe phải có điểm đón, điểm đến và loại xe. |
| **BR-05** | Sau khi khách hàng gửi yêu cầu, hệ thống phải chuyển yêu cầu sang trạng thái tìm tài xế. |
| **BR-06** | Khách hàng phải được thông báo về trạng thái xử lý yêu cầu đặt xe. |

---

## 3. Quy tắc tìm và phân công tài xế

| Mã | Business Rule |
|---|---|
| **BR-07** | Hệ thống chỉ xem xét các tài xế đang ở trạng thái sẵn sàng nhận chuyến. |
| **BR-08** | Tài xế được lựa chọn phải phù hợp với loại xe mà khách hàng yêu cầu. |
| **BR-09** | Hệ thống phải ưu tiên tài xế phù hợp và gần điểm đón của khách hàng. |
| **BR-10** | Nếu tài xế được đề xuất không phản hồi hoặc từ chối chuyến, hệ thống phải tiếp tục tìm tài xế khác. |
| **BR-11** | Nếu không tìm được tài xế phù hợp, hệ thống phải thông báo cho khách hàng. |
| **BR-12** | Khi tài xế chấp nhận chuyến, hệ thống phải ghi nhận tài xế được phân công cho chuyến đó. |

---

## 4. Quy tắc thực hiện chuyến

| Mã | Business Rule |
|---|---|
| **BR-13** | Tài xế phải cập nhật trạng thái chuyến trong quá trình thực hiện. |
| **BR-14** | Các trạng thái chính của chuyến gồm: tìm tài xế, đã phân công tài xế, tài xế đến điểm đón, đã đón khách, đang di chuyển và hoàn thành. |
| **BR-15** | Khi chuyến hoàn thành, hệ thống phải ghi nhận thông tin chuyến để phục vụ tính cước, thanh toán và lưu lịch sử. |
| **BR-16** | Hệ thống phải lưu thông tin vị trí của tài xế để hỗ trợ tìm tài xế và dự kiến thời gian đến. |

---

## 5. Quy tắc tính cước và thanh toán

| Mã | Business Rule |
|---|---|
| **BR-17** | Sau khi chuyến hoàn thành, hệ thống phải xác định số tiền khách hàng phải trả dựa trên loại dịch vụ và thông tin chuyến đi. |
| **BR-18** | Khách hàng được phép thanh toán bằng tiền mặt hoặc phương thức thanh toán điện tử được hệ thống hỗ trợ. |
| **BR-19** | Thông tin nhạy cảm của thẻ hoặc tài khoản thanh toán không được lưu trực tiếp trong hệ thống CAB. |
| **BR-20** | Thanh toán điện tử phải được xử lý thông qua nhà cung cấp dịch vụ thanh toán bên ngoài. |
| **BR-21** | Khi thanh toán điện tử thất bại, hệ thống phải thông báo cho khách hàng và cho phép xử lý lại theo chính sách của doanh nghiệp. |

---

## 6. Quy tắc thông báo

| Mã | Business Rule |
|---|---|
| **BR-22** | Khách hàng phải được thông báo khi yêu cầu đặt xe được tiếp nhận. |
| **BR-23** | Khách hàng phải được thông báo khi tài xế nhận chuyến. |
| **BR-24** | Khách hàng phải được thông báo khi tài xế đến điểm đón. |
| **BR-25** | Khách hàng phải được thông báo khi chuyến xe hoàn thành và khi thanh toán có kết quả. |
| **BR-26** | Tài xế phải được thông báo khi có chuyến mới hoặc có thay đổi liên quan đến chuyến đang thực hiện. |

---

## 7. Quy tắc vận hành

| Mã | Business Rule |
|---|---|
| **BR-27** | Nhân viên vận hành được phép theo dõi các chuyến đang diễn ra và trạng thái tài xế theo quyền được cấp. |
| **BR-28** | Nhân viên vận hành được phép hỗ trợ xử lý các trường hợp chuyến bị lỗi theo chính sách của doanh nghiệp. |
| **BR-29** | Các thao tác quản trị quan trọng phải được lưu vết để phục vụ kiểm tra và xử lý sự cố. |

---

# Business Rules cần xác nhận

Các quy tắc dưới đây chưa được xác định cụ thể trong yêu cầu hiện tại. Cần trao đổi với khách hàng hoặc Ban giám đốc trước khi triển khai chính thức.

| Mã | Nội dung cần xác nhận |
|---|---|
| **BR-Q01** | Bán kính tối đa để hệ thống tìm kiếm tài xế là bao nhiêu? |
| **BR-Q02** | Tài xế có bao nhiêu thời gian để phản hồi yêu cầu chuyến? |
| **BR-Q03** | Sau khi tài xế từ chối hoặc không phản hồi, hệ thống chuyển sang tài xế tiếp theo sau bao lâu? |
| **BR-Q04** | Ngoài khoảng cách, hệ thống có tiêu chí nào khác để ưu tiên tài xế không? |
| **BR-Q05** | Công thức tính cước chuyến xe cụ thể là gì? |
| **BR-Q06** | Có áp dụng phụ phí theo thời điểm, quãng đường, loại xe hoặc điều kiện khác không? |
| **BR-Q07** | Khách hàng có được phép hủy chuyến không và có phát sinh phí hủy không? |
| **BR-Q08** | Nếu tài xế hủy chuyến sau khi đã nhận, hệ thống có tự động tìm tài xế khác không? |
| **BR-Q09** | Khi thanh toán điện tử thất bại, khách hàng được phép thanh toán lại bao nhiêu lần? |
| **BR-Q10** | Khi mất kết nối mạng hoặc GPS, hệ thống xử lý trạng thái chuyến và vị trí tài xế như thế nào? |

---

# Tổng kết Business Rules

| Loại | Số lượng | Phạm vi |
|---|---:|---|
| Business Rules chính thức | **29** | Sử dụng cho MVP |
| Business Rules cần xác nhận | **10** | Cần thống nhất với khách hàng |
| **Tổng cộng** | **39** | Bao gồm cả nội dung cần xác nhận |

> **Lưu ý:** BR-Q01 đến BR-Q10 chưa được xem là Business Rule chính thức của hệ thống. Sau khi khách hàng xác nhận, các nội dung này mới được chuẩn hóa thành Business Rule chính thức và đánh số lại nếu cần.

**Module Quản lý Khách hàng (MVP)**
* **Xác thực cơ bản:** Đăng ký và đăng nhập nhanh bằng số điện thoại.
* **Đặt xe (Luồng cốt lõi):** Cho phép nhập điểm đón và điểm đến qua API bản đồ; hệ thống hiển thị cước phí dự kiến dựa trên công thức tĩnh (tổng quãng đường x đơn giá).
* **Theo dõi hành trình:** Cập nhật theo thời gian thực 4 trạng thái chính yếu: Đang tìm tài xế $\rightarrow$ Tài xế đang đến $\rightarrow$ Đang di chuyển $\rightarrow$ Hoàn thành.
* **Thanh toán tối giản:** Triển khai thanh toán bằng tiền mặt (Cash) và tối đa một cổng thanh toán điện tử cơ bản để ghi nhận luồng tiền.
* **Ngoài phạm vi MVP (Out of scope):** Đánh giá tài xế, lưu địa chỉ yêu thích, mã khuyến mãi, phân hạng thành viên.

**Module Quản lý Tài xế (MVP)**
* **Quản lý hồ sơ tối giản:** Bỏ qua quy trình tự đăng ký phức tạp. Tài khoản tài xế có thể do nhân viên vận hành tạo và cấp quyền trực tiếp để nhanh chóng đưa vào hoạt động.
* **Cập nhật trạng thái làm việc:** Cung cấp duy nhất nút bật/tắt trạng thái sẵn sàng (Online/Offline) và liên tục gửi tọa độ GPS về hệ thống.
* **Thuật toán phân công (Dispatching) cơ bản:** Sử dụng cơ chế tìm kiếm theo bán kính địa lý gần nhất (ví dụ: quét các tài xế trống trong bán kính 2km) hoặc cơ chế Broadcast (phát đồng loạt). Bỏ qua hoàn toàn các tham số ưu tiên về tỷ lệ nhận chuyến, điểm đánh giá hay thâm niên.
* **Thực thi chuyến đi:** Giao diện thao tác một chạm để tài xế cập nhật luồng trạng thái: Chấp nhận chuyến $\rightarrow$ Đã đến điểm đón $\rightarrow$ Bắt đầu hành trình $\rightarrow$ Kết thúc chuyến.
* **Ngoài phạm vi MVP (Out of scope):** Điểm đánh giá (Rating), hệ thống thưởng/phạt (Penalty), ví nội bộ phức tạp, xem thống kê hiệu suất tài xế.

**Danh sách Yêu cầu Nghiệp vụ (Business Requirements) - Lựa chọn Xe & Tài xế (MVP)**

| Mã BR | Hạng mục | Mô tả yêu cầu cho giai đoạn MVP |
| :--- | :--- | :--- |
| **BR-01** | **Lựa chọn loại phương tiện cơ bản** | Khách hàng chỉ được cung cấp các tùy chọn phân loại xe thiết yếu nhất để đáp ứng nhu cầu vận chuyển (ví dụ: Xe 4 chỗ tiêu chuẩn, Xe 7 chỗ tiêu chuẩn). Hệ thống không xử lý các bộ lọc phức tạp (xe hạng sang, xe điện, xe ghép) nhằm đơn giản hóa công thức tính cước và logic tìm kiếm. |
| **BR-02** | **Cơ chế ghép nối tài xế tự động** | Để đảm bảo hệ thống vận hành trơn tru và nhanh chóng, khách hàng không tự lướt danh sách để chọn tài xế. Hệ thống sẽ tự động quét và chỉ định tài xế đang ở trạng thái "Sẵn sàng" có vị trí địa lý gần điểm đón nhất. |
| **BR-03** | **Hiển thị thông tin tài xế rút gọn** | Sau khi hệ thống ghép nối thành công, giao diện khách hàng chỉ hiển thị các thông tin định danh bắt buộc: Tên tài xế, số điện thoại, biển số xe và vị trí GPS trên bản đồ. Không thu thập, không tính toán và không hiển thị các dữ liệu đánh giá chất lượng (Rating, thâm niên, số huy hiệu). |
| **BR-04** | **Tự động xử lý luồng từ chối chuyến** | Nếu tài xế được hệ thống lựa chọn từ chối yêu cầu hoặc không phản hồi trong thời gian quy định (ví dụ: 15 giây), hệ thống tự động chuyển yêu cầu đặt xe tới tài xế gần thứ hai. Khách hàng không cần thao tác chọn lại xe hay tạo lại cuốc xe từ đầu. |

**B5: Yêu cầu Nghiệp vụ (Business Requirements) - Chức năng Lựa chọn Xe & Tài xế (Giai đoạn MVP)**

| Mã BR | Tên yêu cầu | Mô tả chi tiết (Theo tiêu chuẩn MVP) |
| :--- | :--- | :--- |
| **BR-01** | **Lựa chọn loại phương tiện (Vehicle Selection)** | Khách hàng được yêu cầu chọn loại dịch vụ/phương tiện cơ bản trước khi xác nhận đặt chuyến (ví dụ: CAB 4 chỗ, CAB 7 chỗ hoặc CAB Moto). Các bộ lọc nâng cao như xe hạng sang, xe tiện chuyến, hoặc yêu cầu tài xế nữ sẽ không đưa vào phạm vi MVP để tối giản hệ thống. |
| **BR-02** | **Cơ chế chỉ định tài xế tự động (Auto-Dispatching)** | Khách hàng không được chọn thủ công tài xế từ một danh sách. Để đảm bảo thời gian đáp ứng nhanh nhất, hệ thống tự động tìm kiếm và phân công tài xế đang ở trạng thái "Sẵn sàng" và có vị trí địa lý gần điểm đón nhất. |
| **BR-03** | **Cung cấp thông tin nhận diện (Driver/Vehicle Info)** | Khi hệ thống ghép nối thành công, màn hình ứng dụng của khách hàng chỉ hiển thị các thông tin định danh bắt buộc để nhận xe: Tên tài xế, Số điện thoại (để liên lạc), Biển số xe, Loại xe và Vị trí hiện tại trên bản đồ. Các thông tin về điểm đánh giá (Rating) hay số chuyến đã hoàn thành bị loại bỏ khỏi MVP. |
| **BR-04** | **Luồng tìm kiếm tài xế thay thế (Re-routing)** | Trong trường hợp tài xế được hệ thống chỉ định từ chối chuyến hoặc không phản hồi quá thời gian quy định (ví dụ 15-30 giây), hệ thống phải tự động lặp lại quá trình phân công cho tài xế gần thứ hai. Khách hàng chỉ thấy trạng thái "Đang tìm tài xế" và không phải thao tác đặt lại. |
| **BR-05** | **Thông báo hết xe (No Driver Available)** | Nếu hệ thống đã mở rộng bán kính tìm kiếm tối đa (theo quy định của doanh nghiệp) mà vẫn không có tài xế nào tiếp nhận, hệ thống phải thông báo rõ ràng cho khách hàng: "Hiện tại không có tài xế phù hợp, vui lòng thử lại sau" và kết thúc yêu cầu để giải phóng luồng xử lý. |

**Mô hình hóa quy trình nghiệp vụ (Business Process Model) - Luồng Đặt xe MVP**

**1. Bảng mô tả luồng quy trình (Process Flow Description)**

| Bước | Tác nhân | Thao tác / Xử lý | Mã BR đối chiếu |
| :--- | :--- | :--- | :--- |
| 1 | Khách hàng | Nhập điểm đón, điểm đến và lựa chọn loại phương tiện (4 chỗ, 7 chỗ...). | BR-01 |
| 2 | Hệ thống | Tính toán cước phí dự kiến dựa trên quãng đường và hiển thị cho khách hàng. | |
| 3 | Khách hàng | Xác nhận "Đặt xe". | |
| 4 | Hệ thống | Chuyển trạng thái "Đang tìm tài xế". Quét tọa độ GPS, xác định tài xế Online gần nhất phù hợp với loại xe. | BR-02 |
| 5 | Hệ thống | Gửi thông báo yêu cầu nhận chuyến đến Ứng dụng của Tài xế được chọn. | BR-02 |
| 6 | Tài xế | Nhận thông báo và có khoảng thời gian giới hạn (VD: 15s) để "Chấp nhận" hoặc "Từ chối". | |
| 7a | Hệ thống | **Ngoại lệ (Từ chối/Timeout):** Tự động bỏ qua tài xế hiện tại, lặp lại Bước 4 để tìm tài xế gần thứ 2. | BR-04 |
| 7b | Hệ thống | **Ngoại lệ (Hết xe):** Nếu vượt quá số lần quét hoặc giới hạn bán kính, gửi thông báo "Không có tài xế" cho khách và kết thúc luồng. | BR-05 |
| 8 | Hệ thống | **Luồng chính (Chấp nhận):** Khóa cuốc xe cho tài xế này. Gửi thông tin định danh (Tên, SĐT, Biển số, Loại xe) và vị trí tài xế sang cho Khách hàng. | BR-03 |
| 9 | Tài xế | Di chuyển đến điểm đón. Bấm xác nhận "Đã đến điểm đón" trên ứng dụng. | |
| 10 | Tài xế | Khách lên xe. Bấm xác nhận "Bắt đầu chuyến đi". | |
| 11 | Tài xế | Đến điểm trả khách. Bấm xác nhận "Hoàn thành chuyến đi". | |
| 12 | Hệ thống | Ghi nhận trạng thái hoàn thành. Hiển thị tổng tiền cần thanh toán cho cả Khách hàng và Tài xế để thực hiện giao dịch (tiền mặt/chuyển khoản). | |

---

**2. Sơ đồ luồng nghiệp vụ (BPMN / Flowchart bằng Mermaid)**

```mermaid
flowchart TD
    %% Tác nhân: Khách hàng (C), Hệ thống (S), Tài xế (D)
    Start([Khách hàng mở App]) --> C1(Nhập điểm đón, điểm đến)
    C1 --> C2(Chọn loại xe - BR-01)
    C2 --> S1(Hệ thống tính và hiển thị giá)
    S1 --> C3{Khách bấm Đặt xe?}
    C3 -- Hủy --> End1([Kết thúc])
    C3 -- Xác nhận --> S2(Hệ thống quét tài xế gần nhất - BR-02)
    
    S2 --> S3(Phát cuốc cho Tài xế 1)
    S3 --> D1{Tài xế phản hồi?}
    
    D1 -- Từ chối / Quá giờ --> S4{Còn tài xế trong bán kính?}
    S4 -- Còn --> S2_loop(Hệ thống quét tài xế gần thứ N - BR-04)
    S2_loop --> S3
    S4 -- Không còn --> S5(Thông báo hết xe - BR-05)
    S5 --> End2([Hủy cuốc tự động])
    
    D1 -- Chấp nhận --> S6(Ghép nối thành công. Hiển thị thông tin TX - BR-03)
    S6 --> D2(Tài xế di chuyển đến điểm đón)
    D2 --> D3(Tài xế xác nhận: Đã đến)
    D3 --> D4(Tài xế xác nhận: Bắt đầu chuyến)
    D4 --> D5(Tài xế xác nhận: Hoàn thành chuyến)
    D5 --> S7(Hệ thống ghi nhận hoàn thành & Tính cước cuối)
    S7 --> End3([Thanh toán & Kết thúc])
    
    %% Style
    classDef system fill:#f9f,stroke:#333,stroke-width:2px;
    class S1,S2,S2_loop,S3,S4,S5,S6,S7 system;

# Tài liệu Phân tích Nghiệp vụ (BA) - Nền tảng Đặt xe CAB (Giai đoạn MVP)

## 1. Danh sách Stakeholders (Các bên liên quan)

| Tên | Vai trò |
| :--- | :--- |
| **Ban lãnh đạo / Ban giám đốc** | Người ra quyết định chiến lược và đầu tư nền tảng. Có nhu cầu xem báo cáo tổng quan và định hướng mở rộng hệ thống. |
| **Khách hàng** | Người dùng cuối sử dụng hệ thống để tạo yêu cầu đặt xe, theo dõi hành trình và thanh toán cước phí. |
| **Tài xế** | Đối tác cung cấp dịch vụ vận chuyển. Sử dụng ứng dụng để nhận yêu cầu đặt xe, cập nhật trạng thái chuyến đi và chia sẻ vị trí. |
| **Nhân viên vận hành** | Quản lý dữ liệu hệ thống (khách hàng, tài xế, phương tiện). Giám sát các chuyến đi đang diễn ra và hỗ trợ xử lý ngoại lệ. |
| **Business Analyst (BA)** | Người phân tích và thiết kế hệ thống. Chịu trách nhiệm xác định phạm vi, quy trình nghiệp vụ và các yêu cầu chức năng/phi chức năng. |
| **Nhóm phát triển (Dev Team)** | Chịu trách nhiệm thiết kế kiến trúc kỹ thuật và lập trình xây dựng nền tảng CAB dựa trên các yêu cầu đã phân tích. |
| **Cổng thanh toán (Bên thứ 3)** | Đối tác xử lý các giao dịch thanh toán điện tử, đảm bảo tính bảo mật. |
| **Dịch vụ thông báo (Bên thứ 3)** | Hệ thống bên ngoài hỗ trợ gửi các cập nhật thời gian thực tới thiết bị của khách hàng và tài xế. |

---

## 2. Ma trận Stakeholder (Power/Interest Grid)

| | Mức độ quan tâm thấp (Low Interest) | Mức độ quan tâm cao (High Interest) |
| :--- | :--- | :--- |
| **Quyền lực cao<br>(High Power)** | **Giữ hài lòng (Keep Satisfied)**<br>• Cổng thanh toán<br>• Dịch vụ thông báo | **Quản lý chặt chẽ (Manage Closely)**<br>• Ban lãnh đạo / Ban giám đốc<br>• Nhóm phát triển (Dev Team)<br>• Business Analyst (BA) |
| **Quyền lực thấp<br>(Low Power)** | **Theo dõi (Monitor)**<br>*(Chưa có đối tượng nổi bật)* | **Cung cấp thông tin (Keep Informed)**<br>• Khách hàng<br>• Tài xế<br>• Nhân viên vận hành |

```mermaid
quadrantChart
    title Ma trận Stakeholder (Power/Interest) - Nền tảng CAB
    x-axis Mức độ quan tâm thấp --> Mức độ quan tâm cao
    y-axis Quyền lực thấp --> Quyền lực cao
    quadrant-1 Quản lý chặt chẽ
    quadrant-2 Giữ hài lòng
    quadrant-3 Theo dõi
    quadrant-4 Cung cấp thông tin
    Ban lãnh đạo: [0.85, 0.90]
    Business Analyst: [0.80, 0.80]
    Nhóm phát triển: [0.90, 0.75]
    Cổng thanh toán: [0.25, 0.85]
    Dịch vụ thông báo: [0.35, 0.75]
    Khách hàng: [0.90, 0.30]
    Tài xế: [0.85, 0.20]
    Nhân viên vận hành: [0.70, 0.35]

# Tài liệu Phân tích Nghiệp vụ (BA) - Nền tảng Đặt xe CAB (Giai đoạn MVP)

## 1. Danh sách Stakeholders (Các bên liên quan)

| Tên | Vai trò |
| :--- | :--- |
| **Ban lãnh đạo / Ban giám đốc** | Người ra quyết định chiến lược và đầu tư nền tảng. Có nhu cầu xem báo cáo tổng quan và định hướng mở rộng hệ thống. |
| **Khách hàng** | Người dùng cuối sử dụng hệ thống để tạo yêu cầu đặt xe, theo dõi hành trình và thanh toán cước phí. |
| **Tài xế** | Đối tác cung cấp dịch vụ vận chuyển. Sử dụng ứng dụng để nhận yêu cầu đặt xe, cập nhật trạng thái chuyến đi và chia sẻ vị trí. |
| **Nhân viên vận hành** | Quản lý dữ liệu hệ thống (khách hàng, tài xế, phương tiện). Giám sát các chuyến đi đang diễn ra và hỗ trợ xử lý ngoại lệ. |
| **Business Analyst (BA)** | Người phân tích và thiết kế hệ thống. Chịu trách nhiệm xác định phạm vi, quy trình nghiệp vụ và các yêu cầu chức năng/phi chức năng. |
| **Nhóm phát triển (Dev Team)** | Chịu trách nhiệm thiết kế kiến trúc kỹ thuật và lập trình xây dựng nền tảng CAB dựa trên các yêu cầu đã phân tích. |
| **Cổng thanh toán (Bên thứ 3)** | Đối tác xử lý các giao dịch thanh toán điện tử, đảm bảo tính bảo mật. |
| **Dịch vụ thông báo (Bên thứ 3)** | Hệ thống bên ngoài hỗ trợ gửi các cập nhật thời gian thực tới thiết bị của khách hàng và tài xế. |

---

Lỗi hiển thị trong ảnh của bạn xảy ra vì bảng Markdown bị tràn dòng hoặc các thẻ `<br>` bị dính liền làm hỏng cấu trúc cột. 

Dưới đây là phiên bản đã sửa lại định dạng bảng Markdown cho gọn gàng, không bị lỗi xuống dòng, kèm theo toàn bộ tài liệu chuẩn để bạn copy:

# Tài liệu Phân tích Nghiệp vụ (BA) - Nền tảng Đặt xe CAB (Giai đoạn MVP)

## 1. Danh sách Stakeholders (Các bên liên quan)

| Tên | Vai trò |
| :--- | :--- |
| **Ban lãnh đạo / Ban giám đốc** | Người ra quyết định chiến lược và đầu tư nền tảng. Có nhu cầu xem báo cáo tổng quan và định hướng mở rộng hệ thống. |
| **Khách hàng** | Người dùng cuối sử dụng hệ thống để tạo yêu cầu đặt xe, theo dõi hành trình và thanh toán cước phí. |
| **Tài xế** | Đối tác cung cấp dịch vụ vận chuyển. Sử dụng ứng dụng để nhận yêu cầu đặt xe, cập nhật trạng thái chuyến đi và chia sẻ vị trí. |
| **Nhân viên vận hành** | Quản lý dữ liệu hệ thống (khách hàng, tài xế, phương tiện). Giám sát các chuyến đi đang diễn ra và hỗ trợ xử lý ngoại lệ. |
| **Business Analyst (BA)** | Người phân tích và thiết kế hệ thống. Chịu trách nhiệm xác định phạm vi, quy trình nghiệp vụ và các yêu cầu chức năng/phi chức năng. |
| **Nhóm phát triển (Dev Team)** | Chịu trách nhiệm thiết kế kiến trúc kỹ thuật và lập trình xây dựng nền tảng CAB dựa trên các yêu cầu đã phân tích. |
| **Cổng thanh toán (Bên thứ 3)** | Đối tác xử lý các giao dịch thanh toán điện tử, đảm bảo tính bảo mật. |
| **Dịch vụ thông báo (Bên thứ 3)** | Hệ thống bên ngoài hỗ trợ gửi các cập nhật thời gian thực tới thiết bị của khách hàng và tài xế. |

---

## 2. Ma trận Stakeholder (Power/Interest Grid)

| Nhóm quyền lực / quan tâm | Mức độ quan tâm thấp (Low Interest) | Mức độ quan tâm cao (High Interest) |
| :--- | :--- | :--- |
| **Quyền lực cao (High Power)** | **Giữ hài lòng (Keep Satisfied)**<br>• Cổng thanh toán<br>• Dịch vụ thông báo | **Quản lý chặt chẽ (Manage Closely)**<br>• Ban lãnh đạo / Ban giám đốc<br>• Nhóm phát triển (Dev Team)<br>• Business Analyst (BA) |
| **Quyền lực thấp (Low Power)** | **Theo dõi (Monitor)**<br>• *(Chưa có đối tượng nổi bật)* | **Cung cấp thông tin (Keep Informed)**<br>• Khách hàng<br>• Tài xế<br>• Nhân viên vận hành |

```mermaid
quadrantChart
    title Ma trận Stakeholder (Power/Interest) - Nền tảng CAB
    x-axis Mức độ quan tâm thấp --> Mức độ quan tâm cao
    y-axis Quyền lực thấp --> Quyền lực cao
    quadrant-1 Quản lý chặt chẽ
    quadrant-2 Giữ hài lòng
    quadrant-3 Theo dõi
    quadrant-4 Cung cấp thông tin
    Ban lãnh đạo: [0.85, 0.90]
    Business Analyst: [0.80, 0.80]
    Nhóm phát triển: [0.90, 0.75]
    Cổng thanh toán: [0.25, 0.85]
    Dịch vụ thông báo: [0.35, 0.75]
    Khách hàng: [0.90, 0.30]
    Tài xế: [0.85, 0.20]
    Nhân viên vận hành: [0.70, 0.35]

# Yêu cầu Phi chức năng (Non-Functional Requirements - NFR) - Nền tảng CAB (Giai đoạn MVP)

Dựa trên bối cảnh và định hướng phát triển của doanh nghiệp, các yêu cầu phi chức năng dành cho giai đoạn MVP được quy định như sau:

## 1. Hiệu năng và Khả năng đáp ứng (Performance & Scalability)
* **NFR-01 (Thời gian phản hồi API):** Các thao tác tra cứu cơ bản, định vị bản đồ và gửi yêu cầu đặt xe phải phản hồi về giao diện ứng dụng trong vòng dưới 2 giây (điều kiện mạng 4G tiêu chuẩn).
* **NFR-02 (Tần suất cập nhật vị trí):** Tọa độ GPS của tài xế khi ở trạng thái Online phải được đồng bộ về máy chủ liên tục với tần suất 5 giây/lần để đảm bảo tính thời gian thực (real-time) cho việc điều phối.
* **NFR-03 (Khả năng mở rộng độc lập):** Kiến trúc hệ thống phía Backend phải được tách biệt thành các dịch vụ độc lập tối thiểu giữa module xử lý chuyến đi (Dispatching) và module thông báo, nhằm đảm bảo khi lượng truy cập tăng cao không làm sập toàn bộ hệ thống.

## 2. Tính sẵn sàng và Độ tin cậy (Availability & Reliability)
* **NFR-04 (Tính sẵn sàng của dịch vụ MVP):** Hệ thống cốt lõi (Khách hàng đặt xe và Tài xế nhận cuốc) phải đạt mức độ sẵn sàng tối thiểu 99% trong giờ cao điểm.
* **NFR-05 (Cơ chế chịu lỗi cô lập):** Lỗi phát sinh từ một dịch vụ bên thứ ba (ví dụ: mất kết nối cổng thanh toán điện tử hoặc dịch vụ gửi thông báo push notification) tuyệt đối không được làm gián đoạn luồng cốt lõi là tạo chuyến đi và phân công tài xế.

## 3. Bảo mật và An toàn dữ liệu (Security & Compliance)
* **NFR-06 (Mã hóa đường truyền):** Toàn bộ dữ liệu truyền tải giữa ứng dụng di động (Mobile App) và máy chủ (Server) phải được mã hóa bắt buộc thông qua giao thức HTTPS / TLS 1.3.
* **NFR-07 (Bảo mật thông tin thanh toán):** Đúng theo yêu cầu của doanh nghiệp, hệ thống CAB không được phép lưu trữ trực tiếp các thông tin nhạy cảm của thẻ ngân hàng hoặc tài khoản thanh toán điện tử trên cơ sở dữ liệu nội bộ; mọi giao dịch phải điều hướng qua bên thứ ba đạt chuẩn PCI-DSS.
* **NFR-08 (Xác thực và phân quyền):** Mọi phiên làm việc (Session) của khách hàng và tài xế phải thông qua token định danh bảo mật sau khi xác thực OTP thành công. Các thao tác can thiệp hệ thống từ nhân viên vận hành bắt buộc phải được ghi vết (audit log).

## 4. Khả năng bảo trì và Triển khai (Maintainability & Deployability)
* **NFR-09 (Triển khai từng phần):** Hệ thống phải cho phép nhóm phát triển cập nhật hoặc vá lỗi từng module riêng biệt (như module khách hàng hoặc module tài xế) mà không bắt buộc phải dừng toàn bộ hệ thống (Zero-downtime deployment cho các bản cập nhật nhỏ).
* **NFR-10 (Lưu trữ Nhật ký hệ thống - Logging):** Hệ thống phải ghi lại toàn bộ các sự kiện lỗi quan trọng (Error logs), lịch sử trạng thái chuyến đi và lịch sử phản hồi của tài xế trong cơ sở dữ liệu để phục vụ công tác tra cứu, giải quyết tranh chấp khi có sự cố phát sinh.

# Thiết kế Mô hình Thực thể Kết hợp (Entity Relationship Diagram - ERD) - Giai đoạn MVP

Dựa trên các Quy tắc Nghiệp vụ (BR) và Yêu cầu Chức năng (FR) đã xác định ở các phần trước cho nền tảng CAB (phiên bản MVP gồm Quản lý Khách hàng và Quản lý Tài xế), dưới đây là mô hình ERD với các thực thể cốt lõi, thuộc tính và mối quan hệ giữa chúng.

## 1. Danh sách các Thực thể (Entities) và Thuộc tính

### 1. Thực thể `Customer` (Khách hàng)
Lưu trữ thông tin định danh tối thiểu của khách hàng sử dụng dịch vụ.
*   `customer_id` (PK): Mã định danh khách hàng (UUID / Long).
*   `phone_number`: Số điện thoại khách hàng (Dùng để xác thực OTP).
*   `status`: Trạng thái tài khoản (Active, Blocked).
*   `created_at`: Thời điểm đăng ký tài khoản.

### 2. Thực thể `Driver` (Tài xế)
Lưu trữ thông tin hồ sơ và trạng thái hoạt động của đối tác tài xế.
*   `driver_id` (PK): Mã định danh tài xế.
*   `phone_number`: Số điện thoại tài xế (Dùng để nhận OTP và liên lạc).
*   `name`: Tên tài xế.
*   `online_status`: Trạng thái làm việc hiện tại (Online / Offline) (Liên quan FR-D01).
*   `current_latitude`: Vĩ độ GPS hiện tại của tài xế (Cập nhật realtime).
*   `current_longitude`: Kinh độ GPS hiện tại của tài xế (Cập nhật realtime).
*   `status`: Trạng thái tài khoản được duyệt bởi nhân viên vận hành (Pending, Active, Locked).

### 3. Thực thể `Vehicle` (Phương tiện)
Lưu trữ thông tin xe của tài xế phục vụ cho việc phân loại chuyến đi.
*   `vehicle_id` (PK): Mã định danh phương tiện.
*   `driver_id` (FK): Khóa ngoại liên kết tới tài xế sở hữu.
*   `vehicle_type`: Loại phương tiện cơ bản theo BR-01 (VD: `CAR_4_SEATS`, `CAR_7_SEATS`).
*   `license_plate`: Biển số xe (Dùng để khách hàng nhận diện).

### 4. Thực thể `Trip` (Chuyến đi / Cuốc xe)
Thực thể trung tâm lưu trữ toàn bộ vòng đời của một yêu cầu đặt xe từ lúc tạo đến khi hoàn thành.
*   `trip_id` (PK): Mã định danh cuốc xe.
*   `customer_id` (FK): Khách hàng tạo yêu cầu.
*   `driver_id` (FK, Nullable): Tài xế nhận cuốc (Có thể trống nếu chưa tìm được hoặc hủy).
*   `pickup_latitude`: Tọa độ vĩ độ điểm đón.
*   `pickup_longitude`: Tọa độ kinh độ điểm đón.
*   `dropoff_latitude`: Tọa độ vĩ độ điểm đến.
*   `dropoff_longitude`: Tọa độ kinh độ điểm đến.
*   `vehicle_type_requested`: Loại xe khách hàng yêu cầu.
*   `estimated_fare`: Số tiền cước phí dự kiến (Tính theo công thức tĩnh).
*   `status`: Trạng thái chuyến đi (Values: `FINDING`, `DRIVER_ARRIVING`, `IN_PROGRESS`, `COMPLETED`, `CANCELLED`).
*   `created_at`: Thời gian tạo yêu cầu đặt xe.
*   `completed_at`: Thời gian kết thúc chuyến đi.

---

## 2. Mô tả Quan hệ giữa các Thực thể (Relationships)

| Thực thể A | Mối quan hệ (Cardinality) | Thực thể B | Mô tả ý nghĩa liên kết |
| :--- | :---: | :--- | :--- |
| **Customer** | `1 : N` | **Trip** | Một khách hàng có thể tạo nhiều chuyến đi trong lịch sử, nhưng một chuyến đi thuộc về duy nhất một khách hàng. |
| **Driver** | `1 : 1` | **Vehicle** | Ở giai đoạn MVP tối giản, mỗi tài xế quản lý và gắn liền với duy nhất một phương tiện hoạt động. |
| **Driver** | `1 : N` | **Trip** | Một tài xế có thể thực hiện nhiều chuyến đi qua các thời điểm khác nhau, nhưng tại một thời điểm (một `Trip` đang chạy), chuyến đi chỉ được gán cho một tài xế duy nhất. |

---

## 3. Sơ đồ ERD (Biểu đồ thực thể kết hợp bằng Mermaid)

```mermaid
erDiagram
    CUSTOMER ||--o{ TRIP : creates
    DRIVER ||--|{ VEHICLE : owns
    DRIVER ||--o{ TRIP : executes

    CUSTOMER {
        string customer_id PK
        string phone_number
        string status
        datetime created_at
    }

    DRIVER {
        string driver_id PK
        string phone_number
        string name
        string online_status
        float current_latitude
        float current_longitude
        string status
    }

    VEHICLE {
        string vehicle_id PK
        string driver_id FK
        string vehicle_type
        string license_plate
    }

    TRIP {
        string trip_id PK
        string customer_id FK
        string driver_id FK
        float pickup_latitude
        float pickup_longitude
        float dropoff_latitude
        float dropoff_longitude
        string vehicle_type_requested
        float estimated_fare
        string status
        datetime created_at
        datetime completed_at
    }

# Thiết kế Sơ đồ Use Case (Use Case Diagram & Description) - Nền tảng CAB (Giai đoạn MVP)

Dựa trên phạm vi MVP đã xác định (gồm Module Khách hàng, Module Tài xế và Hệ thống trung tâm tự động hóa), dưới đây là mô hình Use Case bao gồm tác nhân, sơ đồ tổng quan và đặc tả chi tiết cho các chức năng cốt lõi.

## 1. Xác định Tác nhân (Actors) và Use Case trong MVP

| Tác nhân | Các Use Case chính trong MVP |
| :--- | :--- |
| **Khách hàng (Customer)** | • Đăng ký / Đăng nhập tài khoản (qua OTP)<br>• Nhập điểm đón / điểm đến & chọn loại xe<br>• Gửi yêu cầu đặt xe<br>• Theo dõi trạng thái & vị trí tài xế chuyến đi |
| **Tài xế (Driver)** | • Cập nhật trạng thái hoạt động (Online / Offline)<br>• Nhận thông báo cuốc xe mới<br>• Phản hồi cuốc xe (Chấp nhận / Từ chối)<br>• Cập nhật luồng trạng thái chuyến đi (Đã đến điểm đón, Bắt đầu, Hoàn thành) |
| **Hệ thống (System / Backend)** | • Thuật toán tự động quét và phân công tài xế gần nhất<br>• Xơ chế tự động chuyển cuốc (Re-routing) khi tài xế từ chối/hết giờ<br>• Tính toán cước phí dự kiến tĩnh<br>• Quản lý phiên chuyến đi và ghi logs |

---

## 2. Sơ đồ Use Case tổng quan (Diagram bằng Mermaid)

```mermaid
usecaseDiagram
    actor KhachHang as "Khách hàng"
    actor TaiXe as "Tài xế"
    actor HeThong as "Hệ thống (Backend)"

    rectangle "Hệ thống Nền tảng CAB - MVP" {
        usecase "Đăng nhập / Xác thực OTP" as UC1
        usecase "Đặt xe (Nhập điểm & Chọn loại xe)" as UC2
        usecase "Theo dõi hành trình chuyến đi" as UC3
        
        usecase "Cập nhật trạng thái Online/Offline" as UC4
        usecase "Nhận và phản hồi cuốc xe" as UC5
        usecase "Cập nhật tiến trình chuyến đi" as UC6
        
        usecase "Tự động phân công tài xế (Auto-Dispatch)" as UC7
        usecase "Tự động điều phối thay thế (Re-routing)" as UC8
        usecase "Tính cước & Quản lý phiên" as UC9
    }

# Thiết kế Sơ đồ Use Case (Use Case Diagram & Description) - Nền tảng CAB (Giai đoạn MVP)

Dựa trên phạm vi MVP đã xác định (gồm Module Khách hàng, Module Tài xế và Hệ thống trung tâm tự động hóa), dưới đây là mô hình Use Case bao gồm tác nhân, sơ đồ tổng quan và đặc tả chi tiết cho các chức năng cốt lõi.

## 1. Xác định Tác nhân (Actors) và Use Case trong MVP

| Tác nhân | Các Use Case chính trong MVP |
| :--- | :--- |
| **Khách hàng (Customer)** | • Đăng ký / Đăng nhập tài khoản (qua OTP)<br>• Nhập điểm đón / điểm đến & chọn loại xe<br>• Gửi yêu cầu đặt xe<br>• Theo dõi trạng thái & vị trí tài xế chuyến đi |
| **Tài xế (Driver)** | • Cập nhật trạng thái hoạt động (Online / Offline)<br>• Nhận thông báo cuốc xe mới<br>• Phản hồi cuốc xe (Chấp nhận / Từ chối)<br>• Cập nhật luồng trạng thái chuyến đi (Đã đến điểm đón, Bắt đầu, Hoàn thành) |
| **Hệ thống (System / Backend)** | • Thuật toán tự động quét và phân công tài xế gần nhất<br>• Xơ chế tự động chuyển cuốc (Re-routing) khi tài xế từ chối/hết giờ<br>• Tính toán cước phí dự kiến tĩnh<br>• Quản lý phiên chuyến đi và ghi logs |

---

## 2. Sơ đồ Use Case tổng quan (Diagram bằng Mermaid)

```mermaid
usecaseDiagram
    actor KhachHang as "Khách hàng"
    actor TaiXe as "Tài xế"
    actor HeThong as "Hệ thống (Backend)"

    rectangle "Hệ thống Nền tảng CAB - MVP" {
        usecase "Đăng nhập / Xác thực OTP" as UC1
        usecase "Đặt xe (Nhập điểm & Chọn loại xe)" as UC2
        usecase "Theo dõi hành trình chuyến đi" as UC3
        
        usecase "Cập nhật trạng thái Online/Offline" as UC4
        usecase "Nhận và phản hồi cuốc xe" as UC5
        usecase "Cập nhật tiến trình chuyến đi" as UC6
        
        usecase "Tự động phân công tài xế (Auto-Dispatch)" as UC7
        usecase "Tự động điều phối thay thế (Re-routing)" as UC8
        usecase "Tính cước & Quản lý phiên" as UC9
    }

    KhachHang --> UC1
    KhachHang --> UC2
    KhachHang --> UC3

    TaiXe --> UC1
    TaiXe --> UC4
    TaiXe --> UC5
    TaiXe --> UC6

    UC2 -.-> UC7 : <<include>>
    UC5 -.-> UC8 : <<extend>>
    UC2 -.-> UC9 : <<include>>
    UC6 -.-> UC9 : <<include>>

# Tiêu chí Chấp nhận (Acceptance Criteria - AC) cho các Yêu cầu Chức năng (FR) - MVP

Dựa trên các Yêu cầu Chức năng (FR) đã xây dựng cho giai đoạn MVP của nền tảng CAB, dưới đây là các Tiêu chí Chấp nhận (Acceptance Criteria) cụ thể theo chuẩn **BDD (Behavior-Driven Development)** với định dạng `Given - When - Then` để đội ngũ phát triển và kiểm thử (QA) tiến hành nghiệm thu.

---

## 1. Tiêu chí Chấp nhận cho Module Khách hàng (Customer App)

### FR-C01: Xác thực tài khoản (OTP)
* **AC-01.1 (Gửi mã OTP thành công):**
  * **Given** Khách hàng đang ở màn hình đăng nhập và nhập số điện thoại hợp lệ.
  * **When** Khách hàng nhấn nút "Nhận mã OTP".
  * **Then** Hệ thống phải gửi mã xác thực thành công về số điện thoại đó và hiển thị màn hình nhập OTP kèm đồng hồ đếm ngược 60 giây.
* **AC-01.2 (Xác thực OTP hợp lệ):**
  * **Given** Khách hàng đã nhập mã OTP gồm 6 chữ số do hệ thống cung cấp.
  * **When** Khách hàng bấm nút "Xác nhận".
  * **Then** Hệ thống cho phép đăng nhập thành công, lưu phiên làm việc (Session) và chuyển hướng khách hàng vào màn hình chính (Trang đặt xe).

### FR-C02 & FR-C03: Nhập vị trí, Chọn loại xe và Báo giá
* **AC-02.1 (Hiển thị cước phí dự kiến):**
  * **Given** Khách hàng đã nhập đầy đủ địa chỉ điểm đón và điểm đến trên bản đồ.
  * **When** Khách hàng chọn một loại phương tiện cụ thể (VD: CAB 4 chỗ).
  * **Then** Hệ thống phải hiển thị chính xác cước phí dự kiến tính theo công thức tĩnh (Khoảng cách $\times$ Đơn giá chuẩn) và nút "Đặt xe" được kích hoạt.

### FR-C04 & FR-C05: Gửi yêu cầu và Theo dõi trạng thái
* **AC-04.1 (Chuyển trạng thái khi đặt xe):**
  * **Given** Khách hàng đã chọn loại xe và thấy giá tiền dự kiến.
  * **When** Khách hàng bấm nút "Đặt xe".
  * **Then** Giao diện phải lập tức chuyển sang màn hình "Đang tìm tài xế" và hệ thống tiến hành kích hoạt thuật toán phân công ngầm dưới nền.

---

## 2. Tiêu chí Chấp nhận cho Module Tài xế (Driver App)

### FR-D01: Chuyển đổi trạng thái (Online/Offline)
* **AC-05.1 (Bật trạng thái sẵn sàng):**
  * **Given** Tài xế đã đăng nhập thành công vào ứng dụng tài xế.
  * **When** Tài xế gạt nút chuyển sang chế độ "Sẵn sàng" (Online).
  * **Then** Ứng dụng phải bắt đầu định kỳ gửi tọa độ GPS hiện tại của tài xế về máy chủ trung tâm với tần suất 5 giây/lần.

### FR-D02 & FR-D03: Nhận thông báo và Phản hồi cuốc xe
* **AC-06.1 (Hiển thị popup nhận cuốc):**
  * **Given** Tài xế đang ở trạng thái Online và nằm trong bán kính quét của hệ thống.
  * **When** Có một yêu cầu đặt xe phù hợp được phát tới.
  * **Then** Màn hình điện thoại của tài xế phải hiển thị popup thông tin chuyến đi (Điểm đón, Điểm đến, Khoảng cách) kèm thanh đếm ngược thời gian phản hồi trong 15 giây.
* **AC-06.2 (Xử lý quá thời gian timeout):**
  * **Given** Tài xế nhận được thông báo cuốc xe mới nhưng không bấm nút Chấp nhận trong vòng 15 giây.
  * **When** Hết thời gian đếm ngược.
  * **Then** Hệ thống phải tự động đóng popup, ghi nhận là "Từ chối" và chuyển cuốc xe sang tài xế tiếp theo mà không làm ảnh hưởng đến ứng dụng của tài xế.

### FR-D04: Cập nhật hành trình tuần tự
* **AC-07.1 (Tuân thủ luồng trạng thái một chiều):**
  * **Given** Tài xế đã chấp nhận cuốc xe và đang trên đường đến điểm đón.
  * **When** Tài xế đến nơi và bấm nút "Đã đến điểm đón".
  * **Then** Trạng thái trên ứng dụng khách hàng phải được cập nhật thời gian thực theo, đồng thời nút bấm của tài xế chuyển sang bước tiếp theo ("Bắt đầu chuyến đi"). Tài xế không thể nhảy cóc trạng thái khi chưa hoàn thành bước trước đó.

---

## 3. Tiêu chí Chấp nhận cho Module Hệ thống Trung tâm (Backend Auto-Dispatch)

### FR-S01 & FR-S02: Thuật toán quét và Re-routing
* **AC-08.1 (Cơ chế tự động chuyển tài xế thay thế):**
  * **Given** Tài xế số 1 được hệ thống chỉ định nhận cuốc nhưng bấm nút "Từ chối" hoặc bị Timeout.
  * **When** Hệ thống nhận tín hiệu từ chối từ tài xế số 1.
  * **Then** Hệ thống phải tự động loại bỏ tài xế số 1 khỏi phiên, tìm ngay tài xế có vị trí gần thứ hai trong bán kính cho phép và gửi thông báo cuốc xe mới tới tài xế đó trong vòng dưới 2 giây. Khách hàng hoàn toàn không phải thao tác tạo lại yêu cầu.

### FR-S03: Thông báo khi hết xe
* **AC-09.1 (Xử lý khi không còn tài xế):**
  * **Given** Hệ thống đã thực hiện quét tìm kiếm qua toàn bộ các tài xế trong bán kính giới hạn tối đa nhưng không có ai chấp nhận hoặc không còn tài xế Online.
  * **When** Vòng lặp quét kết thúc.
  * **Then** Hệ thống phải đóng hoàn toàn phiên tìm kiếm, hiển thị hộp thoại thông báo lỗi rõ ràng cho khách hàng ("Hiện tại không tìm thấy tài xế phù hợp, vui lòng thử lại sau") và giải phóng dữ liệu cuốc xe.
# Bảng Truy vết Yêu cầu (Traceability Matrix) - Nền tảng CAB (Giai đoạn MVP)

Bảng truy vết dưới đây giúp kiểm soát chặt chẽ toàn bộ dự án bằng cách liên kết xuyên suốt từ **Quy tắc Nghiệp vụ (BR)**, **Yêu cầu Chức năng (FR)**, **Use Case (UC)** cho đến **Tiêu chí Chấp nhận (AC)**. Điều này đảm bảo không có yêu cầu nào bị bỏ sót và mọi tính năng đều có thể kiểm thử nghiệm thu chính xác.

| Mã BR | Tên Quy tắc Nghiệp vụ (Business Rules) | Mã FR liên kết | Tên Yêu cầu Chức năng (Functional Requirements) | Mã Use Case | Mã Tiêu chí Chấp nhận (Acceptance Criteria) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **BR-01** | Quy tắc phân loại phương tiện | **FR-C02**<br>**FR-C03** | Nhập vị trí & Tìm đường<br>Báo giá cuốc xe | UC-C02 | AC-02.1 |
| **BR-02** | Quy tắc phân công tài xế tự động | **FR-C04**<br>**FR-D01**<br>**FR-S01** | Gửi yêu cầu đặt xe<br>Chuyển trạng thái Online/Offline<br>Thuật toán quét tài xế | UC-C02<br>UC-D01<br>UC-7 | AC-04.1<br>AC-05.1 |
| **BR-03** | Quy tắc hiển thị thông tin nhận diện | **FR-C05** | Theo dõi trạng thái & Thông tin tài xế | UC-C02<br>UC-D02 | AC-06.1 |
| **BR-04** | Quy tắc xử lý từ chối/timeout chuyến đi | **FR-D03**<br>**FR-S02** | Chấp nhận/Từ chối cuốc xe<br>Cơ chế Re-routing thay thế | UC-D02<br>UC-8 | AC-06.2<br>AC-08.1 |
| **BR-05** | Quy tắc thông báo khi không tìm thấy tài xế | **FR-C07**<br>**FR-S03** | Thông báo hết xe & Quản lý phiên | UC-C02<br>UC-9 | AC-09.1 |
| **BR-06** | Quy tắc xác thực tài khoản tối giản | **FR-C01** | Xác thực tài khoản qua OTP | UC-C01<br>UC-D01 | AC-01.1<br>AC-01.2 |
| **BR-07** | Quy tắc cập nhật trạng thái hành trình tuần tự | **FR-D04** | Cập nhật luồng trạng thái hành trình | UC-D03 | AC-07.1 |
