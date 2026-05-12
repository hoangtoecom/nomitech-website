# Research POS Platform — Sapo vs Pancake

> Saved: 2026-05-12 (session trước khi migrate sang Mac)
> Status: Chưa quyết — research để anh suy nghĩ trên máy mới
> Context: Nomitech online-first, 10-50 đơn/day plan, web là landing tĩnh hiện tại

## Tóm tắt quyết định

Đã loại bỏ:
- ❌ **KiotViet** — Anh đổi ý, chưa phù hợp giai đoạn đầu doanh thu thấp
- ❌ **Self-build full POS** — Risk cao với non-tech + sắp khai trương, multi-channel sync phức tạp + HDDT compliance

Còn lại 2 ứng viên:
- 🟢 **Sapo Pro** (399k/tháng, 249k nếu ký 2 năm)
- 🟡 **Pancake POS** (POS free, Chat có phí ẩn)

## So sánh

| Tiêu chí | Sapo Pro | Pancake POS + Chat |
|---|---|---|
| DNA gốc | Retail-first (POS bán lẻ) | Conversational-first (chatbot FB) |
| Giá tháng | 399k (hoặc 249k ký 2 năm) | POS: 0đ; Chat: ~90k+ (2023 ref) |
| Phí setup | 1tr (miễn nếu ký 2 năm) | 0đ |
| Sync Shopee/TikTok | Qua Omnichannel | NATIVE (mạnh nhất VN) |
| Chatbot inbox auto | Không có | Có (gói Chat) |
| Website TMĐT | Có Sapo Web (Nomitech không cần) | Không có |
| MCP tools | 105 tool (npx, dễ) | 23 tool (Bun runtime, khó cài) |
| Pricing transparency | ✅ Công khai | ❌ Phải liên hệ sales |
| Trial | 14 ngày miễn phí | 14 ngày miễn phí |

## Action plan khi qua Mac

### Bước 1: Đăng ký trial cả 2

- **Sapo Pro**: https://www.sapo.vn/dang-ky-su-dung-mien-phi.html
- **Pancake POS**: https://pancake.vn → đăng ký POS (free)

### Bước 2: Hỏi sales Pancake về giá thật 2026

- Pancake POS free đến giới hạn nào?
- Pancake Chat gói thấp nhất giá bao nhiêu?

### Bước 3: Test cùng workflow trên cả 2

Setup mẫu 5-10 sản phẩm linh kiện PC:
- Kết nối Shopee Shop trial
- Kết nối TikTok Shop trial
- Test sync inventory 2 chiều
- Test chatbot reply tự động (chỉ Pancake có)
- Compare UX + tốc độ + báo cáo

### Bước 4: Quyết định dựa trên data thực tế trial

Tiêu chí ưu tiên cho Nomitech:
1. Sync Shopee/TikTok mượt = priority #1
2. Chatbot inbox = priority #2 (tư vấn build PC cho khách)
3. Báo cáo dễ hiểu = priority #3
4. Giá < 500k/tháng = priority #4

## URLs tham khảo

- Sapo bảng giá: https://www.sapo.vn/bang-gia.html
- Pancake pricing: https://pancake.vn/pricing
- Sapo MCP (open source, npx cài dễ): https://www.npmjs.com/package/sapo-mcp
- Pancake MCP (open source, cần Bun): https://github.com/nguyennguyenit/pancake-pos-mcp
- Sapo MCP docs: https://sapo-mcp-overview.pages.dev/
- Pancake MCP docs: https://pancake-pos-mcp-overview.pages.dev/

## Lưu ý quan trọng

**MCP ≠ Platform**: 2 MCP đều open source/miễn phí, nhưng để dùng được cần có TÀI KHOẢN TRẢ PHÍ ở Sapo/Pancake. MCP chỉ là cầu nối Claude AI ↔ Platform.

**Cả 2 MCP đều build bởi 1 dev cá nhân** `nguyennguyenit` (không phải official từ Sapo/Pancake) → rủi ro maintenance về lâu dài. Nếu chọn vì MCP, lưu ý điểm này.

## Em (Claude) sẽ pick up gì khi anh quay lại

Khi anh trên Mac mở file này hoặc gõ "tiếp tục vụ chọn POS Nomitech", em sẽ:
- Đọc file này để có context đầy đủ
- Áp dụng 5 nuance writing humility nếu cần viết copy cho Nomitech
- Đọc PROJECT.md của Nomitech (nếu đã có) để biết tech stack web
- Tiếp tục từ Bước 1 trial đăng ký nếu anh chưa làm

## Trạng thái lúc tạm dừng

- Anh đang quyết tâm tối ưu chi phí giai đoạn đầu (low volume <30 đơn/day)
- Web nomitech.vn = static HTML landing only, KHÔNG có cart/checkout
- Strategy: bán chủ yếu qua Shopee + TikTok Shop, web làm brand showcase
- Sẵn sàng trial cả 2 platform để có data thực tế trước khi quyết
