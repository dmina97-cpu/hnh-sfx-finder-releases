# hnh-sfx-finder-releases
Bản phát hành HNH SFX Finder cho DaVinci Resolve Studio
Plugin giúp quản lí, tìm, nghe thử và chèn sound effect, video, hình ảnh từ thư viện trên máy vào timeline Resolve. Tìm nhanh bằng tiếng Việt hoặc tiếng Anh, quản lý tags và Favorites ngay trong một cửa sổ.

Anh em cần hỏi cách dùng, báo lỗi hoặc muốn góp ý thêm tính năng thì nhắn Zalo cho mình nhé.

Mới: Tab Hình ảnh và Video
Ba tab Âm thanh, Hình ảnh và Video dùng chung thư viện, tags và Favorites. Thêm folder trong Thư viện; mỗi tab chỉ hiện đúng loại tài nguyên. Tags/Favorites của ảnh và video cũng được xuất/nhập cùng bản sao lưu.

Trong tab Hình ảnh hoặc Video, tìm theo tên/folder/tags, chọn folder từ danh sách hoặc lọc Yêu thích/Gần đây. Kết quả chia trang để thư viện lớn vẫn nhẹ. Chọn một thẻ để xem preview; thumbnail được tạo khi thẻ xuất hiện trên màn hình và lưu cache cục bộ.

Ảnh: chọn thời lượng bằng giây, chọn track V1/V2… rồi Chèn tại Playhead. Nếu Resolve nhận các ảnh đánh số thành image sequence, bật Show Individual Frames trong Media Storage và import lại ảnh riêng.

Video: dùng player để xem/tua; nút In/Out lấy vị trí đang xem, hoặc nhập giây và bật Chèn đoạn In/Out. Toàn bộ bỏ vùng chọn. Mặc định chèn phần hình. Bật Kèm âm thanh & liên kết clip, chọn audio track A1/A2… để lấy cả tiếng; cả hai dùng chung In/Out và vị trí playhead. Cần vùng trống trên cả hai track. Hỗ trợ một track âm thanh nguồn nhúng trong video; nguồn nhiều track hoặc audio liên kết ngoài cần xử lý trong Resolve. Nếu lỗi sau khi chèn, plugin thử gỡ các clip vừa tạo và báo kết quả; kiểm tra timeline nếu thông báo chưa gỡ được.

Nút Tải lại track đọc timeline đang mở. Track khóa không được chọn; cần có track video trên timeline. Ảnh/video lỗi preview do codec vẫn có thể thử Import hoặc chèn bằng Resolve. Khả năng nhập phụ thuộc định dạng được Resolve hỗ trợ; plugin không chuyển mã.

Chọn loại tài nguyên cho từng thư mục
Khi thêm folder, tích Âm thanh, Hình ảnh hoặc Video (có thể chọn nhiều loại). Mặc định theo tab đang mở. Trong Thư viện, bấm Loại quét cạnh folder để sửa và quét lại. Folder cũ chưa có lựa chọn vẫn quét cả ba loại như trước.

Bỏ một loại chỉ bỏ khỏi index. Tags/Favorites vẫn giữ và xuất hiện lại khi bật loại đó rồi quét. Nếu các thư viện lồng nhau, một file vẫn hiện khi được ít nhất một folder cho phép quét. Giới hạn loại giúp giảm đọc thông tin và kích thước index, nhưng vẫn cần duyệt cây folder.

Ngày thêm, lọc nhanh và danh sách tags
Ngày thêm là lần đầu plugin ghi nhận đường dẫn file, không phải ngày tạo hoặc ngày sửa file trên ổ đĩa. File mới được ghi nhận từ bản 0.7.2; file cũ không có dữ liệu ngày sẽ hiện Chưa rõ ngày thêm. Quét lại, sửa nội dung hoặc tắt/bật loại quét không làm đổi ngày đã ghi nhận.

Chọn Hôm nay, 7 ngày qua (hôm nay và 6 ngày trước), Khoảng ngày hoặc Chưa rõ ngày thêm. Các mốc dùng ngày trên máy; khoảng ngày bao gồm cả ngày kết thúc. Rê chuột vào tên/thẻ file để xem thời điểm cụ thể. Bản sao lưu mới giữ ngày khi chuyển sang thư viện mới.

Danh sách tags hiển thị nhãn đã gắn và số file của loại tài nguyên đang mở, không phụ thuộc bộ lọc ngày/search. Chọn tag để lọc. Nếu chưa có tag, chọn file → nhập các tag cách nhau bằng dấu phẩy → Lưu tags. Bỏ lọc ngày / tag không xóa tags đã lưu.

