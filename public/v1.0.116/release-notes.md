# PingPK v1.0.116 — bản thử nghiệm

- Chuyển máu vào túi bang: khi hoàn toàn không phản hồi, chờ khoảng 1 giây rồi nghỉ lỗi 1 giây. Nhánh này khoảng 2 giây, chưa gồm lịch tác vụ.
- Nếu đã có phản hồi hoặc nhận một phần/khác thứ tự, vẫn chờ đủ cả lô ổn định 1 giây trong giới hạn 5 giây cũ. Các trường hợp này có thể lâu hơn 2 giây.
- Bỏ bảng log cuối cửa sổ và thu gọn giao diện; giữ nút Đăng ký, các trang cũ và log chẩn đoán nền.
- Giữ sửa lưới theo con trỏ hiện tại, native FIFO, chống chuyển ngược, điều kiện đủ hai túi và đóng shop trước khi ra hậu doanh.

Đã qua kiểm tra tự động về mua/chuyển thuốc, phản hồi chậm/từng phần, rollback, giao dịch native và bố cục. Chưa xác nhận trên game thật.

**Chưa có kết quả quét Defender:** công cụ quét EXE/thư mục/ZIP trả lỗi dịch vụ `0x800106BA`, ExitCode 2. Đây là lỗi không chạy được quét, không phải kết quả phát hiện virus; cũng không xác nhận gói đã qua kiểm tra antivirus. Không rebuild hoặc thay thiết lập Defender để chọn kết quả.

Gói công khai chỉ chứa cấu hình mặc định, không có license/key khách, cấu hình cá nhân, mật khẩu rương hoặc khóa ký. Giữ riêng dữ liệu đang dùng của bản cũ; giải nén toàn bộ gói, giữ `Shared/engine.dll` trong thư mục bản này.

Bản thử nghiệm được đăng theo yêu cầu người dùng; không thay Latest, kênh cập nhật tự động hoặc lối mở cục bộ.

ZIP SHA256: `f90dc4b066ada4fc535874ccea1f5be820d6d7a4e123dcc3a40e0fdbfe783238`.
