---
stepsCompleted: ['step-01-init', 'step-02-discovery', 'step-03-core-experience', 'step-04-emotional-response', 'step-05-inspiration', 'step-06-design-system', 'step-07-defining-experience']
inputDocuments:
  - planning-artifacts/prd.md
  - planning-artifacts/product-brief-Solo-Exit-2026-03-05.md
  - brainstorming/brainstorming-session-2026-03-05-175851.md
---

# UX Design Specification — Solo Exit

**Author:** NgocBich
**Date:** 2026-03-06

---

## Executive Summary

### Tầm nhìn sản phẩm (UX)

Solo Exit là mobile app đồng hành người dùng VN từ nhân viên → solopreneur. App cần tạo ra cảm giác **an toàn + hành động** — bớt stress, không thêm stress.

**Khoảnh khắc UX quan trọng nhất:** Mở app lần đầu → nhập 3 con số → thấy đếm ngược → "OMG, ra số rồi!" (dưới 60 giây)

### Đối tượng người dùng

| Persona | Tuổi | Đặc điểm UX | Thiết bị |
|---------|------|-------------|---------|
| **Minh** (MVP) | 25-30 | Tech-savvy, dùng app đêm | iPhone/Android |
| **Hùng** (Đợt 2) | 30-40 | Ít thời gian, UX nhẹ nhàng | Android |
| **Linh** (Đợt 3) | 28-35 | Power user, cần dashboard | Mobile + Web |
| **Phúc** (Đợt 4) | 20-24 | Gen Z, visual-first | iPhone |

### Bản đồ cảm xúc (Emotional Design Map)

| Màn hình | Cảm xúc mục tiêu | Thiết kế hướng đến |
|----------|-------------------|-------------------|
| Onboarding | Tò mò + An toàn | Slider nhẹ nhàng, ngôn ngữ "ước tính" |
| Đếm ngược chính | Tự tin + Kích thích | Số lớn, animation đẹp, tiến trình rõ |
| Thu nhập tăng | Phấn khích + Tự hào | Animation celebration, số giảm |
| Khi setback | Bình tĩnh + Hy vọng | Tone ấm, không đổ lỗi, gợi ý Plan B |
| AI Chat | Ấm áp + Được lắng nghe | Typing indicator, streaming text, tone bạn bè |
| Quay lại app | Được chào đón | Welcome back, không trách móc |
| Paywall | Muốn thêm + Hợp lý | Chỉ hiện sau khi đã thấy giá trị |

### Thách thức UX chính

| # | Thách thức | Giải pháp UX |
|---|-----------|-------------|
| 1 | **Onboarding < 60 giây** — nhập số tiền nhạy cảm | Thanh kéo (slider) thay gõ số + placeholder gợi ý + nút "Tôi không biết" |
| 2 | **AI Companion tự nhiên** — không cảm giác bot | Typing indicator (3 chấm) + streaming text (hiện dần) + tone ấm áp |
| 3 | **Đếm ngược TĂNG ngược** khi setback | UX bình tĩnh, không đổ lỗi, gợi ý điều chỉnh kế hoạch |
| 4 | **Paywall đúng lúc** — chặn trả tiền nhưng không gây khó chịu | Hiện sau 1-2 tuần dùng free, khi user ĐÃ THẤY giá trị |
| 5 | **Welcome back** — user bỏ app quay lại | Không trách móc, chào đón, countdown tự điều chỉnh |
| 6 | **Độ trễ API** — AI mất 2-5 giây | Typing indicator + streaming response + skeleton loading |

### Cơ hội thiết kế

| # | Cơ hội | Ý tưởng UX |
|---|--------|-----------|
| 1 | **Widget đếm ngược** | Widget home screen — nhìn mỗi ngày, visual ấn tượng |
| 2 | **Micro-animations** | Đếm ngược GIẢM → animation celebration = dopamine hit |
| 3 | **AI personality** | AI có "tính cách" — ấm áp, hài hước nhẹ, hiểu VN |
| 4 | **Auto dark mode** | Tự động theo giờ hệ thống (Minh dùng đêm, Hùng dùng ngày) |
| 5 | **Tháp kỹ năng visual** | Tower xây dần → cảm giác "xây lâu đài" |
| 6 | **Social Proof đẹp** | "847 người giống bạn" → visual component, không chỉ text |
| 7 | **Share Card** | Tạo ảnh story đếm ngược → share Zalo/Instagram = marketing miễn phí |

