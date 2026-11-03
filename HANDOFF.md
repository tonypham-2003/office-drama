# Office Drama: tóm tắt dự án (để chuyển sang project mới)

## Hiện trạng
- **Link chơi:** https://tonypham-2003.github.io/office-drama/ (thêm `#ma-phong` để vào phòng riêng, ví dụ `#nhom-huy`).
- **Mã nguồn:** repo GitHub `tonypham-2003/office-drama`, toàn bộ game nằm trong một file `index.html`.
- **Bản trong Claude (artifact):** https://claude.ai/artifact/REU9714EC1aQcxTvGUniHx. Bản này online qua tính năng room của Claude, cần tài khoản Claude. Bản chính để chơi với bạn bè là bản GitHub.

## Ý tưởng game
- Game văn phòng 2D nhìn từ trên xuống, chạy trên trình duyệt (điện thoại và máy tính).
- Chơi online tối đa 5 người, hoặc chơi với 12 đồng nghiệp do máy điều khiển.
- Một ván dài 4 phút. Hết giờ thì tính điểm và trao danh hiệu.
- Phong cách: đồ họa gọn gàng, nhân vật ngố và dị hợm (mắt lồi, chân mì sợi, găng tay hoạt hình).

## Nhân vật (phòng ban, kỹ năng ⭐)
| Nhân vật | Phòng | Kỹ năng |
|---|---|---|
| Sales (người) | Sales | Chốt deal: +12 KPI |
| Mèo Kế toán | Kế toán | Trừ lương: người bên cạnh -12 KPI |
| Chó HR | HR | Lập biên bản: -12 uy tín, đứng hình |
| Lốp Vận hành | Vận hành | Lăn: tăng tốc, húc ngã người khác |
| Bình hoa Lễ tân | Lễ tân | Loa phường: người xung quanh -4 uy tín |
| Chậu cây IT | IT | Tắt wifi: người xung quanh bị chậm |
| Lò vi sóng | Market Research | Hâm nóng drama: -10 uy tín, +12 stress, kêu DING! |
| Sếp (NPC) | Phòng Sếp | Đi tuần, phạt người đánh nhau hoặc tám chuyện |

## Lối chơi
- **Chỉ số:** KPI, Uy tín, Thiện cảm, Stress, Năng lượng (hồi ở Pantry).
- **Hành động (phím 1–7):** Nói chuyện (chọn 1 trong 3 câu: Khen, Hỏi chuyện riêng, Cà khịa, Rủ rê, Buôn dưa), Nói xấu, Tán tỉnh, Đấm, Nịnh sếp, Kỹ năng, Trốn (vào tủ hoặc thùng carton).
- **Sự kiện ngẫu nhiên:**
  - Sếp đi tìm người giao việc gấp (trốn tìm)
  - Họp đột xuất
  - Mất wifi
  - Tiệc trà sữa
  - Sếp kiểm tra KPI
- **Đánh Sếp:** đủ đòn thì Sếp "ngất" 20 giây; ai từng đấm được +15 KPI.
- **Nhiệm vụ** (giấy note vàng): pha cà phê, nộp báo cáo, họp, nói chuyện, trốn việc...
- **Điểm** = KPI + 0.8×Uy tín + 0.6×Thiện cảm − 0.4×Stress + 5×số nhiệm vụ.
- **Danh hiệu:** Nhân viên xuất sắc, Trùm drama, Võ sĩ văn phòng, Người lật đổ Sếp, Thánh nịnh, Cặp đôi văn phòng, Đề xuất cho nghỉ việc.

## Kỹ thuật chơi online (bản GitHub)
- Dùng PeerJS (miễn phí, không cần server riêng).
- Người vào phòng đầu tiên làm chủ phòng (hub). Máy chủ phòng điều khiển Sếp, sự kiện và đồng hồ. Chủ phòng thoát thì người khác tự lên thay.
- Mỗi người gửi vị trí và chỉ số khoảng 15 lần/giây. Hành động tác động lên người khác gửi kèm dưới dạng hiệu ứng (trừ điểm, choáng, lời thoại).
- Một số mạng 4G hoặc wifi công ty có thể chặn kết nối trực tiếp giữa các máy (chưa có máy chủ TURN).

## Lịch sử sửa đổi chính
1. Bản đầu: chơi với 12 đồng nghiệp máy, đồ họa gọn gàng.
2. Thêm hệ thống nói chuyện theo lựa chọn và trốn tìm.
3. Thử đồ họa "xấu cố ý" kiểu MS Paint: người dùng không thích, đã bỏ.
4. Đổi sang nhân vật ngố: mắt lồi, chân mì sợi, tay khều khào.
5. Thêm chơi online 5 người, đưa lên GitHub Pages.
6. Sửa lỗi điện thoại bị phóng to không bấm được nút; thêm nút + / − để thu phóng bản đồ.

## Việc có thể làm tiếp
- Thêm máy chủ TURN để mạng nào cũng kết nối được.
- Nhân vật quay đủ 4 hướng, thêm nhân vật mới (máy photocopy, cốc cà phê, cây nước...).
- Chat chữ giữa người chơi; chế độ đóng vai Sếp cho người thật.
- Bảng xếp hạng lưu qua nhiều ván.
