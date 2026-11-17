# QA Scorecard — Bó Hoa Đến Trễ

Phiên bản: 2026-11-16 (component-first V3)
File: `index.html` (48.578 bytes)

## Component inventory & PASS/FAIL

| Component | Symbol / hook | Scene | Đánh giá | Ghi chú |
|---|---|---|---|---|
| Bánh kem | `#v3-cake`, `#v3-cloche`, `#v3-candle`, `#v3-flame` | 9–11 | PASS | Cloche đã viết lại (đĩa 2 ellipse, kính trắng .42, vệt sáng, núm); nến có ngọn nối ngọn, flame dịch y=-13; thổi nến ra khói `#9C9290` |
| Gấu bông | `#v3-teddy` (viewBox 0 0 240 200) | 4 (bản đồ), 8 (thiệp) | PASS | Vision: scene 4 góc dưới phải ô lưới x430–620/y340–460, dễ thương, tim đỏ, không cắt; scene 8 bên phải thiệp, thích hợp, không che lời |
| Các loài hoa | `#v3-flower-*`, `#v3-bud`, `#v3-stem`, `#v3-leaf` | 3–7 | PASS | 3 loài chọn được (Hồng/Cúc/Tulip) + bud nở 0/1/2 |
| Tấm thiệp | `#v3-card`, `#v3-vase`, `#v3-polaroid`, `#v3-wax-seal` | 8 | PASS | Giấy pink + dây tie; wax seal 420,300 |
| Hộp quà | `#v3-gift-box` | scene final | PASS | Thân `#D98FA3`, nắp `#F2BFC9`, dây `#F2D28C`, nơ `#F5D7DD` |

## Kiểm tra xác định (không suy đoán)

- Viewport 390×844 @2x và 1440×900 @1: `document.documentElement.scrollWidth == innerWidth` (không overflow ngang).
- Gấu bông nằm trong khung art (inside=true) cả scene 4 và scene 8; `over=0` (không đè caption/chapter/h2/h3).
- Kích thước render gấu: scene 4 = 37×43 px CSS @390, 71×82 px @1440; scene 8 = 36×42 px @390.
- Contrast palette: ink `#2F2A2E`, body `#51464C`, muted `#756B72`, rose-text `#9D5C72` trên `#FBF7F2` (đo WCAG ratio — xem log).
- Focus bàn phím: CDP `Input.dispatchKeyEvent` Tab thật, đọc `outlineStyle`; quét CSS `:focus`.

## Trạng thái

- Chưa push commit mới lên GitHub (chờ duyệt).
- Chờ user xác nhận: có muốn thêm/bớt component nào không.
