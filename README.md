---


---

<h2 id="phần-1-phân-tích-bài-toán-io">PHẦN 1: PHÂN TÍCH BÀI TOÁN (I/O)</h2>
<h3 id="đầu-vào-và-đầu-ra">1. Đầu vào và đầu ra</h3>
<p><strong>Đầu vào:</strong></p>
<ul>
<li>
<p>Ban Kỹ thuật: 3 người, làm code và kiểm thử API.</p>
</li>
<li>
<p>Ban Thiết kế: 2 người, thiết kế giao diện.</p>
</li>
<li>
<p>Ban Kinh doanh: 2 người, viết Business Plan.</p>
</li>
<li>
<p>Nhà đầu tư: 1 người, xem Business Plan và Slide Pitch.</p>
</li>
</ul>
<p><strong>Đầu ra:</strong></p>
<ul>
<li>
<p>Cấu trúc thư mục Google Drive.</p>
</li>
<li>
<p>Phân quyền cho từng nhóm.</p>
</li>
<li>
<p>Bảo vệ tài liệu quan trọng và kiểm soát quyền truy cập.</p>
</li>
</ul>
<h3 id="cấu-trúc-thư-mục">2. Cấu trúc thư mục</h3>
<pre><code>CampusPay/
├── 01_Technical/
├── 02_Design/
├── 03_Business/
├── 04_Shared_Documents/
└── 05_Sensitive_Data/
</code></pre>
<ul>
<li>
<p><strong>01_Technical:</strong> Chứa mã nguồn và tài liệu API.</p>
</li>
<li>
<p><strong>02_Design:</strong> Chứa thiết kế giao diện và hình ảnh.</p>
</li>
<li>
<p><strong>03_Business:</strong> Chứa Business Plan và tài liệu kinh doanh.</p>
</li>
<li>
<p><strong>04_Shared_Documents:</strong> Chứa Slide Pitch và Business Summary.</p>
</li>
<li>
<p><strong>05_Sensitive_Data:</strong> Chứa API keys và dữ liệu khách hàng.</p>
</li>
</ul>
<h3 id="các-bước-thực-hiện">3. Các bước thực hiện</h3>
<ol>
<li>
<p>Tạo thư mục CampusPay và các thư mục con.</p>
</li>
<li>
<p>Đặt tên thư mục rõ ràng.</p>
</li>
<li>
<p>Sắp xếp tài liệu vào đúng thư mục.</p>
</li>
<li>
<p>Cấp quyền phù hợp cho từng nhóm.</p>
</li>
<li>
<p>Đặt tài liệu nhạy cảm ở chế độ Restricted.</p>
</li>
<li>
<p>Kiểm tra quyền truy cập và lịch sử phiên bản.</p>
</li>
<li>
<p>Đặt thời hạn 14 ngày cho nhà đầu tư.</p>
</li>
<li>
<p>Thu hồi quyền khi thành viên nghỉ việc.</p>
</li>
</ol>
<h2 id="phần-2-triển-khai-và-chống-lỗi">PHẦN 2: TRIỂN KHAI VÀ CHỐNG LỖI</h2>
<h3 id="phân-quyền-cho-từng-nhóm">4. Phân quyền cho từng nhóm</h3>
<p><strong>1. Mã nguồn và tài liệu API</strong></p>
<ul>
<li>
<p>Ban Kỹ thuật: Editor.</p>
</li>
<li>
<p>Ban Thiết kế: Không có quyền.</p>
</li>
<li>
<p>Ban Kinh doanh: Không có quyền.</p>
</li>
<li>
<p>Nhà đầu tư: Không có quyền.</p>
</li>
<li>
<p>Bảo mật: Chỉ người có nhiệm vụ mới được truy cập.</p>
</li>
</ul>
<p><strong>2. Thiết kế UI và hình ảnh</strong></p>
<ul>
<li>
<p>Ban Kỹ thuật: Viewer.</p>
</li>
<li>
<p>Ban Thiết kế: Editor.</p>
</li>
<li>
<p>Ban Kinh doanh: Viewer.</p>
</li>
<li>
<p>Nhà đầu tư: Không có quyền.</p>
</li>
<li>
<p>Bảo mật: Không chia sẻ công khai.</p>
</li>
</ul>
<p><strong>3. Business Plan</strong></p>
<ul>
<li>
<p>Ban Kỹ thuật: Viewer.</p>
</li>
<li>
<p>Ban Thiết kế: Không có quyền.</p>
</li>
<li>
<p>Ban Kinh doanh: Editor.</p>
</li>
<li>
<p>Nhà đầu tư: Viewer.</p>
</li>
<li>
<p>Bảo mật: Ban Kỹ thuật chỉ được xem, không được sửa.</p>
</li>
</ul>
<p><strong>4. Slide Pitch và Business Summary</strong></p>
<ul>
<li>
<p>Ban Kỹ thuật: Viewer.</p>
</li>
<li>
<p>Ban Thiết kế: Viewer.</p>
</li>
<li>
<p>Ban Kinh doanh: Editor.</p>
</li>
<li>
<p>Nhà đầu tư: Viewer.</p>
</li>
<li>
<p>Bảo mật: Nhà đầu tư chỉ được xem tài liệu đã duyệt.</p>
</li>
</ul>
<p><strong>5. API keys và dữ liệu khách hàng</strong></p>
<ul>
<li>
<p>Ban Kỹ thuật: Editor theo nhiệm vụ.</p>
</li>
<li>
<p>Ban Thiết kế: Không có quyền.</p>
</li>
<li>
<p>Ban Kinh doanh: Không có quyền.</p>
</li>
<li>
<p>Nhà đầu tư: Không có quyền.</p>
</li>
<li>
<p>Bảo mật: Đặt Restricted, không dùng Anyone with the link.</p>
</li>
</ul>
<h3 id="trả-lời-3-bẫy-dữ-liệu">5. Trả lời 3 bẫy dữ liệu</h3>
<p><strong>Bẫy 1: Chia sẻ Business Plan cho Ban Kỹ thuật</strong></p>
<p>Cấp quyền Viewer để Ban Kỹ thuật đọc và hiểu dự án nhưng không thể chỉnh sửa nội dung. Không cấp quyền Editor vì họ không phụ trách viết Business Plan.</p>
<p><strong>Bẫy 2: Nhà đầu tư muốn tải Slide Pitch</strong></p>
<p>Cấp quyền Viewer đối với bản PDF và cho phép tải xuống để thuyết trình offline. Không cấp quyền chỉnh sửa bản gốc.</p>
<p>Không cần tắt tính năng Viewers can download đối với bản PDF này vì nhà đầu tư cần tải file về máy.</p>
<p><strong>Bẫy 3: Thành viên nghỉ việc</strong></p>
<ul>
<li>
<p>Xóa quyền truy cập của thành viên khỏi các tệp và thư mục.</p>
</li>
<li>
<p>Xóa thành viên khỏi các nhóm được chia sẻ.</p>
</li>
<li>
<p>Nếu dùng tài khoản công ty, yêu cầu quản trị viên khóa tài khoản khi phù hợp.</p>
</li>
<li>
<p>Kiểm tra lại quyền để bảo đảm thành viên không còn truy cập tài liệu.</p>
</li>
</ul>
<h3 id="nguyên-tắc-bảo-mật">6. Nguyên tắc bảo mật</h3>
<ul>
<li>
<p>Chỉ cấp quyền cần thiết cho từng người.</p>
</li>
<li>
<p>Tài liệu nhạy cảm phải để Restricted.</p>
</li>
<li>
<p>Tài liệu quan trọng cần có lịch sử phiên bản tối thiểu 30 ngày.</p>
</li>
<li>
<p>Quyền nhà đầu tư phải hết hạn sau 14 ngày.</p>
</li>
<li>
<p>Kiểm tra quyền truy cập thường xuyên.</p>
</li>
</ul>
<p>Lưu ý: Cần kiểm tra tính năng hết hạn quyền và lịch sử phiên bản theo loại tài khoản Google Drive đang sử dụng.</p>

