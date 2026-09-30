# HNH SFX Finder

> ## 📢 Dự án đã chuyển sang MRM
> HNH SFX Finder giờ là một phần của **MRM — Media Resource Manager** (plugin DaVinci + ứng dụng quản lý tài nguyên dựng).
> Bản mới, hướng dẫn và báo lỗi: **https://github.com/dmina97-cpu/mrm-media-resource-manager**
>
> Repo này **không còn cập nhật**. Bản cuối: [v0.12.2](../../releases/latest) — kèm hướng dẫn chuyển sang plugin mới và xóa plugin cũ.
>
> *Nội dung bên dưới là tài liệu của bản cũ (0.10.x), giữ lại để tham khảo.*

---

**Local SFX Browser & Workflow Tool for DaVinci Resolve**
<img width="1020" height="806" alt="image" src="https://github.com/user-attachments/assets/2046c6b2-2347-4115-84b9-993d007d3161" />

HNH SFX Finder giúp tìm kiếm, nghe thử và đưa Sound Effect vào DaVinci Resolve nhanh hơn, đặc biệt hữu ích khi làm việc với thư viện SFX lớn.

Thay vì phải mở từng thư mục để tìm và nghe file:

**Search → Preview → Insert / Drag to Timeline**

Toàn bộ thư viện được xử lý **local trên máy**, không cần tải SFX lên cloud.

---

## Phiên bản hỗ trợ

| Hệ điều hành | DaVinci Resolve | Phiên bản HNH | Cách hoạt động |
|---|---|---|---|
| Windows | Studio | HNH SFX Finder Studio | Workflow Integration |
| Windows | Free | HNH SFX Finder Free | Companion App |
| macOS Apple Silicon | Studio | HNH SFX Finder Studio | Workflow Integration |

> Bản Free sử dụng ứng dụng companion độc lập và Native Drag & Drop thay cho Workflow Integration.

---

# Tính năng nổi bật

### Tìm kiếm & quản lý thư viện

- Tìm kiếm nhanh trong toàn bộ thư viện SFX local.
- Quét nhiều folder và subfolder.
- Smart Search hỗ trợ từ khóa Việt / Anh.
- Quản lý nhiều thư viện cùng lúc.
- Theo dõi thay đổi khi thêm hoặc xóa file.
- Favorites và Recent.
- Tag và metadata.
- Bộ lọc theo loại media, thời lượng và thuộc tính.
- Backup / Restore dữ liệu thư viện.

### Preview

- Nghe SFX trực tiếp trước khi sử dụng.
- Hiển thị waveform.
- Waveform Cache giúp tải lại nhanh hơn.
- Không cần import vào Resolve chỉ để nghe thử.

### Media

HNH SFX Finder không chỉ được thiết kế cho SFX mà còn có khả năng quản lý:

- Audio
- Image
- Video

---

# DaVinci Resolve Studio

Bản Studio sử dụng **Workflow Integration** để giao tiếp trực tiếp với DaVinci Resolve.

### Tính năng bổ sung

- Insert at Playhead.
- Chọn Audio Track A1 / A2 / A3...
- Tìm track trống trước khi insert.
- Hạn chế chèn đè lên audio đang có.
- Hỗ trợ chọn hoặc tạo track phù hợp.
- Các công cụ Timeline Range và audio workflow.
- Import media trực tiếp vào Resolve.

### Workflow