### Nguyên tắc thiết kế (Design Principles)

| # | Nguyên tắc | Ý nghĩa |
|---|-----------|---------|
| 1 | **An toàn trước kích thích** | User phải cảm thấy an toàn trước khi kích thích hành động |
| 2 | **60 giây hoặc ít hơn** | Mọi giá trị cốt lõi phải đến trong 1 phút |
| 3 | **Không bao giờ đổ lỗi** | Khi user thất bại hoặc bỏ cuộc → đón nhận, không phán xét |
| 4 | **Quen thuộc + bất ngờ** | Navigation quen (như Momo/Zalo), nội dung bất ngờ (đếm ngược, AI) |

### Ràng buộc thiết kế

| # | Ràng buộc | Chi tiết |
|---|----------|---------|
| 1 | **One-hand use** | Nút chính ở nửa dưới màn hình, 80% user VN cầm phone 1 tay |
| 2 | **Navigation quen thuộc** | Bottom tab bar (Momo), chat bubble (Zalo), animation mượt (TikTok) |
| 3 | **Font tối thiểu 16px** | Dễ đọc cho nhiều nhóm tuổi |

## Core User Experience

### Hành động cốt lõi

**Hành động #1 (làm nhiều nhất):** Mở app → nhìn đếm ngược → cảm thấy tiến bộ

**Hành động quyết định:** Onboarding 3 câu hỏi → thấy kết quả lần đầu

**Vòng lặp chính (Core Loop):**
```
Nhập thu nhập phụ → Đếm ngược GIẢM → Cảm giác tiến bộ → Quay lại xem tiếp
```

### Chiến lược nền tảng

| Quyết định | Chi tiết |
|-----------|--------|
| Nền tảng | Mobile-first (iOS + Android), Cross-platform |
| Tương tác | Touch-based, one-hand use, nửa dưới màn hình |
| Offline | Xem đếm ngược + tháp kỹ năng, nhập thu chi |
| Thiết bị | Widget home screen, biometric, push notification |
| Navigation | Bottom tab bar (quen thuộc Momo/Zalo) |

### Đăng ký: Value-first, Register-later

Màn hình đầu tiên KHÔNG phải đăng ký:
1. Mở app → "Bạn muốn biết còn bao lâu để tự do?" → vào luôn slider
2. 3 câu hỏi → thấy đếm ngược
3. "Muốn LƯU kết quả? Đăng ký ngay!" → đăng ký SAU khi đã thấy giá trị

### Tương tác không cần nghĩ

| Tương tác | Cảm giác mong muốn |
|----------|--------------------|
| Mở app → thấy đếm ngược | Tự động, < 2 giây, không cần login lại |
| Nhập thu nhập mới | 1 nút → gõ số → đếm ngược cập nhật ngay |
| Hỏi AI | Như nhắn tin cho bạn, không cần "lệnh" |
| Xem tháp kỹ năng | Vuốt lên/xuống, đánh dấu 1 chạm |
| Share tiến trình | 1 nút → Share Card → chọn Zalo/Instagram |
| Chuyển tab | Giữ state, không reload, nhớ vị trí cuộn |

### Gesture Map

| Gesture | Hành động |
|---------|----------|
| Vuốt xuống | Refresh đếm ngược |
| Vuốt trái/phải | Chuyển tab |
| Long press đếm ngược | Mở chi tiết tính toán |
| Double tap kỹ năng | Đánh dấu hoàn thành |

### Khoảnh khắc quyết định (Make-or-Break)

| # | Khoảnh khắc | Thành công | Thất bại |
|---|------------|-----------|----------|
| 0 | **Lần đầu mở app** | Slider ngay, không đăng ký → hook | Form đăng ký dài → xóa |
| 1 | **Đếm ngược lần đầu** | "OMG, ra số rồi!" → tiếp | "Nhàm" → xóa |
| 2 | **AI trả lời lần đầu** | "Nó hiểu mình!" → trust | "Bot vô hồn" → bỏ |
| 3 | **Thu nhập phụ đầu tiên** | "Đếm ngược giảm!" → addicted | Quên nhập → vô nghĩa |
| 4 | **Quay lại sau setback** | "Vẫn ở đây cho mình" → trung thành | "Lâu quá" → xóa |

