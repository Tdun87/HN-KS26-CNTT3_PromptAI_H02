# BÀI LÀM PHA 2 – HACKATHON 02

- **Mã đề:** 09
- **Họ tên:** Nguyễn Tiến Dũng
- **Lớp:** CNTT3
- **Link repository Pha2:** https://github.com/Tdun87/HN-KS26-CNTT3_PromptAI_H02
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):** Gemini

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đặt chỗ workshop ra JSON

**KET QUA AI**

```text
[
  {
    "ma_lop": "NANTAY",
    "ngay_hoc": "2026-12-13",
    "nguoi_lon": 2,
    "tre_em": 1,
    "ca_hoc": "chieu",
    "ghi_chu": null
  },
  {
    "ma_lop": "BANXOAY",
    "ngay_hoc": "2027-01-10",
    "nguoi_lon": 3,
    "tre_em": 0,
    "ca_hoc": null,
    "ghi_chu": "1 người bị đau cổ tay"
  },
  {
    "ma_lop": "VEGOM",
    "ngay_hoc": null,
    "nguoi_lon": 4,
    "tre_em": 0,
    "ca_hoc": "sang",
    "ghi_chu": "1 bạn đi xe lăn"
  }
]
```

**Link trò chuyện:** https://share.gemini.google/kpiNfhJ1Z9rE

## 4.3. Báo giá bằng Chain-of-Thought

**KET QUA AI**

```text
Tiền người lớn (lớp BANXOAY): 5 × 550.000 = 2.750.000 đồng

Tiền trẻ em (2 trẻ 8 tuổi và 12 tuổi tính 70%, 1 bé 4 tuổi miễn phí): 2 × (550.000 × 70%) = 2 × 385.000 = 770.000 đồng

Tiền học: 2.750.000 + 770.000 = 3.520.000 đồng

Giảm giá nhóm (đủ 5 người lớn, giảm 5% tiền học): 3.520.000 × 5% = 176.000 đồng → Tiền học sau giảm: 3.520.000 - 176.000 = 3.344.000 đồng

Phí nung và giao (4 sản phẩm): 4 × 80.000 = 320.000 đồng

Tổng tiền: 3.344.000 + 320.000 = 3.664.000 đồng

[RESULT: 3.664.000 đồng]
```

**Link trò chuyện:** https://share.gemini.google/b9ksU9vnsVYj

### b) Kiểm tra kết quả AI

AI tính đúng

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
{
  "loai_su_co": "hong_san_pham",
  "so_khach": 3,
  "so_san_pham_bi_hong": 5,
  "tom_tat": "Khách nhận hàng có 5/6 sản phẩm gốm bị nứt vỡ khi giao, yêu cầu xưởng giải quyết."
}
```

**Link trò chuyện:** https://share.gemini.google/BOI5ASVPsjP9

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```text
| Tiêu chí | Điểm | Minh chứng | Đề xuất sửa |
| :--- | :--- | :--- | :--- |
| Đúng thông tin (50%) | 0/5 | Nhân viên báo giá sai (*"200k"* thay vì **250.000 đồng/người lớn** cho lớp VEGOM) và báo sai chính sách đổi lịch (*"đổi trước 1 ngày thì free"* thay vì phí **30.000 đồng/người** do đổi trước 1 ngày tương đương 24 giờ, nằm trong mốc từ 12 đến dưới 48 giờ). | Sửa lại chính xác: Giá lớp vẽ gốm (VEGOM) là **250.000 đồng/người lớn**. Nếu đổi lịch trước giờ học 1 ngày (24 giờ), mức phí áp dụng là **30.000 đồng/người** (chỉ miễn phí khi đổi trước từ 48 giờ trở lên). |
| Đầy đủ (30%) | 1.5/3 | Đã đề cập tới cả hai câu hỏi của khách (giá lớp và phí đổi lịch) nhưng hoàn toàn thiếu phần mời khách cung cấp ngày học, ca học và số lượng người để hỗ trợ đặt chỗ. | Bổ sung câu mời đặt chỗ ở cuối: *"Nếu anh/chị muốn đăng ký, vui lòng cho bên em biết ngày học, ca học và số lượng người tham gia để em hỗ trợ giữ chỗ ạ."* |
| Giọng điệu (20%) | 0.5/2 | Văn phong quá suồng sã, thiếu tính chuyên nghiệp (*"Hi chị ơi"*, *"200k thôi nè, vui lắm luôn"*, *"free nha chị"*, *"nhắn em nha"*). | Thay thế bằng ngôn ngữ lịch sự, chuẩn mực: dùng *"Dạ chào anh/chị"*, *"250.000 đồng"*, *"miễn phí"*, *"liên hệ lại với bên em ạ"*. |

**Tổng điểm: 2/10**
```

**Link trò chuyện:** https://share.gemini.google/q6El2PIMsgkv