Chọn nhiều file: tags và Favorites
Bấm Chọn nhiều rồi tích checkbox cạnh các file. Chọn các file đang hiện áp dụng cho trang hiện tại (SFX tối đa 500 kết quả). Có thể chọn tiếp ở trang khác; đổi tab sẽ bỏ chọn, đổi bộ lọc sẽ bỏ các lựa chọn không còn khớp.

Nhập tags cách nhau bằng dấu phẩy rồi Thêm tag hoặc Xóa tag. Thêm tag giữ các tags cũ; Xóa tag chỉ xóa nhãn đã nhập, không xóa file. Thêm/Bỏ yêu thích áp dụng cho các file đã chọn. Tối đa 30 tags mỗi file. Dữ liệu được giữ trong bản sao lưu như chỉnh từng file.

Sidebar Tags và thêm tag nhanh
Bắt đầu trong 1 phút
Mở Thư viện → + Thêm thư mục, chọn folder chứa SFX. Plugin đọc cả thư mục con.
Gõ từ khóa, ví dụ whoosh nhanh hoặc tiếng kim loại. Chọn một kết quả rồi bấm Preview để nghe thử.
Trong Resolve, mở project và timeline, đặt playhead tại vị trí cần chèn.
Chọn audio track trong plugin, rồi bấm Insert tại Playhead. Nếu chỉ cần đưa file vào Media Pool, bấm Import.
Tìm kiếm, bộ lọc và duyệt folder
Tìm theo tên file/thư mục, hỗ trợ từ khóa Việt–Anh và tìm gần đúng. Các nút Whoosh, Impact, UI, Riser… giúp tìm nhanh theo nhóm.

Kết hợp bộ lọc định dạng, thư viện, tags và thời lượng Từ–Đến (giây). File chưa xác định thời lượng có thể chưa xuất hiện khi đang lọc thời lượng.

Bật Duyệt thư mục để xem cây folder. Bấm tên folder để lọc cả thư mục con; bấm mũi tên để mở nhánh. Tất cả SFX bỏ lọc folder, các bộ lọc khác vẫn giữ. Ẩn bảng folder không tự bỏ lọc.

Nút Tương tự tìm các sound gần loại theo từ khóa của file đang chọn; đây không phải so sánh nội dung âm thanh. Mở thư mục hoặc chuột phải kết quả để tìm file trong Explorer.

Chèn nhạc vào In/Out Timeline
Đánh I và O trên timeline Resolve. Trong tab Âm thanh, chọn file và track A đích, đổi Chèn theo thành In/Out Timeline. Plugin đọc vùng khi quay lại cửa sổ; nút Đọc lại I/O cập nhật thủ công. Khi bấm chèn, vùng được đọc lại từ Resolve, không phụ thuộc playhead.

Điểm In trong plugin là điểm bắt đầu lấy nhạc (mặc định 0 giây); độ dài lấy từ timeline. Điểm Out của nhạc vẫn dùng nghe thử, không giới hạn vùng chèn này. Nhạc thiếu thời lượng sẽ báo lỗi, chưa tự lặp/kéo giãn. Track phải mở khóa, trống trong vùng I/O và chừa 2 frame sau Out để tránh va chạm do làm tròn. Hỗ trợ một track audio nguồn; mapping nhiều track hoặc audio liên kết ngoài cần xử lý trong Resolve.

Ưu tiên dấu audio; nếu không có dấu audio thì dùng dấu video. Nếu thiếu một mốc, cần đánh đủ I/O. Plugin khôi phục dấu sau chèn; nếu bạn đổi dấu trong lúc chèn sẽ giữ dấu mới. Sai số làm tròn tối đa 2 frame được báo, sai lệch lớn hơn sẽ thử gỡ clip mới. Bản Resolve thiếu API sẽ báo rõ; vẫn dùng Playhead như trước.

Preview, waveform, In/Out và âm lượng
Bấm Preview hoặc nút ▶ ở kết quả để nghe/dừng. Bật Auto preview để nghe khi chuyển lựa chọn. Waveform cho phép bấm để tua.

Tua tới điểm bắt đầu rồi bấm In [I], tua tới điểm kết thúc rồi bấm Out [O]; cũng có thể nhập thời gian bằng giây. Điểm Out phải lớn hơn In và nằm trong thời lượng file.

Bật Lặp đoạn để nghe lặp vùng chọn. Khi có vùng In/Out, nút chèn đổi thành Insert đoạn chọn. Bấm Toàn bộ để bỏ vùng chọn. Import vẫn đưa file gốc vào Media Pool.

