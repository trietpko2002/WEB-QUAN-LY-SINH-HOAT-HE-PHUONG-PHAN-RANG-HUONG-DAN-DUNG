# 🌟 HỆ THỐNG QUẢN LÝ SINH HOẠT HÈ CẤP PHƯỜNG (BẢN PRO)

> **Một nền tảng quản lý thanh thiếu niên tham gia sinh hoạt hè tại địa phương thông minh, bảo mật và hoàn toàn tự động.**
> Tích hợp Groq AI, tự động chia nhóm, xuất báo cáo PDF/Excel, bảo mật Cloudflare Turnstile và giao diện chuẩn Web-App hiện đại.

---

## 📑 MỤC LỤC
1. [ Bảng Phân Quyền (Role Matrix)](#-bảng-phân-quyền)
2. [👦 Hướng dẫn dành cho Học sinh / Thanh niên](#1-dành-cho-học-sinh--thanh-niên)
3. [👨‍💼 Hướng dẫn dành cho Quản lý Nhóm](#2-dành-cho-quản-lý-nhóm)
4. [👑 Hướng dẫn dành cho Quản trị viên (Admin)](#3-dành-cho-quản-trị-viên-admin)
5. [💡 Các tính năng Nâng cao (Deep Dive)](#4-các-tính-năng-nâng-cao)

---

## 📊 BẢNG PHÂN QUYỀN

| Tính năng | Học Sinh (Public) | Quản Lý (Manager) | Quản Trị (Admin) |
| :--- | :---: | :---: | :---: |
| **Đăng ký tham gia** | ✅ | ✅ | ✅ |
| **Tra cứu sđt quản lý** | ✅ | ✅ | ✅ |
| **Đăng nhập hệ thống** | ❌ | ✅ (Chỉ thấy nhóm mình) | ✅ (Thấy toàn bộ) |
| **Sửa thông tin học sinh** | ❌ | ✅ (Chỉ nhóm mình) | ✅ (Toàn bộ) |
| **Thêm mới / Xóa / Điểm danh** | ❌ | ✅ (Chỉ nhóm mình) | ✅ (Toàn bộ) |
| **Chuyển học sinh sang nhóm khác** | ❌ | ⏳ (Gửi yêu cầu, chờ duyệt) | ✅ (Chuyển ngay) |
| **Thống kê Biểu đồ & Xuất PDF** | ❌ | ❌ | ✅ |
| **Tạo & Chia Nhóm Tự động** | ❌ | ❌ | ✅ |
| **Nhập/Xuất Excel & Backup JSON**| ❌ | ❌ | ✅ |
| **Dùng Trợ lý AI (Groq)** | ❌ | ❌ | ✅ |

---

## 👦 1. DÀNH CHO HỌC SINH / THANH NIÊN
*(Giao diện bên ngoài trang chủ, không cần đăng nhập)*

### 📝 Đăng ký Sinh hoạt hè
- Truy cập vào đường link hệ thống do địa phương cung cấp.
- Tại màn hình chính, nhấn vào nút **ĐĂNG KÝ SINH HOẠT HÈ**.
- Hệ thống sẽ mở ra một cửa sổ Form điền thông tin (Họ tên, SĐT Zalo, Trường, Lớp, Chi đoàn, Địa chỉ...).
- Nhấn **Gửi** và chờ thông báo chữ "Thành công".
- Thông tin của bạn sẽ được tự động lưu vào cơ sở dữ liệu và chuyển trạng thái thành "Chưa thông báo".

### 🔍 Tra cứu thông tin Bí thư / Quản lý
- Dùng khi muốn chủ động liên hệ xin phép vắng hoặc hỏi lịch sinh hoạt.
- Tại mục **Tra cứu Bí thư / Quản lý**, chọn tab **Chi Đoàn** hoặc **Nhóm**.
- Chọn tên Chi đoàn/Nhóm của mình trong danh sách thả xuống.
- Hệ thống hiển thị Tên và Số điện thoại. Bạn có thể **bấm trực tiếp vào số điện thoại** (trên smartphone) để gọi ngay lập tức.

---

## 👨‍💼 2. DÀNH CHO QUẢN LÝ NHÓM
*Tài khoản được cấp bởi Admin Hệ thống.*

### 🔐 Đăng nhập & Đổi mật khẩu
1. Nhập **Tên đăng nhập** và **Mật khẩu** (Mật khẩu mặc định khi mới cấp thường là: `Abc@123`).
2. Nhập mã xác nhận (Captcha) gồm 6 ký tự. Có thể bấm icon 🔄 để đổi mã nếu khó nhìn.
3. Tick vào ô xác minh Cloudflare "Tôi không phải robot".
4. **Bắt buộc đổi mật khẩu:** Nếu là lần đầu tiên đăng nhập, một bảng thông báo đỏ sẽ hiện ra yêu cầu bạn đổi mật khẩu mới (tối thiểu 6 ký tự) để bảo vệ nhóm của mình.

### 📋 Quản lý danh sách thành viên
- Sau khi đăng nhập, bạn chỉ nhìn thấy danh sách các học sinh/thanh niên **thuộc nhóm của mình**.
- Nút **Sửa (Icon Cây bút)**: Giúp bạn cập nhật thông tin sai sót của học sinh.
- Nút **Báo (Icon Clipboard)**: Bấm 1 lần, hệ thống sẽ copy nội dung chào mừng có sẵn tên, trường, sđt của người đó. Đồng thời, nhãn trạng thái tự đổi từ màu đỏ (Chưa báo) sang màu xanh (Đã báo).

### 🔄 Xin chuyển nhóm cho học sinh
- Nút **Chuyển Nhóm (Icon Mũi tên 2 chiều)**: Dùng khi học sinh xin qua nhóm khác để sinh hoạt cùng bạn bè.
- Chọn nhóm muốn chuyển tới.
- Hệ thống sẽ gắn một nhãn màu hồng **"🕒 Xin qua: [Tên nhóm]"** dưới tên người đó. Bạn phải chờ Admin duyệt thì dữ liệu mới thực sự biến mất khỏi danh sách của bạn.

### 🙋‍♂️ Báo cáo Điểm danh
- Bắt buộc làm sau mỗi buổi sinh hoạt. Trên thanh công cụ, nhấn nút xanh dương **Báo Cáo Điểm Danh**.
- Hệ thống sẽ hiển thị danh sách tất cả học sinh trong nhóm.
- Bạn chỉ cần **Tick chọn những ai VẮNG MẶT**.
- Hệ thống tự động tính số người "Có mặt" và tổng hợp tên người vắng vào ô "Ghi chú". Nhấn **Lưu Báo Cáo** để nộp lên cho Admin.

---

## 👑 3. DÀNH CHO QUẢN TRỊ VIÊN (ADMIN)
*Tài khoản có toàn quyền quản trị, thấy toàn bộ dữ liệu.*

### 📊 Theo dõi Thống kê & Báo cáo
- Thanh Dashboard ngay trên đầu hiển thị 4 thẻ: Tổng số, Đã báo, Chưa báo, và **Chờ duyệt** (Màu vàng).
- Nút **Thống Kê (Icon Chart)**: Mở bảng biểu đồ trực quan (Biểu đồ tròn, cột thống kê Trường, Giới tính, Chi đoàn). Bạn có thể bấm nút **Xuất Báo Cáo PDF** để in báo cáo nộp cho cấp trên.
- *Mẹo:* Bạn có thể bấm vào các cột/phần của biểu đồ, hệ thống sẽ tự động đóng biểu đồ và **lọc danh sách** theo đúng tiêu chí bạn vừa bấm!

### 👥 Quản lý Danh mục (Chi đoàn & Nhóm)
- **Quản lý Chi Đoàn (Nút Tím)**: Thêm, sửa, xóa Chi đoàn và nhập SĐT của Bí thư.
- **Chia Nhóm (Nút Cam)**: 
  - Tạo các nhóm mới, cấp tên tài khoản quản lý.
  - Reset mật khẩu của quản lý về mặc định (`Abc@123`).
  - Theo dõi trực tiếp **Tiến độ điểm danh** của từng nhóm (Tổng số, Có mặt, Ai vắng, Thời gian báo cáo lúc mấy giờ).
  - **Tính năng Auto Group (Chia nhóm ngẫu nhiên):** Chọn 1 bộ lọc (VD: lọc riêng Nam), mở bảng Chia nhóm, nhập mật khẩu Admin và bấm Bắt đầu. Hệ thống sẽ xáo trộn ngẫu nhiên và chia đều các học sinh đang hiển thị vào tất cả các nhóm!

### ✔️ Xử lý Yêu cầu Chuyển nhóm
- Khi Quản lý nhóm gửi yêu cầu, số trên thẻ "Chờ duyệt" góc phải sẽ tăng lên.
- Tại cột *Thao tác* của người đó, Admin sẽ thấy xuất hiện 2 nút: **[✓ Duyệt]** (Chấp nhận chuyển) hoặc **[✕ Hủy]** (Từ chối chuyển). Nhấn xong hệ thống sẽ xử lý ngay lập tức mà không tải lại trang.

### 🤖 Trợ lý Phân tích Dữ liệu AI (GROQ AI)
- Nhấn nút **Phân tích AI**.
- Nhập API Key của Groq. Cung cấp Prompt (yêu cầu).
- AI sẽ tự động thu thập số liệu hiện tại của phường và đưa ra các lời khuyên, kế hoạch, đánh giá thực trạng cực kỳ chuyên sâu bằng tiếng Việt.

### 📢 Trình tạo Thông báo Tập thể
- Lọc ra một danh sách (VD: Tìm những bạn lớp 10, chưa báo cáo).
- Nhấn **Tạo Thông Báo**, điền Tiêu đề, Thời gian, Địa điểm. Bấm **Tạo Nội Dung**.
- Nếu bạn tick vào ô checkbox *"Đồng thời cập nhật trạng thái đã báo cho X người"*, khi bạn bấm Copy, lập tức toàn bộ X người đang hiển thị sẽ được tick xanh "Đã báo" tự động. Rất tiện để không phải bấm thủ công từng người.

---

## 💡 4. CÁC TÍNH NĂNG NÂNG CAO (DEEP DIVE)

**1. Thao tác Hàng loạt (Bulk Actions)**
- Tick chọn 1 hoặc nhiều ô vuông ở cột đầu tiên của danh sách.
- Lập tức trên thanh công cụ sẽ mọc ra 2 nút: **Xóa Đã Chọn (Màu đỏ)** và **Đánh Dấu Đã Báo (Màu xanh)** kèm theo số lượng. Nhấn vào để thực hiện hàng loạt.

**2. Nhập & Xuất dữ liệu Excel**
- **Xuất Excel**: Lọc dữ liệu bạn muốn, bấm Xuất. File tải về (`.xlsx`) đã được tự động căn chỉnh độ rộng cột chuẩn chỉ, sẵn sàng in ấn.
- **Nhập Excel**: Bấm Nhập Excel, chọn file `.xlsx`. Hệ thống thông minh sẽ tự động nhận diện các cột như: *Họ và Tên, Họ Tên, Giới tính, SDT, Lớp...* (không phân biệt viết hoa/thường) và import hàng nghìn bản ghi chỉ trong vài giây. Có xử lý cả lỗi ngày tháng Excel (dạng số Serial).

**3. Hệ thống Sao lưu cực mạnh (Backup/Restore JSON)**
- **Sao lưu**: Tải toàn bộ Database sạch về máy dưới dạng `.json`.
- **Khôi phục**: Khi hệ thống bị lỗi hoặc bị xóa nhầm, bấm Khôi phục. Tính năng này vô cùng nguy hiểm vì nó **ghi đè và xóa sổ dữ liệu cũ**, do đó hệ thống bắt buộc Admin phải: *Nhập lại Mật khẩu Admin* + *Nhập Captcha*. Sau đó hệ thống sẽ cắt dữ liệu thành từng Chunk (gói 100 người) để upload, đảm bảo không bị lỗi Timeout của Google Script.

**4. Bộ lọc đa tầng thời gian thực**
- Thanh tìm kiếm: Cứ gõ là lọc (debounce nội bộ). Lọc Tên, Số điện thoại (chấp nhận cả gõ có cách hoặc dính liền), hoặc Mã TN.
- Kết hợp bộ lọc: Bạn có thể chọn cùng lúc: *Nam + Sinh năm 2008 + Chưa báo + Mạng Viettel*... Dữ liệu sẽ trả về ngay lập tức không có độ trễ nhờ thuật toán JS lọc tại Client.

**5. Tự động bảo toàn dữ liệu SĐT**
- Mọi SĐT nhập qua Form, Web hay Excel đều được hệ thống ép kiểu bằng cách gắn dấu nháy đơn `'` ẩn phía trước. Đảm bảo Excel/Google Sheet không bao giờ ăn mất số `0` ở đầu số điện thoại của học sinh.

---

<div align="center">
  <i>Xây dựng với chuẩn Web-App hiện đại (Google Apps Script + HTML/CSS/JS + API Fetch)</i><br>
  <b>Tác giả: Triết Võ | Bản quyền © 2026 Tổ Công Nghệ Đoàn Phường</b>
</div>