### Micro-moment Map

| Khoảnh khắc nhỏ | UX phản hồi |
|-----------------|------------|
| Đang chờ AI trả lời | 3 chấm nhảy + tip ngẫu nhiên: "70% thu nhập phụ bắt đầu từ kỹ năng có sẵn" |
| Vừa nhập thu nhập | Confetti animation nhẹ + số đếm ngược chạy xuống |
| Hoàn thành 1 kỹ năng | Tháp thêm 1 tầng + âm thanh "ding!" |
| Đạt milestone countdown | Full-screen celebration + nút Share Card |

### Nguyên tắc trải nghiệm

| # | Nguyên tắc | Áp dụng |
|---|-----------|--------|
| 1 | **Giá trị trong 60 giây** | 3 câu → đếm ngược. Không form dài, không tutorial. |
| 2 | **Đếm ngược là trung tâm** | Mọi tính năng → feed vào đếm ngược |
| 3 | **AI = bạn đồng hành** | Hiểu context, nhớ lịch sử, tone ấm áp |
| 4 | **Tiến bộ nhỏ > kế hoạch lớn** | Mỗi ngày 1 bước nhỏ > master plan phức tạp |

## Desired Emotional Response

### Mục tiêu cảm xúc chính

| Cảm xúc | Khi nào | Tại sao |
|---------|--------|--------|
| **"Tôi có thể làm được"** | Thấy đếm ngược lần đầu | Từ mơ hồ → con số cụ thể = sức mạnh |
| **"Có người hiểu mình"** | AI trả lời về nỗi sợ | Solopreneur = cô đơn, AI bù đắp |
| **"Mình đang tiến bộ"** | Đếm ngược giảm | Nhập → giảm → vui → nhập tiếp |
| **"Mình không một mình"** | Social proof | "847 người giống bạn" |
| **"Dữ liệu an toàn"** | Mỗi lần mở app | Biometric + Share Card không lộ số tiền |

### Hành trình cảm xúc theo thời gian

| Giai đoạn | Tuần | Cảm xúc chính | Thiết kế hỗ trợ |
|-----------|------|---------------|------------------|
| Khám phá | 0 | Tò mò | Slider ngay, không đăng ký |
| Onboarding | 0 | Bất ngờ + An toàn | 3 màn, placeholder, "Tôi không biết" |
| Tuần đầu | 1 | Tự tin | "✅ Bước 1/5 hoàn thành!" |
| Thói quen | 2-4 | Quyết tâm | Nhắc nhẹ, AI động viên |
| Thu nhập đầu | 4-8 | Phấn khích | Confetti animation |
| Setback | bất kỳ | Bình tĩnh | Màu trung tính, không đỏ |
| Bỏ cuộc tạm | bất kỳ | Được đón nhận | Welcome back, không trách |
| Milestone | 3-6 tháng | TỰ HÀO | Full-screen celebration + Share |

### Vi cảm xúc

| Cặp cảm xúc | ✅ Mong muốn | ❌ Tránh | Cách thiết kế |
|-------------|-----------|-------|---------------|
| Tự tin ↔ Bối rối | Tự tin | Bối rối | Slider đơn giản, placeholder |
| Tin tưởng ↔ Nghi ngờ | Tin tưởng | Nghi ngờ | Disclaimer + vẫn hữu ích |
| Phấn khích ↔ Lo lắng | Phấn khích | Lo lắng | Ngôn ngữ "ước tính" |
| Thành tựu ↔ Thất vọng | Thành tựu | Thất vọng | Celebration + tiến bộ nhỏ |
| Thuộc về ↔ Cô đơn | Thuộc về | Cô đơn | Social proof + AI bạn bè |
| Riêng tư ↔ Bị lộ | An tâm | Sợ lộ lương | Biometric + Share Card chỉ show % |

### Cảm xúc → Quyết định thiết kế