```text
Search
   ↓
Preview
   ↓
Select Track
   ↓
Insert at Playhead

DaVinci Resolve Free
DaVinci Resolve Free không sử dụng phiên bản Workflow Integration của HNH.
Thay vào đó, HNH SFX Finder Free chạy như một ứng dụng companion độc lập bên cạnh Resolve.
Workflow
HNH SFX Finder Free
        ↓
      Search
        ↓
      Preview
        ↓
  Native Drag & Drop
        ↓
Media Pool / Timeline

Bạn có thể tìm và nghe SFX trong HNH, sau đó kéo file trực tiếp vào:
- Media Pool
- Audio Track trên Timeline
Portable EXE
Bản Windows Free được đóng gói thành một file:
HNH_SFX_Finder_Free_v0.9.0_x64.exe

Không cần cài:
- Node.js
- npm
- WorkflowIntegration.node
- Workflow Integration Plugin
Chỉ cần mở EXE và sử dụng.
Cài đặt
Windows + DaVinci Resolve Studio
1. Giải nén HNH SFX Finder
Không chạy plugin trực tiếp trong file ZIP.
2. Chạy installer
install_windows.bat

3. Khởi động lại DaVinci Resolve
Mở:
Workspace
→ Workflow Integrations
→ HNH SFX Finder

4. Thêm thư viện
Ví dụ:
D:\SFX Library

Chỉ cần chọn thư mục gốc.
HNH sẽ tự quét các thư mục con:
SFX Library
├── Whoosh
├── Impact
├── Transition
├── UI
├── Cinematic
├── Ambience
└── Funny

Sau khi index hoàn tất, bạn có thể Search và Preview ngay.
Windows + DaVinci Resolve Free
Không cần cài plugin vào DaVinci Resolve.
Chạy:
HNH_SFX_Finder_Free_v0.9.0_x64.exe

Sau đó:
1. Add SFX Library
2. Search
3. Preview
4. Kéo SFX sang Resolve

Có thể kéo trực tiếp vào:
Media Pool

hoặc:
Timeline → A1 / A2 / A3...

Gợi ý sử dụng
Nếu có hai màn hình:
Monitor 1 → DaVinci Resolve
Monitor 2 → HNH SFX Finder

HNH có thể hoạt động như một SFX Browser riêng trong quá trình dựng.
macOS Apple Silicon + DaVinci Resolve Studio
Hỗ trợ máy Mac sử dụng Apple Silicon.
Ví dụ:
M1
M2
M3
M4

1. Thoát hoàn toàn DaVinci Resolve
2. Giải nén HNH SFX Finder
3. Chạy
install_macos.command

Nếu macOS chặn lần mở đầu tiên:
Right Click
→ Open

Nhập mật khẩu Administrator nếu installer yêu cầu.
4. Mở DaVinci Resolve Studio
Vào:
Workspace
→ Workflow Integrations
→ HNH SFX Finder

Library path trên macOS
Ví dụ thư viện nằm trong máy:
/Users/username/SFX Library/

Hoặc SSD ngoài:
/Volumes/SFX SSD/SFX Library/

Nếu chuyển database từ Windows sang macOS, có thể sử dụng Backup / Restore rồi thiết lập lại Library Root theo đường dẫn mới.
Studio vs Free
Tính năng	Studio	Free
Search SFX	✓	✓
Smart Search Việt / Anh	✓	✓
Preview	✓	✓
Waveform	✓	✓
Favorites / Recent	✓	✓
Tags / Metadata	✓	✓
Library Management	✓	✓
Backup / Restore	✓	✓
Drag & Drop	✓	✓
Insert at Playhead	✓	—
Chọn Audio Track tự động	✓	—
Tìm track trống	✓	—
Điều khiển Timeline qua Integration	✓	—
Workflow Integration	✓	—
Companion App	—	✓


Dữ liệu & quyền riêng tư
HNH SFX Finder được thiết kế theo hướng Local First.
Thư viện SFX, index, waveform và dữ liệu quản lý được xử lý trên máy.
Bạn không cần upload thư viện SFX cá nhân lên cloud để sử dụng các chức năng tìm kiếm cơ bản của HNH SFX Finder.
Roadmap
Mục tiêu tiếp theo của HNH SFX Finder là phát triển từ một SFX Browser thành một SFX Assistant.
Hướng phát triển:
Timeline
   ↓
Detect Cut / Transition / Event
   ↓
Classify
   ↓
Suggest SFX
   ↓
Preview
   ↓
Insert

Một số hướng đang nghiên cứu:
- Timeline-aware SFX suggestions.
- Gợi ý Whoosh theo cut / transition.
- Gợi ý Impact cho hard cut.
- Gợi ý Riser / Downer cho transition.
- Gợi ý Pop / Click cho text và UI.
- Intensity: Soft / Medium / Hard.
- Style: Clean / Cinematic / Funny.
- Smart semantic ranking.
- Local-first processing.
Các tính năng trong Roadmap chưa được coi là tính năng chính thức cho tới khi xuất hiện trong bản release.
Báo lỗi & góp ý
Nếu gặp lỗi, vui lòng cung cấp:
HNH SFX Finder version:
DaVinci Resolve version:
Free / Studio:
Windows / macOS:
Mô tả lỗi:
Ảnh hoặc video lỗi:

Thông tin này giúp việc kiểm tra và sửa lỗi nhanh hơn.
