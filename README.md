# Hướng dẫn cài đặt và chạy ứng dụng

> Lưu ý: Cần có **git** để clone repo!

## 1. Clone repository chính

```bash
git clone https://github.com/ddang770/chatbot-utt.git
cd chatbot-utt
```

## 2. Clone các repository con

Clone **backend**:

```bash
git clone https://github.com/ddang770/utt-chatbot-backend.git backend
```

Clone **frontend**:

```bash
git clone https://github.com/ddang770/utt-chatbot-frontend.git frontend
```

> Lưu ý: Sau khi clone, thư mục có tên lần lượt là **backend** và **frontend**.

## 3. Cấu hình biến môi trường

Sau khi đã có **backend** và **frontend**, đổi tên file `.env.example` thành `.env`:

```bash
mv ./.env.example ./.env
```

Sau đó mở file `.env` và thêm các key cần thiết:

```env
OPENAI_KEY=your_openai_api_key_here
OPENROUTER_API_KEY=your_openrouter_api_key_here
```

## 4. Build ứng dụng với Docker
> Lưu ý: Cần phải có **Docker**, bạn có thể tải Docker Desktop tại đây: https://www.docker.com/get-started/

Build sẽ mất 1 khoảng kha khá thời gian!

```bash
docker-compose build
```

Sau khi build xong ta có thể khởi chạy ứng dụng

```bash
docker-compose up -d
```

- Client app → http://localhost:3000
- Server → http://localhost:8000
- Database → running internally

Vậy là xong, truy cập vào http://localhost:3000 để sử dụng

---
# Các url của app
- Home page: http://localhost:3000
- Admin page: http://localhost:3000/admin/dashboard