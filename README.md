# n8n-docker
Cài N8N sử dụng docker compose kết hợp với Cloudflare Tunnel

Bước 1: Vào Cloudflare Tunnel thiết lập để lấy token
Bước 2: Thay thế token nhận được vào nội dung sau và copy tất cả:

docker run -d --name cloudflared --restart unless-stopped --network host cloudflare/cloudflared:latest tunnel --no-autoupdate run --token thay_token

Bước 3: Paste cả cụm trên vào docker

Bước 4: Trong cấu hình của Cloudflare Tunnel. Mục Service chọn Type là HTTP - URL localhost:5678 là xong

