# BẾP AI — phiên bản có AI thật

## Có gì?
- Web mobile-first 6 màn hình.
- AI thật qua OpenAI Responses API.
- API key chỉ nằm ở server, không đưa vào trình duyệt.
- Gợi ý tối đa 3 món theo nguyên liệu, mục tiêu, thời gian, khẩu phần, ngân sách.
- Chế độ "Cùng tôi nấu": AI tạo từng bước cho người mới.
- Xử lý sự cố khi nấu.
- Có chế độ demo cục bộ nếu chưa cấu hình API key.

## Chạy trên máy
Yêu cầu Node.js 20+.

```bash
npm install
cp .env.example .env
```

Mở `.env` và thay:
`OPENAI_API_KEY=sk-...`

Sau đó:

```bash
npm start
```

Mở:
http://localhost:3000

## Đưa lên Internet
Có thể deploy thư mục này lên một dịch vụ Node.js hỗ trợ biến môi trường.
Thiết lập:
- `OPENAI_API_KEY`
- `OPENAI_MODEL=gpt-5.6-luna`
- `PORT` nếu nền tảng yêu cầu

Sau khi có URL HTTPS, dùng URL đó để tạo QR.

## An toàn API key
Không đặt `OPENAI_API_KEY` trong `index.html` hoặc JavaScript chạy ở trình duyệt.
Không commit `.env` lên GitHub.

## Lưu ý sản phẩm
BẾP AI là trợ lý nấu ăn, không phải công cụ y tế. Kcal chỉ là ước tính. Người dùng phải tự kiểm tra dị ứng và tình trạng thực phẩm.