| Cảm xúc | Quyết định UX |
|---------|---------------|
| "Tôi có thể" | Số đếm ngược TO, RÕ, chính giữa màn hình |
| "Nhanh quá!" | 3 màn, mỗi màn 1 câu, < 60s |
| "Không phán xét" | AI không dùng "nhưng"/"tuy nhiên" khi setback |
| "Mình đang thắng" | % thay đổi + animation khi cải thiện |
| "Ấm áp" | AI dùng emoji nhẹ, xưng "mình-bạn", nhớ tên |
| "Đã bắt đầu rồi" | Progress bar "Bước 1/5 hoàn thành" sau onboarding |
| "Không sao cả" | Đếm ngược tăng → màu trung tính, không đỏ/cảnh báo |

## UX Pattern Analysis & Inspiration

### Sản phẩm truyền cảm hứng

| App | Điều làm tốt | Solo Exit học gì |
|-----|-------------|-------------------|
| **Momo** | Bottom tab bar, biometric, quick actions | Navigation + biometric login |
| **Zalo** | Chat bubble, notification badge, phản hồi nhanh | AI chat UI + notification |
| **TikTok** | Animation mượt, full-screen, cuốn hút | Micro-animations |
| **Duolingo** | Streak, progress visual, gamification nhẹ | Tháp kỹ năng + streak |
| **Calm** | Tone nhẹ, dark UI, âm thanh relax | AI tone + welcome back |
| **Notion** | Toggle sections, breadcrumb, templates | Toggle chi tiết countdown |

### UX Patterns chuyển đổi

**Navigation:**
| Pattern | Áp dụng |
|---------|--------|
| Bottom tab bar (5 tab) | Home / AI / Kỹ năng / Thu nhập / Tôi |
| Floating action button | Nút "+" nhập thu nhập |
| Pull-to-refresh | Vuốt xuống refresh đếm ngược |

**Tương tác:**
| Pattern | Áp dụng |
|---------|--------|
| Chat bubble (Zalo) | AI Companion |
| Slider input | Onboarding lương/chi tiêu |
| Swipe actions | Vuốt kỹ năng → hoàn thành |
| Toggle sections (Notion) | Chi tiết tính toán countdown |
| **Optimistic UI** | Đếm ngược giảm NGAY khi nhập, server xác nhận sau |

**Visual:**
| Pattern | Áp dụng |
|---------|--------|
| Hero number (số lớn giữa) | Đếm ngược "9 THÁNG 12 NGÀY" |
| Progress ring/bar | "Bước 2/5" |
| Confetti celebration | Thu nhập phụ giảm countdown |
| Card-based layout | Share Card, kỹ năng cards |

### Anti-Patterns cần tránh

| ❌ Tránh | ✅ Thay bằng |
|---------|------------|
| Onboarding tutorial dài | Vào luôn slider, học qua dùng |
| Quá nhiều notification | Max 3-4/tuần, tone nhẹ |
| Màu đỏ cho số tiền | Màu trung tính |
| Form đăng ký phức tạp | Value-first, register-later |
| Gamification nặng | Celebration nhẹ, không leaderboard |
| Dashboard quá nhiều số | 1 số chính + detail khi cần |
| Yêu cầu review sớm | Hỏi review SAU milestone đầu tiên |

### Benchmark thành công

| Pattern | Mục tiêu | Tham chiếu |
|---------|---------|------------|
| Onboarding completion | ≥ 70% | Industry avg 60% |
| Tab switch speed | < 200ms | Momo ~150ms |
| AI first response | < 3 giây | Nhanh hơn Zalo reply |
| Celebration animation | < 2 giây | Không che nội dung |
| Countdown update (Optimistic) | < 100ms | Trước server confirm |

## Design System Foundation

### Lựa chọn: Material Design 3 (Customized)

**Lý do:**
- 80% user VN dùng Android → Material = quen thuộc
- MVP cần nhanh → component có sẵn
- Flutter hỗ trợ tốt nhất Material Design
- Dark mode built-in, Accessibility built-in

### Tùy chỉnh thương hiệu

