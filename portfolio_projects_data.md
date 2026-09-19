# Danh Sách Dự Án Portfolio - Unity Game Developer

Tài liệu này lưu trữ toàn bộ thông tin chi tiết kỹ thuật của từng dự án để phục vụ việc viết nội dung hiển thị trên trang Portfolio GitHub Pages.

---

## 1. [Đồ án Tốt nghiệp] Bullet Hell: Pixel Survival (Tâm huyết nhất)
- **Thể loại:** 2D Rogue-like Bullet Hell
- **Vai trò:** UI/UX Engineer & Client Developer
- **Các Module trực tiếp xây dựng:**
  - Hệ thống Giao diện toàn diện bằng Unity 6 UI Toolkit (UXML + USS + C#): Main Menu, Loadout & Upgrade, Shop, Daily Quests, Settings, Pause Menu, Game Over / Win-Loss Flow, Tutorial Film Reel, HUD Gameplay.
  - Hệ thống Bản địa hóa Đa ngôn ngữ (Reactive Localization Engine): Nạp dữ liệu từ điển JSON hỗ trợ 5 ngôn ngữ (Việt, Anh, Tây Ban Nha, Nhật, Trung), đổi ngôn ngữ thời gian thực không cần reload Scene.
  - Hệ thống Game Feel & Phản hồi Xúc giác (Tactile UI Juice): Kiến trúc 3-Layer Pixel Art, Squash & Stretch, Floating Text, Numeric Lerp, Film Reel Carousel.
  - Cầu nối Xác thực Ngầm (Async Auth Bridge): Firebase Auth ngầm trong màn hình Loading.
- **Điểm Kỹ thuật Nổi bật:**
  1. Kiến trúc UI Toolkit & 3-Layer Pixel Art (Tối ưu 3–5 Draw Calls/màn hình nhờ Auto-Batching và Sprite Atlas, GPU Matrix Transform 60 FPS).
  2. Event-Driven / EventBus Pattern (Loose Coupling, không [SerializeField]/FindObject, triệt tiêu NullReferenceException).
  3. Chống vỡ Layout CJK & Font Fallback Chain (Flexbox, Dynamic SDF Font Atlas xử lý triệt để lỗi ô vuông □ trên mobile).
  4. Gatekeeper Pattern & Anti-Leak Fallback (Kiểm duyệt dữ liệu chuỗi thô, fallback từ điển tiếng Anh khi mạng lỗi).
- **Links:**
  - Gameplay Video: https://youtu.be/IdTHQMXIXbs?si=sJUEOIXIms4EfcpY
  - Source Code (GitLab): https://gitlab.com/thanhcu06-group/duantotnghiep
  - Download Game (Google Drive): https://drive.google.com/file/d/1BPu1iA8iUxGNkAoJjSVWzMBlLd4GjR5-/view?usp=drive_link

---

## 2. [Internship / Doanh nghiệp] Ywondergreenfarm — 3D Farm Simulation
- **Thể loại:** 3D Farm Simulation (URP)
- **Vai trò:** Unity Game Developer (Core Gameplay, Simulation & UI Architecture)
- **Các Module trực tiếp xây dựng:**
  - Hệ thống Nông trại & Chăn nuôi (vòng đời cây trồng, thú nuôi, cơ chế sinh lão bệnh tử 8h/20h, 24h/48h).
  - Hệ thống Xây dựng & Quy hoạch Lưới 3D (BuildGridManager, GhostPlacementController, TilePlacementSystem, URP Ghost Preview Shader bán trong suốt).
  - Hệ thống Lưu trữ & Đồng bộ Dữ liệu Thời gian thực (Offline Progression / Catch-up theo Unix Timestamp).
  - Giao diện & Tối ưu Trải nghiệm Mobile bằng UI Toolkit (UXML/USS, Virtual Joystick, Touch Look 1 ngón, Auto-run, Mobile Safe Area).
  - Hệ thống Dụng cụ & Rigging Nhân vật (Humanoid Animator Rigging gắn cuốc, rìu, cúp, bình tưới, cần câu vào xương bàn tay).
- **Điểm Kỹ thuật Nổi bật:**
  1. ScriptableObject-Driven Architecture & Custom Unity Editor Tooling (CropDataGenerator, ItemDataGenerator tự động sinh hàng trăm assets 1-click).
  2. Real-time Wall-Clock Simulation & Data Persistence (Offline Catch-up theo Unix Epoch không tốn pin).
  3. 3D Grid-based Placement & Spatial Math (WorldToCell / CellToWorldCenter, Occupancy Matrix, Dynamic Ghost URP Shader).
  4. Performance Optimization & Zero GC Allocation hàng frame trên Mobile.
- **Links:**
  - Gameplay Video: https://youtu.be/yuotDzV7hLg
  - Source Code (GitHub): https://github.com/Lam-Phong-Tech/y-wonder-land
  - Download Game (Google Drive): https://drive.google.com/drive/folders/1THiF6xgpZSp_bmnNBV0KKXZvgJmNnBen?usp=drive_link

---

## 3. [Cuộc thi / Nhóm] Thành Lũy Việt
- **Thể loại:** Tower Defense
- (Đang chờ nạp chi tiết & link)

---

## 4. [Cá nhân] Merge Fruit 3D
- **Thể loại:** 3D Physics Puzzle / Merge Game
- (Đang chờ nạp chi tiết & link)

---

## 5. [Cá nhân] Blue Square 2D
- **Thể loại:** 2D Endless Runner / Rhythm
- (Đang chờ nạp chi tiết & link)

---

## 6. [Cá nhân] Flappy Bat
- **Thể loại:** 2D Arcade
- (Đang chờ nạp chi tiết & link)
