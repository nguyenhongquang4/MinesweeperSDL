MINESWEEPER
Contents
1.	Giới thiệu về bản thân	1
2.	Giới thiệu về Game	1
3.	Cách thức chơi game	1
4.	Thông tin về các items trong Game	2
5.	Một vài hình ảnh của Game	2
6.	Cấu trúc Game.	2
7.	Cách cài đặt.	2
8.	Kỹ thuật, công nghệ sử dụng	2
9.	Nguồn tham khảo	2
10.	Kết luận	2
a.	Ưu điểm	2
b.	Nhược điểm	3
c.	Bài học kinh nghiệm	3
d.	Hướng phát triển Game trong tương lai	3
e.	Mức điểm mong muốn 8.5+/10	3


1.	Giới thiệu về bản thân
•	Họ và tên: Nguyễn Hồng Quang
•	Mã sinh viên: 22028263
•	Lớp học phần: 2324II_INT2215_70
2.	Giới thiệu về Game
Minesweeper là một game kinh điển đối với nhiều người. Game sẽ hiển thị một ma trận các ô vuông. Nhiệm vụ của người chơi là cần phải  tính toán về số lượng mìn xung quanh, lựa chọn ô không có mìn, cũng như là có một chút may mắn nữa. 
Video giới thiệu về game:
3.	Cách thức chơi game
Bạn phải tìm cách né/ bỏ qua các vị trí có mìn. Con số hiển thị tượng trưng số mìn có trong các ô xung quanh. 
Nếu ô không có mìn, Các ô xung quanh sẽ đồng loạt tự hiển thị cho đến khi xuất hiện ô có mìn.
Khi chọn trúng ô có mìn, trò chơi kết thúc và bạn thua.

4.	Thông tin về các items trong Game
•	 : Đây là ô chưa mở, trong ô có thể chứa mìn, hoặc là gợi ý có bao nhiêu mìn xung quanh.

•	 : Đây là các ô (tiles) đã được mở trong Game. Mỗi con số đại diện cho số mìn ở các ô xung quanh nó. 
•	 : Đây là item cờ (flag), bạn có thể sử dụng item này để có thể đánh dấu ô mà bạn nghi ngờ /chắc chắn ô đó có mìn. 
•	 : Đây là item mìn (bomb), một khi mở trúng ô, trò chơi kết thúc.

5.	Một vài hình ảnh của Game
6.	Cấu trúc Game.
•	Button.cpp: Một lớp xử lý khung chữ, các sự kiện, xử lý di chuyển và click chuột
•	Texture.cpp: Xử lý, tải và hiển thị các đối tượng ảnh, phông chữ, màu chữ.
•	Variables.cpp: Khai báo và khởi tạo các biến, đối tượng được sử dụng trong Game.
•	MainFunction.cpp: Khởi tạo và xử lý các chức năng chính trong Game bao gồm: tạo Menu, xử lý thuật toán dò mìn, hiện thị ô.
7.	Cách cài đặt.
8.	Kỹ thuật, công nghệ sử dụng
•	Sử dụng các tính năng trong thư viện SDL bao gồm: xử lý đồ họa, font chữ, âm thanh, thao tác chuột, bàn phím, …
•	Sử dụng class để có thể refactor code tiện lợi, dễ đọc hơn.
•	Kết hợp thư viện SDL với làm việc với file để load và xử lý ảnh, font chữ và âm thanh
•	Sử dụng thuật toán BFS trong đồ thị để hiển thị các ô. 
9.	Nguồn tham khảo
•	Tham khảo code trên lazy.foo về kĩ thuật load và render texture, load âm thanh.
•	Lấy nguồn ảnh và âm thanh, font chữ trên itch.io
10.	Kết luận
a.	Ưu điểm
•	Game đã phát triển được giao diện đồ họa cơ bản.
•	Người chơi có thể lựa chọn 3 cấp độ khó với ma trận ô và số lượng mìn khác nhau
•	Có phần tính điểm và quy tắc tính điểm của mỗi độ khó là khác nhau

	Ô không có mìn xung quanh	Ô có số lượng mìn xung quanh
Easy	+10	+5
Medium	+20	+10
Hard	+50	+25
•	Có phần chơi lại (play again) mỗi khi game over hoặc thắng trò chơi.
b.	Nhược điểm
•	Giao diện đồ họa vẫn chưa được đẹp mắt, vẫn ở mức cơ bản
•	File MainFunction.cpp vẫn chưa tối ưu hóa hoàn toàn các mức độ khó. Chưa chia thành các file nhỏ để có thể thuận tiện đọc và theo dõi.
•	Trong lúc làm game, có một vài biến, đối tượng em tạo nhưng không sử dụng mà vẫn chưa xóa -> code chưa hoàn toàn refresh.
c.	Bài học kinh nghiệm
•	Có thể phát triển một game hoàn chỉnh, từ logic game, xử lý sự kiện game, cải thiện về phần refactor code.
•	Có thể thao tác và làm việc với file, quản lý file, chia file sao cho có thể dễ đọc, dễ theo dõi.
•	Biết sử dụng các công cụ hỗ trợ đồ họa
d.	Hướng phát triển Game trong tương lai
•	Tạo danh sách lưu trữ tên người chơi và điểm (bảng xếp hạng)
•	Cải thiện lại phần đồ họa để có giao diện thân thiện với người dùng.
•	Có thể thêm chức năng về thời gian. Thời gian chơi càng sớm, điểm càng cao.
e.	Mức điểm mong muốn 8.5+/10
