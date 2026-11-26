# BÀI LÀM PHA 2 – HACKATHON 02

- **Mã đề:** 05
- **Họ tên:** Nguyễn Thành Nam
- **Lớp:** CNTT2
- **Link repository Pha2:** https://github.com/nam088-vn/HN-KS26-CNTT2_PromptAI_H02_Pha1-Pha2
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):** Gemini

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đặt vé xem phim ra JSON

**KET QUA AI**

```text
[
{
"loai_ve": "P2D",
"ngay_chieu": "2026-12-24",
"ve_nguoi_lon": 2,
"ve_tre_em": 1,
"ghi_chu": null,
"loai_ghe": "thuong"
},
{
"loai_ve": "P3D",
"ngay_chieu": "2027-01-01",
"ve_nguoi_lon": 3,
"ve_tre_em": 0,
"ghi_chu": "1 người hay chóng mặt, cần ngồi gần lối ra",
"loai_ghe": null
},
{
"loai_ve": "GOLD",
"ngay_chieu": null,
"ve_nguoi_lon": 4,
"ve_tre_em": 0,
"ghi_chu": "1 bạn đi xe lăn",
"loai_ghe": "doi"
}
]
```

**Link trò chuyện:**

https://share.gemini.google/4goSrCP41Y7Q

## 4.3. Báo giá bằng Chain-of-Thought

**KET QUA AI**

```text
* **Bước 1: Tiền người lớn**
Phim 3D (P3D) có giá 130.000 đồng/vé người lớn. Nhóm có 5 người lớn:

$$5 \times 130.000 = 650.000\text{ đồng}$$


* **Bước 2: Tiền trẻ em**
Có 2 trẻ em cao 1,1 m và 1,25 m (thuộc diện từ 1 m đến 1,3 m, tính 70% giá vé người lớn) và 1 bé cao 0,9 m (dưới 1 m, miễn phí):

$$(2 \times 130.000 \times 70\%) + (1 \times 0) = 182.000 + 0 = 182.000\text{ đồng}$$


* **Bước 3: Tiền vé (tiền người lớn + tiền trẻ em)**

$$650.000 + 182.000 = 832.000\text{ đồng}$$


* **Bước 4: Giảm giá nhóm**
Nhóm có 5 người lớn nên được giảm 10% trên tổng tiền vé:
* Số tiền được giảm: $832.000 \times 10\% = 83.200\text{ đồng}$
* Tiền vé sau giảm: $832.000 - 83.200 = 748.800\text{ đồng}$


* **Bước 5: Tiền combo**
Nhóm mua 3 combo bắp nước với giá 75.000 đồng/combo (không áp dụng giảm giá):

$$3 \times 75.000 = 225.000\text{ đồng}$$


* **Bước 6: Tổng tiền**

$$\text{Tổng tiền} = 748.800 + 225.000 = 973.800\text{ đồng}$$



[RESULT: 973.800 đồng]
```

**Link trò chuyện:**

https://share.gemini.google/oVhxIp5pXe3E

### b) Kiểm tra kết quả AI

AI làm đúng

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
{"loai_su_co": "loi_ky_thuat", "so_khach": 4, "so_suat_bi_loi": 2, "tom_tat": "Gia đình 4 người gặp sự cố mất tiếng hơn 15 phút ở cả 2 suất phim."}
```

**Link trò chuyện:**

https://share.gemini.google/RYrois0ryex7

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**
```text
| Tiêu chí | Điểm | Minh chứng | Đề xuất sửa |
| --- | --- | --- | --- |
| **Đúng thông tin (50%)** | 0/5 | **(1) Trích dẫn:** *"Vé 2D bên em có 80k thôi nè, rẻ xỉu."* và *"Anh huỷ trước 2 tiếng vẫn được hoàn 50% nha anh."*<br>

<br>**(2) Lý do sai:** Sai cả hai thông tin chuẩn của Ban tổ chức. Giá vé 2D chuẩn là 90.000 đồng/vé người lớn (không phải 80k). Chính sách huỷ vé quy định huỷ trước giờ chiếu dưới 3 giờ sẽ không được hoàn tiền (2 tiếng thuộc mốc dưới 3 giờ, không phải hoàn 50%). | **(3) Câu sửa:** "Dạ, giá vé phim 2D tại rạp Ánh Dương hiện là 90.000 đồng/vé người lớn ạ. Về chính sách huỷ vé, trường hợp huỷ trước giờ chiếu dưới 3 tiếng sẽ không được hỗ trợ hoàn tiền (rạp chỉ hoàn 50% khi huỷ trước từ 3 đến dưới 24 tiếng và hoàn 100% khi huỷ trước từ 24 tiếng trở lên) ạ." |
| **Đầy đủ (30%)** | 1.5/3 | **(1) Trích dẫn:** *"Cần gì nhắn em nha!"*<br>

<br>**(2) Lý do sai:** Bài làm đã đề cập đủ 2 câu hỏi của khách hàng nhưng thiếu phần mời khách cung cấp thông tin chi tiết (ngày, suất chiếu, số lượng vé) để hỗ trợ đặt chỗ theo yêu cầu của rubric. | **(3) Câu sửa:** "Nếu anh/chị muốn đặt vé, vui lòng cung cấp giúp em thông tin về ngày xem, suất chiếu và số lượng vé để em hỗ trợ giữ chỗ ngay cho mình ạ." |
| **Giọng điệu (20%)** | 0.5/2 | **(1) Trích dẫn:** *"Hi anh! Vé 2D bên em có 80k thôi nè, rẻ xỉu. Anh huỷ trước 2 tiếng vẫn được hoàn 50% nha anh. Cần gì nhắn em nha!"*<br>

<br>**(2) Lý do sai:** Sử dụng nhiều từ ngữ suồng sã, thiếu tính chuyên nghiệp trong giao tiếp chăm sóc khách hàng ("Hi", "80k", "thôi nè", "rẻ xỉu", "nha anh", "nhắn em nha"). | **(3) Câu sửa:** "Chào anh/chị, rạp phim Ánh Dương xin phép gửi thông tin tư vấn đến mình ạ: ... Rất mong được đón tiếp anh/chị tại rạp ạ!" |

Tổng điểm: 2/10
```

**Link trò chuyện:**
 
https://share.gemini.google/jdhnxm9YDRd7