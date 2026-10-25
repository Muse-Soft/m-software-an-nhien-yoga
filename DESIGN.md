# DESIGN.md — Landing page studio yoga An Nhiên (MSR-29)

- Project Linear: m-software-an-nhien-yoga — Epic: TEC-226 — Task Thiết kế: TEC-227
- Repo GitHub (public): https://github.com/Muse-Soft/m-software-an-nhien-yoga
- Phạm vi: chỉ 1 landing page, visual-first. Sản phẩm là trang giới thiệu, không phải hệ thống đặt lịch thật.

## 1. Phong cách tham chiếu (MỘT phong cách duy nhất)

Tối giản thiền định kiểu tạp chí Kinfolk: nhịp chậm, nhiều khoảng trắng, ảnh lớn làm nội dung chính, ít chữ, không họa tiết rườm rà, không icon stock lòe loẹt, không khung màu mạnh. Cảm giác: yên tĩnh, sáng tự nhiên, ấm.

## 2. Bảng màu (mã hex kèm vai trò — bắt buộc dùng đúng)

| Mã | Vai trò |
|---|---|
| #F6F1E7 | Nền chính toàn trang |
| #233528 | Chữ chính (tiêu đề, nội dung) |
| #8A9A5B | Màu nhấn chính (nút chính, tiêu đề phụ, đường kẻ nhấn, giá nổi bật) |
| #EBE3CF | Nền phụ (khối xen kẽ, thẻ lớp học) |
| #FFFFFF | Nền ô nhập, thẻ trắng trên nền chính |
| #5A6B57 | Chữ phụ (mô tả phụ, chú thích, giờ học phụ) |
| #D8CDB8 | Kẻ mảnh, viền nhẹ |
| #1E2A20 | Nền tối (chỉ footer, chữ trên nền tối dùng #F6F1E7) |

Cấm dùng màu ngoài bảng này cho tiêu đề, nút, nền và giá. Màu ảnh mẫu không tính là màu giao diện, nhưng ảnh phải đồng tông ấm (xem §4).

## 3. Font chữ

- Tiêu đề: Cormorant Garamond (serif, thanh thoát, thiền định).
- Nội dung: Be Vietnam Pro (sans, dễ đọc tiếng Việt).
- Nạp qua Google Fonts css2, có tham số subset tiếng Việt (unicode-range tiếng Việt phải được trả về).
- Cỡ chữ cụ thể (desktop / mobile):
  - H1 hero: 56px / 40px, line-height 1.15, Cormorant Garamond, weight 500.
  - H2 section: 36px / 28px, line-height 1.25, Cormorant Garamond, weight 500.
  - H3 (tên lớp, tên giáo viên): 22px / 20px, line-height 1.3.
  - Body: 17px, line-height 1.65, Be Vietnam Pro.
  - Chú thích / chữ phụ: 14px, line-height 1.5.
  - Nút: 16px, weight 600, Be Vietnam Pro.
  - Tiêu đề phụ dạng eyebrow (ví dụ "THỞ CHẬM — SỐNG CHẬM"): 13px, uppercase, letter-spacing 0.18em, màu #8A9A5B.

## 4. Quy tắc hình ảnh (ảnh mẫu)

- Ảnh là nội dung chính, không phải trang trí nhỏ. Tất cả ảnh đều phải ghi rõ là ảnh mẫu trong alt (đuôi "(ảnh mẫu)").
- Tông ảnh: ấm, ánh sáng tự nhiên, màu đất và xanh lá nhạt, không ảnh lạnh/xanh dương mạnh, không ảnh studio chói.
- Tỉ lệ khung bắt buộc:
  - Hero: 16:9, full-bleed toàn màn hình, chiều cao tối thiểu 90vh, chữ đặt trên lớp phủ tối nhẹ chỉ đủ đọc (không phủ kín ảnh).
  - Triết lý / không gian: ảnh 4:5 (đứng) đi kèm chữ, hoặc 4:3 cho ảnh không gian rộng.
  - Lớp học (Hatha / Vinyasa / Yin): thẻ ảnh 4:5.
  - Giáo viên: ảnh chân dung 3:4, đồng tông.
  - Lịch học / không gian phụ: ảnh 4:3 nếu có.
- Ảnh mẫu dùng ngay từ bản đầu tiên, chất lượng cao, đồng tông; không dùng ảnh lệch tông, mờ, vỡ.

## 5. Bố cục — 8 khối theo đúng thứ tự này

