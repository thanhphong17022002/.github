# 📕 BỘ QUY TẮC QUẢN LÝ SOURCE CODE (CONTRIBUTING)

Chào mừng bạn tham gia dự án. Để đảm bảo chất lượng code và hệ thống hoạt động ổn định, BẤT KỲ AI (kể cả AI Assistant) khi can thiệp vào Source Code đều phải tuân thủ nghiêm ngặt 3 quy tắc vàng dưới đây:

## Quy tắc 1: CẤM PUSH TRỰC TIẾP LÊN NHÁNH `main`
- Nhánh `main` (hoặc `master`) là nhánh thiêng liêng nhất, chứa code đang chạy Production.
- **TUYỆT ĐỐI KHÔNG** được `git push` code trực tiếp thẳng lên nhánh `main`.
- Hệ thống đã bật **Branch Protection Rule**, mọi nỗ lực push trực tiếp sẽ bị GitHub từ chối.

## Quy tắc 2: Quy trình làm việc bắt buộc (Pull Request Workflow)
Bất cứ khi nào làm một tính năng mới hoặc sửa lỗi, bạn phải làm theo đúng 4 bước sau:
1. **Tạo nhánh mới:** Từ nhánh `main` mới nhất, tạo một nhánh rẽ nhánh có tiền tố rõ ràng:
   - Làm tính năng mới: `feature/ten-tinh-nang`
   - Sửa lỗi khẩn cấp: `hotfix/ten-loi`
2. **Code & Commit:** Chủ động gộp các commit rác lại với nhau, giữ lịch sử sạch đẹp. Không đưa các file rác (như `bin`, `obj`, `.vs`) lên git.
3. **Tạo Pull Request:** Lên GitHub mở Pull Request vào nhánh `main`. 
   - **BẮT BUỘC** điền đầy đủ form `PULL_REQUEST_TEMPLATE`.
   - **BẮT BUỘC** đính kèm ảnh chụp màn hình Trước/Sau (nếu có đổi UI).
   - Tự tích hoàn thành các mục Checklist trong Form.
4. **Từ khóa thần thánh:** Nếu PR này giải quyết một Issue đang mở (VD: Issue #10), bắt buộc phải có dòng chữ `Resolves #10` trong nội dung PR để GitHub tự động đóng lỗi khi gộp code.

## Quy tắc 3: Code sạch (Clean Code) trước khi Commit
Trước khi đẩy code lên nhánh của bạn, hãy tự kiểm tra lại (Self-Review):
- Không để sót `console.log()` hoặc `Console.WriteLine()` dùng để debug.
- Không comment lại những đoạn code thừa thãi, hãy xóa hẳn nó đi (vì Git đã lưu lại lịch sử rồi).
- Nếu sửa đổi liên quan đến cấu trúc hệ thống, bắt buộc phải cập nhật lại tài liệu `.md` tương ứng.

---
*Mọi Pull Request không tuân thủ các quy tắc trên sẽ bị Reject (từ chối gộp code) ngay lập tức.*
