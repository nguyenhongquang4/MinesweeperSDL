# MINESWEEPER

- [Giới thiệu về bản thân](#giới-thiệu-về-bản-thân)
- [Giới thiệu về Game](#Giới-thiệu-về-Game)
- [Hướng dẫn chơi Game](#Hướng-dẫn-chơi-Game)
- [Thông tin về các items trong Game](#Thông-tin-về-các-items-trong-Game)
- [Một vài hình ảnh của Game](#Một-vài-hình-ảnh-của-Game)
- [Cấu trúc Game](#Cấu-trúc-Game)
- [Cách cài đặt](#Cách-cài-đặt)
- [Kỹ thuật, công nghệ sử dụng](#Kỹ-thuật-,-Công-nghệ-sử-dụng)
- [Nguồn tham khảo](#Nguồn-tham-khảo)
- [Kết luận](#Kết-luận)
  	- [Ưu điểm](#Ưu-điểm)
   	- [Nhược điểm](#Nhược-điểm)
   	- [Bài học kinh nghiệm](#Bài-học-kinh-nghiệm)
   	- [Hướng phát triển Game trong tương lai](#Hướng-phát-triển-Game-trong-tương-lai)
   	- [Nguyện vọng về điểm](#Nguyện-vong-về-điểm)





## Giới thiệu về bản thân
•	Họ và tên: Nguyễn Hồng Quang

• Mã sinh viên: 22028263

•	Lớp học phần: 2324II_INT2215_70


## Giới thiệu về Game
Minesweeper là một game kinh điển đối với nhiều người. Game sẽ hiển thị một ma trận các ô vuông. Nhiệm vụ của người chơi là cần phải  tính toán về số lượng mìn xung quanh, lựa chọn ô không có mìn, cũng như là có một chút may mắn nữa. 

Video giới thiệu về game:


## Hướng dẫn chơi Game
Bạn phải tìm cách né/ bỏ qua các vị trí có mìn. Con số hiển thị tượng trưng số mìn có trong các ô xung quanh. 
Nếu ô không có mìn, Các ô xung quanh sẽ đồng loạt tự hiển thị cho đến khi xuất hiện ô có mìn.
Khi chọn trúng ô có mìn, trò chơi kết thúc và bạn thua.


## Thông tin về các items trong Game
•	![tile](https://github.com/user-attachments/assets/fd6aa6be-1ffc-4f39-b38a-205191d934e1): Đây là ô chưa mở, trong ô có thể chứa mìn, hoặc là gợi ý có bao nhiêu mìn xung quanh.

•	![number](https://github.com/user-attachments/assets/d389ea9f-4a97-4be7-b39e-428fa2127cbe): Đây là các ô (tiles) đã được mở trong Game. Mỗi con số đại diện cho số mìn ở các ô xung quanh nó.

•	![flag](https://github.com/user-attachments/assets/1bc51115-f0d3-4988-a2e1-bbd411e72bf2): Đây là item cờ (flag), bạn có thể sử dụng item này để có thể đánh
 dấu ô mà bạn nghi ngờ /chắc chắn ô đó có mìn. 
 
• ![bomb](https://github.com/user-attachments/assets/25db9cae-e727-493a-b37e-3a4874675c0b): Đây là item mìn (bomb), một khi mở trúng ô, trò chơi kết thúc.

• ![backicon1](https://github.com/user-attachments/assets/4371007b-e684-44dd-b941-e640bc88e25b): Đây là item back, có thể quay lại chế độ khó của Game.


## Một vài hình ảnh của Game

## Cấu trúc Game.
•	Button.cpp: Một lớp xử lý khung chữ, các sự kiện, xử lý di chuyển và click chuột.

•	Texture.cpp: Xử lý, tải và hiển thị các đối tượng ảnh, phông chữ, màu chữ.

•	Variables.cpp: Khai báo và khởi tạo các biến, đối tượng được sử dụng trong Game.

•	MainFunction.cpp: Khởi tạo và xử lý các chức năng chính trong Game bao gồm: tạo Menu, xử lý thuật toán dò mìn, hiện thị ô.


## Cách cài đặt.
• 
## Kỹ thuật, công nghệ sử dụng
•	Sử dụng các tính năng trong thư viện SDL bao gồm: xử lý đồ họa, font chữ, âm thanh, thao tác chuột, bàn phím, …

•	Sử dụng class để có thể đóng gói các đối tượng, phương thức và refactor code tiện lợi, dễ đọc hơn.

•	Kết hợp thư viện SDL với làm việc với file để load và xử lý ảnh, font chữ và âm thanh.

•	Sử dụng thuật toán BFS trong đồ thị để hiển thị các ô. 

## Nguồn tham khảo
•	Tham khảo code trên lazy.foo về kĩ thuật load và render texture, load âm thanh.

•	Lấy nguồn ảnh và âm thanh, font chữ trên itch.io

## Kết luận

### Ưu điểm
•	Game đã phát triển được giao diện đồ họa cơ bản.

•	Người chơi có thể lựa chọn 3 cấp độ khó với ma trận ô và số lượng mìn khác nhau

•	Có phần tính điểm và quy tắc tính điểm của mỗi độ khó là khác nhau

| Độ khó | Ô có mìn xung quanh | Ô không có mìn xung quanh |
|--------|---------------------|---------------------------|
|  Easy  | +5                  | +10                       |
| Medium | +10                 | +20                       |
| Hard   | +25                 | +50                       |

•	Có phần chơi lại (play again) mỗi khi game over hoặc thắng trò chơi.

### Nhược điểm
•	Giao diện đồ họa vẫn chưa được đẹp mắt, vẫn ở mức cơ bản

•	File MainFunction.cpp vẫn chưa tối ưu hóa hoàn toàn các mức độ khó. Chưa chia thành các file nhỏ để có thể thuận tiện đọc và theo dõi.

### Bài học kinh nghiệm
•	Có thể phát triển một game hoàn chỉnh, từ logic game, xử lý sự kiện game, cải thiện về phần refactor code.

•	Có thể thao tác và làm việc với file, quản lý file, chia file sao cho có thể dễ đọc, dễ theo dõi.

•	Biết sử dụng các công cụ hỗ trợ đồ họa.

### Hướng phát triển Game trong tương lai
•	Tạo danh sách lưu trữ tên người chơi và điểm (bảng xếp hạng).

•	Cải thiện lại phần đồ họa để có giao diện thân thiện với người dùng.

•	Có thể thêm chức năng về thời gian. Thời gian chơi càng sớm, điểm càng cao.

### Nguyện vọng về điểm
Mức điểm mong muốn 8.5+/10.


