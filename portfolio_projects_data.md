# Danh Sách Dự Án Portfolio - Unity Game Developer

Tài liệu này lưu trữ toàn bộ thông tin chi tiết kỹ thuật của từng dự án để phục vụ việc viết nội dung hiển thị trên trang Portfolio GitHub Pages.

---

## 1. [Đồ án Tốt nghiệp] Bullet Hell
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

## 2. [Internship / Doanh nghiệp] Y Wonder Green Farm
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
  - Gameplay Video: https://youtu.be/jS0IoS0HUss
  - Source Code (GitHub): https://github.com/Lam-Phong-Tech/y-wonder-land
  - Download Game (Google Drive): https://drive.google.com/drive/folders/1THiF6xgpZSp_bmnNBV0KKXZvgJmNnBen?usp=drive_link

---

## 3. [Cuộc thi / Nhóm] Thành Lũy Việt
- **Thể loại:** 2D Tower Defense (Đề tài Lịch sử)
- **Vai trò:** Gameplay & Core Mechanics Programmer (Unity / C#)
- **Các Module trực tiếp xây dựng:**
  - Hệ thống Xây dựng & Tương tác Tháp (BuildableArea, TowerActionMenu, TowerBuildMenu, nâng cấp Lv1→3, bán tháp hoàn ô đất).
  - Hệ thống Chiến đấu & Bắn đạn (TowerShooter quét tầm bắn, Fire Rate, Projectile va chạm trừ máu).
  - Hệ thống Kẻ địch & Đợt tấn công (Enemy di chuyển theo Waypoints, Mathf.Atan2 xoay hướng, EnemySpawner).
  - Hệ thống Bẫy Chiến thuật (TrapMine mìn nổ AOE, TrapSpike chông làm chậm/sát thương).
  - Hệ thống Tư liệu Lịch sử (HistoryData, HistoryPanel lưu và hiển thị 10 chiến dịch lịch sử).
- **Điểm Kỹ thuật Nổi bật:**
  1. Data-Driven Architecture với ScriptableObject (TowerData, EnemyData, WaveConfigSO, TrapData cân bằng Editor).
  2. World Space to Screen Space & Dynamic UI Canvas Matching (Mathf.Clamp chống tràn viền trên mọi tỷ lệ phân giải).
  3. Xử lý Vật lý 2D & Sát thương AOE (Physics2D.OverlapCircleAll & OnTriggerEnter2D nổ diện rộng).
  4. Design Pattern (Singleton DontDestroyOnLoad cho HistoryData xuyên suốt 10 màn chơi, Component-Based logic).
- **Links:**
  - Gameplay Video: https://youtu.be/u7bke6Jkrcc
  - Source Code (GitHub): https://github.com/Nhieenn/ThanhLuyViet

---

## 4. [Cá nhân] Merge Fruit 3D
- **Thể loại:** 3D Physics Puzzle / Merge Game
- **Vai trò:** Unity Gameplay & Physics Developer
- **Các Module trực tiếp xây dựng:**
  - Phát triển Core Gameplay & Cơ chế Hợp nhất (Merge Evolution Logic, tính điểm lũy tiến, particle FX).
  - Điều khiển & Tương tác Vật lý (Physics.Raycast + LineRenderer vẽ đường ngắm dự đoán quỹ đạo rơi tự do, chuyển đổi isKinematic sang Rigidbody khi thả).
  - Hệ thống Cảnh báo & Điều kiện Thua (Hazard Sensor Trigger qua OnTriggerEnter/Exit với danh sách fruitsInZone, hiệu ứng chớp sáng Mathf.PingPong, Camera Shake).
  - Giao diện UI Toolkit (UXML/USS) và hệ thống Audio/Game Manager.
- **Điểm Kỹ thuật Nổi bật:**
  1. Vật lý 3D & Xử lý Quỹ đạo (Physics.Raycast + LineRenderer real-time aim line).
  2. Tối ưu hóa Vùng Cảm biến & Cảnh báo (Optimized Hazard Trigger, không quét FindObjects hàng frame, triệt tiêu GC Alloc).
  3. Giao diện thế hệ mới với Unity UI Toolkit (UXML/USS, dynamic class AddToClassList animation).
  4. Kiến trúc Singleton & Đồng bộ Luồng an toàn với Coroutines.
- **Links:**
  - Gameplay Video: https://youtu.be/oJn-49k7GLs
  - Source Code (GitHub): https://github.com/Nhieenn/Merge-Fruit-1
  - Download Game (Google Drive): https://drive.google.com/drive/u/0/folders/1wrBNeSvJaIHHgHVNZ3la5E97zfRFOjYf

---

## 5. [Cá nhân] Blue Square 2D
- **Thể loại:** 2D Endless Runner / Platformer
- **Vai trò:** Unity Gameplay & Systems Developer
- **Các Module trực tiếp xây dựng:**
  - Core Mechanics & Game Feel: Coyote Time & Jump Buffering (không input drop), New Input System (Keyboard, Touch, Mouse).
  - ThemeManager đổi màu thế giới thời gian thực (Ngày → Chiều → Đêm) theo điểm số (Score-driven Color Lerp).
  - Game Loop & State Management: Dynamic gameSpeed difficulty, High Score PlayerPrefs, UI Toolkit menu.
  - Juiciness: Cinemachine Impulse Camera Shake, Particle System (bụi, crash, trail), AudioManager.
- **Điểm Kỹ thuật Nổi bật:**
  1. Generic Object Pooling (`UnityEngine.Pool.ObjectPool<GameObject>` Dictionary, triệt tiêu Instantiate/Destroy GC spikes).
  2. Platformer Game Feel Optimization (`coyoteTime` & `jumpBufferTime`).
  3. Dynamic Color Cycle & Mathematical Interpolation (`Color.Lerp` đồng bộ Camera, Sprites, Particles).
  4. Seamless Infinite Scrolling (`Mathf.Repeat` GroundScroller) & UI Toolkit UIDocument.
- **Links:**
  - Gameplay Video: https://youtu.be/9lwIQXOVJlQ
  - Source Code (GitHub): https://github.com/Nhieenn/Blue-Square
  - Download Game (Google Drive): https://drive.google.com/drive/u/0/folders/1wrBNeSvJaIHHgHVNZ3la5E97zfRFOjYf

---

## 6. [Cá nhân] Flappy Bat
- **Thể loại:** 2D Arcade
- **Vai trò:** Solo Developer (First Game Development Milestone)
- **Các Module trực tiếp xây dựng:**
  - Vòng đời Game Loop chuẩn (Menu, Playing, Game Over, Restart).
  - Thuật toán sinh ngẫu nhiên chướng ngại vật theo chiều cao và cơ chế sinh trái tim hồi máu.
  - Hệ thống trừ máu va chạm, hồi phục và bộ đếm thời gian sinh tồn (Survival Timer).
  - Sprite Animation chuyển động dơi, giao diện HUD/Menu bằng Unity uGUI Canvas và lưu điểm High Score (PlayerPrefs).
  - Đóng gói và xuất bản thành công trên Windows PC và Android.
- **Điểm Kỹ thuật Nổi bật:**
  1. Procedural Obstacle & Item Spawning (Sinh chướng ngại vật & trái tim hồi máu).
  2. Health & Survival Timer System.
  3. Persistence (PlayerPrefs HighScore) & State Management.
  4. 2D Sprite Animation & uGUI Multi-platform Build.
- **Links:**
  - Gameplay Video: https://youtu.be/alanA02fs-0
  - Download Game (Google Drive): https://drive.google.com/drive/u/0/folders/17yzgNNZ0yk9-4AWSFAlgq63_19fA2_vh