1. **Header (dính):** cao 64px, position sticky, top 0, nền #F6F1E7, z-index 10. Logo chữ "An Nhiên" (Cormorant Garamond) bên trái; menu: Triết lý, Lớp học, Giáo viên, Lịch học, Đặt lịch thử; nút chính "Đặt lịch tập thử" (nền #8A9A5B, chữ #FFFFFF). Mobile: menu thu gọn bằng nút mở, không để menu tràn.
2. **Hero:** ảnh lớn 16:9 full-bleed một lớp học buổi sáng trong phòng tràn nắng. Eyebrow "STUDIO YOGA AN NHIÊN"; H1 đúng tinh thần "Thở chậm, sống chậm" (không bịa slogan khác); dòng phụ 1 câu về không gian yên tĩnh cho người mới và người đã tập lâu; 2 nút: "Đặt lịch tập thử" (nhấn) + "Xem các lớp học" (viền mảnh).
3. **Triết lý + không gian:** 2 cột desktop (chữ + ảnh 4:5), 1 cột mobile. Nội dung: triết lý "thở chậm, sống chậm", không gian yên tĩnh, ánh sáng tự nhiên, phù hợp người mới bắt đầu lẫn người đã tập lâu. Không bịa địa chỉ, giờ mở cửa thật.
4. **Các lớp học:** lưới 3 thẻ (desktop 3 cột, mobile 1 cột), mỗi thẻ ảnh 4:5 + tên lớp + mô tả ngắn + giá mẫu:
   - Hatha — cho người mới, chậm, nền tảng hơi thở.
   - Vinyasa — nhịp nhàng, chuyển động liền mạch.
   - Yin — thư giãn buổi tối, giữ tư thế lâu.
   Giá mẫu: 150.000 đồng/buổi, 1.200.000 đồng/tháng. Bắt buộc có dòng chú thích ngay dưới lưới: "Tất cả giá trên trang là giá mẫu."
5. **Giáo viên:** lưới ảnh chân dung 3:4 đồng tông, mỗi người chỉ có tên mẫu + dòng mô tả lớp phụ trách (không bịa bằng cấp, năm kinh nghiệm thật). Tên giáo viên chưa có thật thì ghi rõ là nội dung mẫu trong phần này.
6. **Lịch học tuần:** bảng lịch tuần gọn (thứ + giờ + lớp), desktop dạng bảng, mobile cuộn ngang trong khung (không vỡ bố cục). Giờ học ghi là "Lịch mẫu" nếu chưa có lịch thật.
7. **Form đặt lịch tập thử (frontend-only):** các trường: họ tên, số điện thoại, lớp muốn thử (Hatha / Vinyasa / Yin), ngày muốn tập, ghi chú (không bắt buộc). Form chỉ giao diện: submit chặn gửi thật (preventDefault) và chỉ hiện dòng "Bản demo — form chưa gửi dữ liệu thật." Cấm hứa "studio sẽ liên hệ xác nhận", cấm link tel: giả.
8. **Footer:** nền tối #1E2A20, chữ #F6F1E7. Ghi: địa chỉ [CẦN BỔ SUNG], điện thoại [CẦN BỔ SUNG], giờ mở cửa [CẦN BỔ SUNG] (mỗi vị trí đều giữ nguyên placeholder, không bịa số). Liên kết neo về các khối trên.

## 6. Responsive / mobile

- Breakpoint: 768px. Dưới 768px: mọi lưới về 1 cột; header 64px giữ nguyên; menu mobile mở/đóng được; hero H1 40px; bảng lịch cuộn ngang trong khung, không tràn trang.
- Desktop: nội dung tối đa 1120px, căn giữa, khoảng trắng giữa các khối tối thiểu 80px.

## 7. Quy tắc dữ liệu thật / placeholder (bắt buộc)

- Giá: toàn bộ là giá mẫu, kèm dòng chú thích ở §5 khối 4.
- Địa chỉ, điện thoại, giờ mở cửa, tên giáo viên thật, lịch thật: chưa có thì giữ [CẦN BỔ SUNG] hoặc ghi "Lịch mẫu" / nội dung mẫu, tuyệt đối không bịa số điện thoại, địa chỉ, bằng cấp.
- Ảnh: tất cả là ảnh mẫu, alt kết thúc bằng "(ảnh mẫu)".

## 8. Kiểm tra đối chiếu (dành cho Dev và QA)

- Đủ 8 khối theo thứ tự §5; đủ 8 mã màu đúng vai trò §2, không màu ngoài bảng.
- Font đúng Cormorant Garamond + Be Vietnam Pro, đúng cỡ §3, hỗ trợ tiếng Việt.
- Ảnh đúng tỉ lệ §4, đồng tông ấm, alt có "(ảnh mẫu)".
- Form đúng frontend-only, không tel: giả, không hứa liên hệ.
- Mobile 768px: 1 cột, menu mở được, bảng không vỡ.
- Chưa kiểm thị giác nếu không chụp được màn hình — ghi rõ trong kết quả, không kết luận đạt thẩm mỹ khi chưa nhìn thấy.
