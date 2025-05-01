Dưới đây là bản dịch tiếng Việt cho tài liệu README của **Prior Swap Bot**:

---

# Prior Swap Bot

Một công cụ tự động đa ví dùng để hoán đổi token PRIOR trên mạng thử nghiệm PRIOR (PRIOR testnet).

## Tính Năng

- Hỗ trợ nhiều ví (thực hiện thao tác trên nhiều ví cùng lúc)  
- Tự động hoán đổi giữa các token PRIOR, USDC và USDT  
- Nhận token miễn phí từ faucet của PRIOR  
- Tối ưu thời gian chờ giữa các giao dịch  
- Giao diện dòng lệnh đơn giản  
- Tùy chỉnh số lượng token hoán đổi và số lần giao dịch  

## Yêu Cầu

- Node.js phiên bản 18 trở lên  
- Truy cập được vào PRIOR testnet  
- Private key của một hoặc nhiều ví Ethereum  

## Cài Đặt

1. Clone repository:
```bash
git clone https://github.com/Zack914/Prior-Testnet-Bot.git
cd Prior-Testnet-Bot
```

2. Cài đặt các thư viện cần thiết:
```bash
npm install
```

3. Tạo file cấu hình môi trường:
```bash
cp .env.example .env
```

4. Chỉnh sửa file `.env` và thêm địa chỉ RPC testnet của bạn:
```
RPC_URL=https://your-prior-testnet-rpc-url
```

5. Cấu hình private key cho ví của bạn:
```bash
cp private_keys.example.txt private_keys.txt
```

6. Mở file `private_keys.txt` và thêm private key (mỗi dòng một key):
```
# Thêm private key vào đây, mỗi dòng một key
# Các dòng bắt đầu bằng # sẽ bị bỏ qua
0x1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef
0xabcdef1234567890abcdef1234567890abcdef1234567890abcdef1234567890
```

## Cách Sử Dụng

Khởi động bot:
```bash
npm start
```

### Tùy Chọn Menu

1. **Hiển thị số dư tất cả ví** – Xem số dư token trong các ví đã nạp  
2. **Nhận token từ Faucet (Tất cả ví)** – Gửi yêu cầu nhận token testnet từ faucet cho tất cả ví  
3. **Tự động hoán đổi (Tất cả ví)** – Thực hiện hoán đổi token trên tất cả ví  
4. **Tự động hoán đổi (Một ví)** – Thực hiện hoán đổi trên một ví do bạn chọn  
5. **Tải lại private key** – Nạp lại danh sách private key từ file  
6. **Dừng hoạt động đang chạy** – Ngừng các giao dịch tự động  
7. **Thoát** – Thoát khỏi chương trình  

## Cấu Hình Tuỳ Chỉnh

Bạn có thể chỉnh sửa trực tiếp trong mã nguồn để thay đổi hành vi bot:

- `getRandomDelay()` – Điều chỉnh thời gian chờ giữa các giao dịch (mặc định 5–15 giây)  
- `getRandomAmount()` – Điều chỉnh lượng token ngẫu nhiên được hoán đổi (mặc định 0.001–0.01)  

## Địa Chỉ Hợp Đồng

- **USDC**: `0x109694D75363A75317A8136D80f50F871E81044e`  
- **USDT**: `0x014397DaEa96CaC46DbEdcbce50A42D5e0152B2E`  
- **PRIOR**: `0xc19Ec2EEBB009b2422514C51F9118026f1cD89ba`  
- **Router**: `0x0f1DADEcc263eB79AE3e4db0d57c49a8b6178B0B`  
- **Faucet**: `0xCa602D9E45E1Ed25105Ee43643ea936B8e2Fd6B7`  

## Bảo Mật

- Không chia sẻ file `.env` hoặc `private_keys.txt` của bạn  
- Các file này đã được đưa vào `.gitignore` để tránh bị đẩy lên Git  
- Chỉ sử dụng công cụ này trên testnet và **chịu trách nhiệm hoàn toàn khi sử dụng**  

## Giấy Phép

MIT License

