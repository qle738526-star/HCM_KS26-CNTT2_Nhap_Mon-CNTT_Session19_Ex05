**Bài 5 : Xây dựng cơ chế xác thực an toàn cho Crypto Wallet** 

***Thiết kế kiến trúc***

- Vẽ sơ đồ luồng dữ liệu giải thích cách 3 lớp bảo vệ phối hợp với nhau để ngăn chặn hacker kể cả khi chúng có mật khẩu.

Lớp 1: Tri thức (Something you know)          
 \- Nhập Mật khẩu     
       
 (Hacker có mật khẩu \-\> Vượt qua)  
         ↓   
 Lớp 2: Sở hữu vật lý (Something you have)   
 \- Mã OTP ( không có thiết bị, nhập sai mã và bị chặn)

 (Xác thực mã không khớp và khóa thành công)  
         ↓   
 Lớp 3: Sinh trắc học (Something you are)       
 \- FaceID / Vân tay   
(Không khớp và bị chặn)

***Xử lý bẫy (Edge Case)***

- **Nếu người dùng đang ở trên máy bay (không có internet/sóng điện thoại), làm sao họ vẫn có thể lấy mã OTP để thực hiện giao dịch?**  
- Dùng app Google Authenticator vì có thuật toán TOTP: nó không cần mạng hay SIM. Mã sẽ được tính toán bằng thuật toán. Cứ mỗi 30 giây thuật toán lại tự đổi một mã mới, dù thiết bị đang bật Chế độ máy bay thì mã sinh ra vẫn khớp với mã phía máy chủ.

        