| Yếu tố | Material mặc định | Solo Exit |
|--------|-------------------|----------|
| Màu chính | Blue/Purple | Gradient warm (cam-vàng = tự do, hy vọng) |
| Font | Roboto | **Be Vietnam Pro** (font VN, miễn phí) |
| Border radius | 12px | 16-20px (mềm hơn, thân thiện) |
| Icon style | Material Icons | **Phosphor Icons** (outline, hiện đại) |
| Animation speed | 200ms | 250-300ms (mượt hơn) |
| Dark mode | Manual toggle | Auto theo giờ hệ thống |

### Component dùng sẵn từ Material

| Component | Sử dụng cho |
|-----------|------------|
| Bottom Navigation Bar | 5 tab chính |
| FAB (Floating Action) | Nút "+" nhập thu nhập |
| Text Field + Slider | Onboarding nhập số |
| Card | Kỹ năng cards, Share Card |
| Bottom Sheet | Chi tiết tính toán |
| Snackbar | Thông báo nhẹ |
| Dialog | Xác nhận xóa, paywall |
| Chip | Tag kỹ năng, bộ lọc |

### Component cần custom

| Component | Lý do custom |
|-----------|-------------|
| Countdown Display | Hero number lớn, animation đặc biệt |
| AI Chat Interface | Chat bubble + typing + streaming |
| Skill Tower | Gamification visual độc đáo |
| Share Card | Template ảnh story |
| Progress Stepper | "Bước 1/5" custom style |

## Defining Experience

### Trải nghiệm định nghĩa

> **"Nhập thu nhập → Đếm ngược GIẢM → Tự do gần hơn"**

Khi ai hỏi "Solo Exit là gì?" — user trả lời: "App cho biết còn bao nhiêu tháng nữa mình có thể nghỉ việc đi làm riêng."

### Mô hình tư duy user

| User nghĩ | Thực tế | UX làm gì |
|----------|---------|----------|
| "Không biết bắt đầu" | Chỉ cần 3 số | Slider đơn giản |
| "Nghỉ việc = rủi ro" | Tính toán được | Đếm ngược = rủi ro thành con số |
| "Cô đơn" | Nhiều người giống | AI + Social proof |
| "Bao giờ đủ?" | Thu nhập phụ ≥ chi tiêu | Đếm ngược trực quan |

### Tiêu chí thành công

| # | Tiêu chí | Mục tiêu |
|---|---------|--------|
| 1 | Time to first value (TTFV) | < 60 giây |
| 2 | "OMG moment" | Screenshot/share rate |
| 3 | Day-1 retention | ≥ 30% (MVP), ≥ 40% (sau optimize) |
| 4 | Nhập thu nhập phụ tuần 1 | Conversion rate |
| 5 | Session frequency | Tăng sau khi đếm ngược giảm |

### Cơ chế trải nghiệm (4.5 bước)

**Bước 1 — Bắt đầu:**
Mở app → "Bạn muốn biết còn bao lâu để tự do?" → [Bắt đầu ngay]

**Bước 2 — Tương tác:**
Slider lương → Slider chi tiêu → Tiết kiệm (hoặc "Tôi không biết")

**Bước 3 — Phản hồi:**
Animation build-up → "9 THÁNG 12 NGÀY" → Confetti → "✅ Bước 1/5!"

**Bước 3.5 — "What if" moment:**
"Nếu bạn kiếm thêm 5 triệu/tháng?" → Slider thu nhập phụ → đếm ngược GIẢM real-time → "6 THÁNG 3 NGÀY!"
→ AHA moment thứ hai: user thấy CON ĐƯỜNG rút ngắn

**Bước 4 — Hoàn thành:**
Home hiện đếm ngược → Widget sẵn → AI: "Chào [tên]! Mình cùng rút ngắn nhé 💪"

### Edge Cases

| Tình huống | Đếm ngược | UX phản hồi |
|-----------|------------|------------|
| Thu nhập phụ ≥ chi tiêu | 0 ngày | "🎉 Bạn ĐÃ SẴN SÀNG! Thời điểm tốt nhất là BÂY GIờ." |
| Tiết kiệm = 0, không thu nhập phụ | Rất dài | "Đừng lo! Mục tiêu đầu: kiếm thêm 2 triệu/tháng" |
| Lương rất cao nhưng chi tiêu cũng cao | Dài | Gợi ý cắt giảm, focus tăng thu |
| User không biết tiết kiệm | Ước tính | Dùng mức trung bình VN, nhắc update sau |
