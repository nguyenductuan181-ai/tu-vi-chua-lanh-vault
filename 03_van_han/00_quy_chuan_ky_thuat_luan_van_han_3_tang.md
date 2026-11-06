---
name: tu-vi-van-han-3-tang
description: Luận vận hạn 3 tầng theo Nữ Pháp Sư Luận Vận Hạn.
---

# Kỹ thuật Luận Vận Hạn 3 Tầng (Nữ Pháp Sư Luận Vận Hạn)

Kho tư liệu gốc: `/opt/ai-os/products/ceo/resources/nu_phap_su_van_han/` (135 bài giảng/audio/pdf, 6.2M ký tự).
Công cụ tra cứu FTS Chunks siêu tốc (<5ms): `tvcl "<từ khóa>"` (đã cấu hình binary toàn cục `/usr/local/bin/tvcl`, tra cứu 4.901 đoạn trích trong `fts_chunks.db`).
QUY TẮC CỐT LÕI: Khi luận giải bất kỳ câu hỏi nào về Vận Hạn/Tử Vi, BẮT BUỘC chạy `tvcl "<từ khóa>"` trước để lấy đúng trích đoạn gốc từ bài giảng của Nữ Pháp Sư, khóa chặt 100% tri thức thực chứng. TUYỆT ĐỐI CẤM trả lời từ kiến thức tổng quát của LLM.

## 1. Ba Tầng Vận Động
- **Tầng 1 - Nguyên Cục (NC):** Gốc rễ, giống cây, nghiệp nền (`cungChu` từ daotuvi).
- **Tầng 2 - Đại Vận 10 năm (ĐV):** Dòng thời cuộc bao trùm, thời tiết theo mùa (`cungDaiVan` từ daotuvi).
- **Tầng 3 - Tiểu Vận (TV):** Nắng mưa trong ngày, duyên kích hoạt sự kiện cụ thể của 1 năm (`cungTieuVan` từ daotuvi). Luận theo **Lưu Niên Thái Tuế** (theo Địa Chi năm xem làm Mệnh.TV) để lấy Can năm an Lưu Tứ Hóa & Lưu Kình Đà (phái Mộc Đầu / Khâm Thiên Giám / Trung Châu Vương Đình Chi).

## 2. Ma Trận Phối Hợp Cát - Hung 3 Tầng
- **Cát - Cát - Cát:** Đại Cát. Thành tựu lớn, thuận buồm xuôi gió, bung sức mở rộng.
- **Cát - Cát - Hung:** Bình hòa / Tiểu Hung. Gốc và vận 10 năm vững thì hung 1 năm chỉ là bài học nhỏ, dễ vượt qua.
- **Cát - Hung - Hung:** Khủng hoảng lớn. Gốc tốt nhưng thời vận đè, tổn hại uy tín, hao tài nếu cố bung sức.
- **Hung - Cát - Cát:** Tiểu Cát. Gốc yếu nhưng gặp thời cứu, có lộc nhưng khó giữ bền nếu thiếu kỷ luật nội tại.
- **Hung - Hung - Cát:** Ảo vọng. Cát 1 năm không đủ sức chống đỡ gốc và đại vận suy, tuyệt đối không đầu tư lớn.
- **Hung - Hung - Hung:** Đại Hung. Nghiệp thức dâng tràn, nguy cơ mất việc, đổ vỡ, bệnh tật; cần thủ thế, tĩnh tâm, tu tập chuyển hóa.
- *Quy tắc việc tốt lớn xảy ra:* Cần tối thiểu 2 tầng Cát + 1 tầng Bình.

## 3. Quy Tắc Kích Hoạt Trùng Tầng
- **Tam Lộc Kích (3 tầng Hóa Lộc hội chiếu):** Lộc NC + Lưu Lộc ĐV + Lưu Lộc TV. Đại phát tài chính. Hội Cát tinh -> thịnh vượng bền vững. Hội Hung tinh -> lộc bạo phát bạo tàn hoặc tiền đền bù tai nạn/rủi ro.
- **Tam Kỵ Kích (3 tầng Hóa Kỵ hội tụ):** Điểm nghẽn nghiệp thức kích hoạt tối đa. Tuyệt đối không mưu sự lớn (không cưới hỏi, không mở cty, không đổi nghề). Mượn lực từ cung Cát khác (Phúc Đức, Phụ Mẫu) để chuyển hóa.
- **Lưu Kình Đà 3 Tầng:** Kình Đà gốc + Kình Đà ĐV + Lưu Kình Đà TV cùng chiếu -> sự kiện biến động mạnh xảy ra dứt khoát (phẫu thuật, di chuyển chỗ ở, thay đổi nhân sự/công việc).

## 4. Quy Chuẩn Gọi API daotuvi.com
- `gioitinh`: Bắt buộc chuỗi `'nam'` hoặc `'nu'` (không dùng int 1/0).
- `giosinh`: Mã giờ 1-13 ($1$: Tý 0-1h ... $10$: Dậu 17-19h).
- `namxem` & `thangxem`: Khi xem tổng quan vận năm YYYY, đặt `thangxem=6` để chắc chắn nằm trọn vẹn trong năm âm lịch cần xem, tránh rơi vào tháng Chạp năm trước nếu để ngày 1/1.
- `thapNhiCung`: Mảng 13 phần tử (index 1..12 tương ứng Tý..Hợi).
  - `cungChu`: Tên cung Nguyên Cục gốc (Tầng 1).
  - `cungDaiVan`: Tên cung Đại Vận 10 năm (Tầng 2, VD: `QUAN LỘC.ĐV`).
  - `cungTieuVan`: Tên cung Tiểu Vận năm xem (Tầng 3, VD: `QUAN LỘC.TV`).
  - `cungSao`: Danh sách sao tọa thủ. Lọc `saoLoai == 1` là Chính tinh, `saoLoai == 9` hoặc tên có tiền tố `Lưu` là Sao Lưu kích hoạt năm.
