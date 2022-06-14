<header>
<h1> Đồ Án môn lập trình mạng căn bản NT106.M21 - Nhóm 4</h1>
 
  <h2> Thành viên thực hiện : </h2>
  
<p>
Võ Thanh Phong		19522017  <br>
Trương Huỳnh Quý		19522110 <br>
Huỳnh Quang Vũ		19522532  <br>
Đỗ Trần Phương Nam	19520749 <br>
Lưu Tinh Anh		20520386    <br>
 </p>
</header>

<body>
  
<div>

  <h2> Đặt vấn đề </h2>
  <p> Bạn đang stress, đang buồn chán và muốn tìm một trò chơi để giải trí ? </p>
  <p> 
    - Cờ vua là một môn thể thao trí lực, là cuộc đấu trí giữa hai đấu thủ trên phạm vi bàn cờ. Trong quá trình thi đấu, hai đấu thủ không chỉ tranh đua với nhau về năng lực thi đấu (sự chuẩn bị thể lực, kỹ thuật, chiến thuật, chiến lược và tâm lý thi đấu), mà còn là sự đấu trí quyết liệt về năng lực tính toán, phán đoán sự đáp trả của đối phương sau mỗi nước cờ. <br>
 - Với đặc thù là một môn thể thao trí tuệ, lượng vận động chủ yếu là lượng vận động tâm lý tác động trực tiếp vào quá trình tư duy của người tập, cho thấy sự tác động rõ nét của môn cờ vua đến năng lực trí tuệ nói riêng (đặc biệt là năng lực tư duy) và các năng lực tâm lý nói chung.<br>
- Cờ vua không chỉ là một trò chơi giải trí lành mạnh trong những lúc nhàn rỗi, giúp người học nâng cao khả năng học các môn khoa học tự nhiên mà còn là một phương tiện rất tốt trong việc giúp người chơi phát triển tư duy, rèn luyện tính kỷ luật, lòng tự trọng và tinh thần độc lập. <br>
- Từ những lợi ích mà trò chơi cờ vua mang lại, nhóm bọn em quyết định chọn game cờ vua làm đề tài của nhóm bọn em. Vừa có thể giải trí sau những giờ học tập căng thẳng, vừa phát triển trí tuệ mà còn nâng cao tinh thần đồng đội khi có thể chơi game cùng những người bạn.</p>
</div>
<div>
  <h2> Flow app </h2>
  <p>
    <img src="https://user-images.githubusercontent.com/91233510/173536843-8f704e4c-c79a-4077-b3f1-132aac339ec4.png">
   <br><br>
- Ban đầu khi bắt đầu start thì người chơi không cập nhật bàn cờ thì sẽ đi qua bước PLAY GAME. <br>
- Khi người chơi di chuyển quân cờ thì sẽ kiểm tra hiệu lực của quân cờ nếu không thành công thì quân cờ sẽ quay lại vị trí cũ và bắt đầu vào ô di chuyển quân cờ rồi tiếp tục với kiểm tra hiệu lực quân cờ. Nếu thành công thì sẽ chuyển qua kiểm tra việc loại bỏ quân cờ.Nếu không thành công thì sẽ sẽ cập nhật quân cờ tại vị trí đó và thay đổi lượt. Còn nếu mà đúng thì sẽ kiểm tra có loại bỏ quân Vua hay không nếu không loại bỏ thì sẽ đưa quân cờ vào mục loại bỏ và cập nhật lại thay đổi lượt. Nếu mà kiểm tra loại quân Vua thì Win Game. <br>
- Tiếp tục, nếu trong bắt đầu mà mình cập nhật bàn cờ nếu mà object nó di chuyển ( tức là các ô trên mỗi quân cờ ) thì sẽ thêm mới object, cập nhật lại vị trí và khởi tạo lại vị trí trước đó. Còn nếu không thì sẽ quay lại cập nhật bàn cờ. Rồi khi đã có đủ 32 object trên bàn cờ thì sẽ bổ nhiệm mỗi vị trí đó vào các nhiệm vụ của quân cờ. Và đã xong thì sẽ có thể bắt đầu trò chơi.<br>
</p>
  <h2>User stories</h2>
    <img src="https://user-images.githubusercontent.com/91233510/173538012-f0573f77-3c3d-415a-891f-c8c11b0d1f4f.png">
  <br>
  <p>
    - User stories dựa trên dạng end user là Player(người chơi) truy cập. Có Epic là Cờ vua (Epic là một thuật ngữ trong phương pháp quản lý dự án Agile chỉ đến 1 câu chuyện người dùng lớn (large user story) có thể chia chẻ thành các user stories nhỏ hơn), các Epic nhỏ hơn là Màn hình chính, Bắt đầu mới, Cài đặt và Thoát. Trong mỗi epic nhỏ đó có các user stories như ta thấy trên hình. Ta có thể thêm task và subtask sau mỗi stories để cụ thể hơn trong việc xây dựng phần mềm.
  </p>
  <h2>Data flow</h2>
    <img src="https://user-images.githubusercontent.com/91233510/173539510-077e20ad-4735-4889-82cf-4cdd90c1b16e.png">
  <br>
  <p>
-	Khi client yêu cầu kết nối thì sẽ gởi yêu cầu kết nối với port được chỉ định. Server sẽ accept và phản hồi lại trạng thái kết nối.<br>
-	Khi kết nối thành công thì ta gởi một yêu cầu về việc xem và quan sát những người chơi đánh cờ và Server sẽ phản hồi ta những thông tin về board, moving, pieces, … rồi từ đó Client sẽ show ra quá trình đó lên màn hình chính.<br>
-	Tương tự vây, yêu cầu disconnect, server sẽ phản hồi và ngừng kết nối với client.<br>

  </p>
    <br><br>
</div>

<footer>
  <h1> Cám ơn cô và các bạn đã theo dõi </h1>
</footer>