Âm lượng nghe thử và Tắt tiếng chỉ điều khiển preview trong plugin, không thay đổi file nguồn hoặc âm lượng clip trên timeline.

Tags, Favorites và Recent
Chọn một SFX → nhập tag vào ô Tag cho SFX đang chọn, cách nhau bằng dấu phẩy → bấm Lưu tags. Ví dụ: chuyển cảnh, nhanh, yêu thích. Muốn sửa/xóa tag thì chỉnh danh sách rồi lưu lại.

Bật Hiện tag cạnh tên SFX để xem nhãn trong kết quả. Dùng ô Lọc tag để tìm theo tag.

Bấm ngôi sao cạnh file để thêm/bỏ Favorites, rồi chọn ★ Yêu thích để xem. Gần đây giúp tìm lại các file đã dùng. Tags và Favorites lưu trong dữ liệu plugin, không ghi vào file âm thanh gốc.

Smart Collections — lưu bộ lọc thường dùng
Đặt từ khóa, folder và các bộ lọc cần dùng → nhập Tên bộ lọc để lưu → bấm Lưu bộ lọc. Chọn lại trong Smart Collections để áp dụng.

Khi đang chọn một bộ lọc đã lưu, bấm Lưu bộ lọc sẽ cập nhật bộ đó. Muốn tạo bộ mới, chọn dòng Smart Collections trống trước. Xóa bộ lọc chỉ xóa bộ lọc đã lưu, không xóa SFX.

Sao lưu và chuyển sang máy khác
Máy cũ: vào Thư viện → Sao lưu & chuyển thư viện → Xuất bản sao lưu. Có thể chọn kèm waveform cache và Recent/lượt sử dụng.
Chép file .hnhbackup sang máy mới. Gói chứa index, tags, Favorites, Smart Collections và tùy chọn plugin; không chứa audio, nên cần chép thư viện âm thanh riêng.
Máy mới: chọn Nhập bản sao lưu. Giữ đường dẫn nếu giống máy cũ, hoặc Chọn thư mục mới cho từng thư viện.
Bấm Đối chiếu file, xem kết quả và chọn file cho những mục cần xác nhận. File có nội dung giống hệt có thể tự ghép kể cả đổi tên. Chỉ trùng tên hoặc có nhiều bản giống nhau thì cần xác nhận.
Chọn các tùy chọn muốn nhập rồi bấm Áp dụng — gộp tags và Favorites. Dữ liệu hiện có được gộp.
File chưa tìm thấy được giữ để Nối lại mục còn thiếu sau khi bổ sung thư viện. Có thể Hoàn tác lần nhập về trạng thái trước nhập; các chỉnh sửa metadata sau lần nhập cũng sẽ được hoàn tác.

Lần xuất đầu và đối chiếu có thể lâu vì phải đọc nội dung file. File đã chuyển định dạng hoặc chỉnh sửa có thể cần xác nhận. Waveform chỉ khôi phục khi nội dung khớp; audio track và kết nối Resolve trên máy mới được giữ riêng.

Quét thư viện, cache và kết nối Resolve
Plugin hiển thị index đã lưu trước, sau đó quét cập nhật trong nền. Lần đầu thêm thư viện cần chờ lập index. Waveform đã có được cache để dùng lại.

Hỗ trợ WAV, MP3, FLAC, AIFF/AIF, M4A/AAC và OGG; khả năng nghe thử còn phụ thuộc bộ giải mã. Tự bỏ các file phụ macOS bắt đầu bằng ._.

Nếu chưa thấy file mới, vào Thư viện và bấm Quét lại. Nếu ổ ngoài chưa kết nối, gắn lại ổ và kiểm tra đường dẫn. Xóa thư viện khỏi danh sách không xóa file trên ổ đĩa.

Kết nối Resolve tự thử khi mở. Nếu chưa kết nối, bảo đảm Resolve đã mở project/timeline, rồi bấm Kết nối lại Resolve. Bản đóng gói dành cho Resolve Studio 20.2 trên Windows, dùng bridge v2.0.0; phiên bản Resolve khác chưa được xác nhận tương thích.

Phím tắt
↑ / ↓: chọn SFX.
Space: nghe/dừng preview.
Enter: chèn vào playhead; Ctrl+Enter: import Media Pool.
I / O: đánh dấu In/Out khi không nhập văn bản.
Ctrl+F: về ô tìm kiếm.
Esc: đóng bảng đang mở hoặc xóa tìm kiếm.
Phím tắt thao tác SFX được tạm ngưng khi đang đọc bảng hướng dẫn này.
