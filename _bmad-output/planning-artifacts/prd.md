---
stepsCompleted: ['step-01-init', 'step-02-discovery', 'step-02b-vision', 'step-02c-executive-summary', 'step-03-success', 'step-04-journeys', 'step-05-domain', 'step-06-innovation', 'step-07-project-type', 'step-08-scoping', 'step-09-functional', 'step-10-nonfunctional', 'step-11-polish', 'step-12-complete']
inputDocuments:
  - planning-artifacts/product-brief-Solo-Exit-2026-03-05.md
  - brainstorming/brainstorming-session-2026-03-05-175851.md
workflowType: 'prd'
documentCounts:
  briefs: 1
  research: 0
  brainstorming: 1
  projectDocs: 0
classification:
  projectType: 'Mobile App → Platform (MVP: Mobile-first)'
  domain: 'Entrepreneurship + Career Tech + Personal Finance + AI Coaching'
  complexity: 'Medium-High'
  projectContext: 'Greenfield'
  scopeExclusions:
    - 'Family sharing via web link'
---

# Product Requirements Document - Solo Exit

**Author:** NgocBich
**Date:** 2026-03-06

**Mục lục:**
1. [Executive Summary](#executive-summary)
2. [Project Classification](#project-classification)
3. [Success Criteria](#success-criteria)
4. [Product Scope](#product-scope)
5. [User Journeys](#user-journeys)
6. [Domain-Specific Requirements](#domain-specific-requirements)
7. [Innovation & Novel Patterns](#innovation--novel-patterns)
8. [Mobile App Specific Requirements](#mobile-app-specific-requirements)
9. [Project Scoping & Phased Development](#project-scoping--phased-development)
10. [Functional Requirements](#functional-requirements)
11. [Non-Functional Requirements](#non-functional-requirements)
12. [Giả định & Phụ thuộc](#giả-định--phụ-thuộc)

## Executive Summary

**Solo Exit** là ứng dụng mobile-first platform sử dụng AI để đồng hành người dùng trên toàn bộ hành trình từ nhân viên đến chủ doanh nghiệp solo (solopreneur). Sản phẩm giải quyết vấn đề cốt lõi: **5-8 triệu người Việt Nam muốn thoát khỏi công việc làm thuê nhưng không có lộ trình rõ ràng** — dẫn đến 60-80% thất bại khi "nhảy rồi tính" hoặc mãi mãi dừng ở giai đoạn "muốn".

Ứng dụng hoạt động theo 2 giai đoạn:
- **Phase 1 — THOÁT:** Trong khi vẫn đi làm, Solo Exit cung cấp đếm ngược tự do, máy tính tài chính, xây tháp kỹ năng, chế độ kiếm thêm bí mật, và AI companion — biến mơ ước mơ hồ thành lộ trình đo lường được.
- **Phase 2 — ĐẾ CHẾ:** Sau khi nghỉ, AI agents xử lý vận hành (marketing, kế toán, customer service), Revenue Autopilot tối ưu doanh thu, và hệ thống tự động hóa giúp 1 người vận hành như đội ngũ 50 người.

Đối tượng MVP: Nhân viên văn phòng 25-35 tuổi, lương 15-30 triệu, muốn thoát 9-to-5 nhưng không biết bắt đầu từ đâu. Khoảnh khắc thay đổi cuộc đời: **khi thu nhập thụ động gấp đôi lương hiện tại** — người dùng không còn "muốn nghỉ" mà là "CHỌN khi nào nghỉ."

### What Makes This Special

1. **Bản đồ hành trình trọn vẹn:** App duy nhất bao phủ từ "muốn nghỉ" → "đã nghỉ" → "thành công" — không ai trên thị trường VN giải quyết toàn bộ hành trình.
2. **AI hiểu cả chiến lược lẫn cảm xúc:** Không chỉ công cụ tính toán — AI companion hiểu nỗi sợ bị phán xét, hội chứng kẻ mạo danh, cô đơn trên hành trình, và tư vấn 24/7 bằng tiếng Việt.
3. **Thiết kế cho bối cảnh Việt Nam:** Luật lao động VN, văn hóa "giữ thể diện", áp lực gia đình, mức lương VN — không phải bản dịch từ sản phẩm US/EU.
4. **Blue ocean timing:** AI democratization (GPT/Claude) lần đầu làm "1 người = đội 50 người" khả thi + thị trường solopreneur VN chưa có ai phục vụ = cửa sổ cơ hội lớn.
5. **Hào dữ liệu (Data Moat):** Mỗi user journey tạo dữ liệu. Sau 10,000 users → AI dự đoán chính xác hơn → đối thủ không thể bắt kịp.

## Project Classification

| Tiêu chí | Giá trị |
|----------|---------|
| **Loại dự án** | Mobile App → Platform (MVP: Mobile-first, mở rộng web dashboard Phase 2) |
| **Lĩnh vực** | Entrepreneurship + Career Tech + Personal Finance + AI Coaching |
| **Độ phức tạp** | Medium-High (AI NLP tiếng Việt, multi-phase UX, payment, community matching) |
| **Bối cảnh** | Greenfield — sản phẩm hoàn toàn mới |

## Success Criteria

### User Success

**Thu nhập thụ động — Milestone theo giai đoạn:**

| Giai đoạn | Mục tiêu | Ý nghĩa |
|-----------|----------|----------|
| MVP (3 tháng) | Thu nhập phụ > 0đ | "Tôi kiếm được tiền ngoài lương!" |
| Growth (6 tháng) | ≥ 50% lương | "Nửa lương rồi, thấy đường!" |
| Target (12 tháng) | ≥ 100% lương | "Bằng lương, tôi có thể nghỉ" |
| WOW (18+ tháng) | ≥ 200% lương | "GẤP ĐÔI! Tôi CHỌN nghỉ!" |

**Các chỉ số khác:**

| Tiêu chí | MVP | 6 tháng | 12 tháng |
|----------|-----|---------|----------|
| Hoàn thành hành trình | — | 5% | 15% |
| Tự tin nghỉ việc | 3→5/10 | 5→6/10 | 6→7/10 |
| Rút ngắn thời gian | — | — | Nhanh hơn 20% |
| Tương tác cộng đồng | AI companion only | ≥ 2/tuần | ≥ 3/tuần |

### Business Success

| Giai đoạn | Chỉ số | Mục tiêu |
|-----------|--------|----------|
| **3 tháng** | Người đăng ký | 5,000 |
| | DAU/MAU | 30% |
| | Chuyển đổi trả tiền | 5% (250 người) |
| **6 tháng** | Tổng users | 20,000 |
| | MRR | 50 triệu VNĐ |
| | Retention D30 | 40% |
| **12 tháng** | Tổng users | 100,000 |
| | MRR | 300 triệu VNĐ |
| | Câu chuyện thành công | ≥ 50 |
| | App Store rating | ≥ 4.5 sao |

### Technical Success

| Tiêu chí | Mục tiêu |
|----------|----------|
| App load time | < 2 giây |
| Crash rate | < 0.5% |
| AI companion satisfaction | ≥ 4/5, response < 3 giây |
| Tỷ lệ bấm nâng cấp (paywall) | ≥ 5% |
| Data security | Zero breach, mã hóa E2E |

### Measurable Outcomes (KPIs)

| KPI | Mục tiêu |
|-----|----------|
| Activation rate (tải → hoàn thành đếm ngược) | ≥ 40% |
| Week-4 retention | ≥ 25% |
| LTV | ≥ 1.5 triệu VNĐ |
| CAC | ≤ 100K VNĐ |
| LTV/CAC | ≥ 3:1 |
| North Star: users đạt milestone/tháng | +20% MoM |

## Product Scope

### MVP (Persona Minh — nhân viên muốn thoát)

| # | Tính năng | Lý do |
|---|-----------|-------|
| 1 | 🔢 Đếm ngược tự do | Hook, mở app mỗi ngày |
| 2 | 📊 Máy tính tài chính | "Bao lâu tôi nghỉ được?" |
| 3 | 🎯 Xây tháp kỹ năng | AI gợi ý lộ trình |
| 4 | 🕵️ Chế độ kiếm thêm | Side-hustle + tracking |
| 5 | 🌙 AI Companion | Cảm xúc + tư vấn 24/7 |
| 6 | 👤 Tài khoản | Auth + data |

**Fail criteria:** < 5K users, < 25% W4 retention, < 250 paying, < 4.0 sao → pivot

> Chi tiết chiến lược MVP, đội ngũ, timeline và rủi ro: xem [Project Scoping & Phased Development](#project-scoping--phased-development)

### Growth Features (Post-MVP)

| Đợt | Tính năng | Persona |
|-----|-----------|---------|
| Đợt 2 | Gương soi, DNA, Lá chắn cô đơn | Hùng (30-40t) |
| Đợt 3 | AI dashboard, Revenue Autopilot, Web | Linh (solopreneur) |

### Vision (Future)

| Năm | Phát triển |
|-----|-----------|
| Năm 1 | MVP → cộng đồng + Hùng |
| Năm 2 | Phase 2 Đế chế + Linh |
| Năm 3 | Hệ sinh thái + B2B |

## User Journeys

### 🎯 Journey 1: Minh — "Từ 23h đêm đến ngày tự do" (MVP — Happy Path)

**Minh, 27 tuổi, dev frontend, lương 22 triệu.**

**Opening Scene:** 23h chủ nhật. Minh lướt TikTok thấy video "3 điều tôi ước mình biết TRƯỚC khi nghỉ việc." Quảng cáo Solo Exit: *"Bạn muốn nghỉ? Tính xem còn bao lâu."*

**Rising Action:**
- Tải app. **Quick-start 3 câu hỏi** (dưới 60 giây): nhập lương (22tr), chi tiêu (15tr), tiết kiệm (47tr) → app hiện ngay: **"CÒN 9 THÁNG 12 NGÀY"** — con số chính xác, ấn tượng mạnh.
- AI Companion phân tích kỹ năng dev + sở thích viết → gợi ý: **Tech content creator + Freelance dev**
- Xây tháp kỹ năng: SEO writing (4 tuần) + Video editing (2 tuần). 30 phút mỗi tối.
- Chế độ kiếm thêm: viết blog React, không conflict NDA. Tháng đầu: 2 triệu. Đếm ngược: **8 tháng 3 ngày**.

**Climax:** Tháng 5 — thu nhập phụ 15 triệu. Đếm ngược: **3 tháng 8 ngày**. AI: *"Nhanh hơn 44%!"* Minh sợ, nhắn AI lúc 22h. AI: *"847 người giống bạn đã thành công. Thu nhập phụ = 68% lương. Bạn đang XÂY lưới, không nhảy mà không lưới."*

**Resolution:** Tháng 7 — nghỉ việc. Thu nhập 35tr, làm 30h/tuần. Share lên cộng đồng.

### ⚠️ Journey 2: Minh — "Khi mọi thứ không theo kế hoạch" (MVP — Edge Case)

- Tháng 3: Sếp tăng lương 30%. Minh phân vân. AI chạy lại phân tích.
- Tháng 4: Blog bị Google phạt, thu nhập tụt 10tr→3tr. Đếm ngược TĂNG NGƯỢC. AI: *"73% solopreneur có ít nhất 1 setback. Mình tính Plan B nhé?"*
- Minh bỏ app 2 tuần. AI notification nhẹ: *"Không sao. 67% cũng nghỉ giữa chừng."*
- **Re-entry:** Minh mở lại app → *"Dù bạn nghỉ, tiết kiệm vẫn ở đó. Đếm ngược đã điều chỉnh. Sẵn sàng tiếp tục?"* — không guilt-trip, chỉ welcome back.
- Minh điều chỉnh kế hoạch. Chậm hơn nhưng tiến.

### 💰 Journey 3: Free → Paid — "Khi nào đáng tiền?" (MVP)

- Free: đếm ngược + basic calculator + community read-only. Đủ hook.
- Tuần 2: Minh muốn Skill Stack chi tiết → paywall: *"Mở khóa AI kỹ năng + side-hustle cá nhân hóa — 99K/tháng"*
- **Trigger upgrade:** User ĐÃ THẤY GIÁ TRỊ → muốn THÊM → trả tiền là natural next step.
- Minh upgrade → AI Companion full context, Stealth Hustle gợi ý cụ thể. *"99K/tháng cho lộ trình đổi đời? Pha cà phê cả tháng còn hơn."*

### 🧑‍🎓 Journey 4: Phúc — "Gen Z chưa biết mình muốn gì" (Đợt 4)

**Phúc, 22 tuổi, admin, lương 12 triệu.**

- Tải app miễn phí. Không có đếm ngược — chưa biết muốn nghỉ để làm gì.
- **Khám phá DNA:** quiz + AI → *"Bạn giỏi tổ chức, thích sáng tạo, introvert. 3 hướng: Virtual Assistant, Event Planner online, Content Manager."*
- Thử side-hustle VA. Thu nhập đầu: 1.5tr/tháng.
- 6 tháng sau → *"À, mình thích Content Manager!"* → Bật đếm ngược → trở thành "Minh".
- Convert free → paid. Hành trình bắt đầu.

### 💼 Journey 5: Hùng — "Xây lưới bí mật" (Đợt 2)

**Hùng, 36 tuổi, trưởng phòng marketing, lương 42 triệu, 2 con.**

- Đếm ngược: **2 NĂM 4 THÁNG**. OK với timeline dài.
- Mỗi tối 1 giờ xây side-business tư vấn marketing SMEs. AI track nhẹ nhàng.
- 6 tháng: side-income 15tr. Thu nhập phụ = 60% lương. Hùng tự show vợ xem trên app.
- CHỌN ở thêm 6 tháng. Thu nhập phụ vượt lương → nghỉ chủ động. PRO user 299K/tháng.

### 😤 Journey 6: Linh — "Solopreneur kiệt sức" (Đợt 3)

**Linh, 31 tuổi, UX freelance, 8 tháng sau nghỉ. 28tr/tháng, 65h/tuần.**

- Nhảy thẳng Phase 2. AI scan: *"43% thời gian là repeatable. 5 tasks automate NGAY."*
- AI phân tích clients: *"Drop Client C = free time cho upsell Client A."*
- Kết quả: 35tr/tháng, 30h/tuần. *"Cuối tuần lại có thời gian cho con."*

### 🔧 Journey 7: Admin/Ops (MVP — Tool bên thứ 3)

- Dùng **Firebase Analytics + Mixpanel + Sentry**. Không build admin panel riêng trong MVP.
- Monitor: DAU, signups, churn, AI feedback scores
- Sự cố AI advice sai → flag trong Sentry → fix → notify user

### Journey Requirements Summary

| Journey | Capabilities | Phase |
|---------|-------------|-------|
| **Minh Happy** | Quick-start onboarding, countdown engine, AI skill analysis, side-hustle matching, AI companion, progress tracking | MVP |
| **Minh Edge** | Re-engagement notifications, re-entry welcome, plan recalculation, setback detection, emotional recovery | MVP |
| **Free→Paid** | Freemium gateway, paywall triggers, upgrade flow, pricing display | MVP |
| **Phúc** | DNA discovery quiz, skill exploration, no-countdown entry, free→paid | Đợt 4 |
| **Hùng** | Long-term mode, gentle notifications, premium subscription | Đợt 2 |
| **Linh** | Phase 2 direct entry, automation audit, client analysis | Đợt 3 |
| **Admin/Ops** | *Firebase + Mixpanel + Sentry. Không build riêng trong MVP.* | Tool 3rd-party |

## Domain-Specific Requirements

Domain Entrepreneurship/Career Tech — không thuộc ngành quy định nặng. Yêu cầu domain nhẹ:

| Yêu cầu | Chi tiết | Mức độ |
|----------|----------|--------|
| **Payment** | App Store/Google Play IAP cho subscription. Tuân thủ Apple/Google policies. | Standard |
| **Dữ liệu tài chính** | Thu chi user chỉ là input/output số — KHÔNG xử lý tiền thật. Mã hóa at-rest và in-transit. | Trung bình |
| **AI Disclaimer** | AI companion advice cần disclaimer: "Không phải tư vấn tài chính/pháp lý chuyên nghiệp." | Bắt buộc |
| **Luật lao động VN** | AI cần hiểu cơ bản: thời hạn thông báo nghỉ, quyền BHXH, non-compete/NDA phổ biến. | Nên có |

## Innovation & Novel Patterns

### Detected Innovation Areas

| # | Innovation | Mô tả | Mức độ |
|---|-----------|--------|--------|
| 1 | **Freedom Countdown™** | Biến ước mơ → con số đếm ngược cụ thể, cập nhật real-time. Chưa app nào có. | 🔴 Đột phá |
| 2 | **Hệ thống tích hợp** | Đổi mới thật = cách KẾT HỢP countdown + coaching cảm xúc + lộ trình kỹ năng. Không phải từng piece riêng lẻ mà là hệ thống hoàn chỉnh. | 🔴 Đột phá |
| 3 | **AI Companion hiểu cảm xúc** | Ứng dụng sáng tạo của AI có sẵn (GPT/Claude) — thiết kế trải nghiệm độc đáo: hiểu sợ, cô đơn, tự ti + ngữ cảnh VN. | 🟡 Ứng dụng sáng tạo |
| 4 | **Dual-Phase** | 1 app, 2 giai đoạn (THOÁT→ĐẾ CHẾ). User tiến hóa thay vì rời đi. | 🟡 Mới lạ |
| 5 | **Stealth Hustle** | AI gợi ý side-hustle không xung đột NDA/công việc hiện tại. | 🟡 Mới lạ |
| 6 | **Bản địa hóa sâu VN** | Thiết kế gốc cho VN, không phải bản dịch. | 🟢 Lợi thế cạnh tranh |

### Bối cảnh thị trường & Đối thủ

| Đối thủ | Họ làm gì | Solo Exit khác gì |
|---------|-----------|-------------------|
| **Indie Hackers** | Cộng đồng solopreneur (tiếng Anh) | AI cá nhân hóa + lộ trình + tiếng Việt |
| **FIRE apps** | Tính tài chính nghỉ hưu sớm | Cho NGHỈ VIỆC để tự kinh doanh, không phải nghỉ hưu |
| **BetterUp** | 1-on-1 coaching ($$$) | AI coaching 24/7, giá 99K/tháng |
| **Skillshare/Udemy** | Học kỹ năng chung chung | Gợi ý DỰA TRÊN phân tích cá nhân |
| **TikTok/YouTube creators** | Dạy "nghỉ việc làm freelance" MIỄN PHÍ | TikTok = advice chung. Solo Exit biết lương, chi tiêu, kỹ năng CỤ THỂ → advice CỤ THỂ. Cá nhân hóa = lý do trả tiền. |

### Cách kiểm chứng

| Innovation | Kiểm chứng bằng | Thời gian |
|-----------|-----------------|----------|
| Countdown | So sánh: có vs không → giữ chân tuần 1 | MVP tuần 1-4 |
| AI Companion | Khảo sát hài lòng + thời gian dùng + dùng lại | MVP tháng 1-3 |
| Stealth Hustle | % kích hoạt + thu nhập phụ tạo ra | MVP tháng 2-4 |
| **Thời gian đến giá trị đầu tiên** | Mở app → thấy đếm ngược = **dưới 60 giây** | MVP tuần 1 |
| Dual-Phase | % chuyển Phase 1→2 | Dài hạn |

> Rủi ro liên quan đến innovation đã được gộp vào [Chiến lược giảm rủi ro](#chiến-lược-giảm-rủi-ro) trong phần Project Scoping.

## Mobile App Specific Requirements

### Tổng quan kỹ thuật

| Câu hỏi | Trả lời |
|---------|--------|
| Native hay Cross-platform? | **Cross-platform** (React Native hoặc Flutter) — 1 codebase cho iOS + Android |
| Cần dùng offline? | **Có giới hạn** — xem đếm ngược + tháp kỹ năng offline. AI cần internet. |
| Push notifications? | **Có** — re-engagement, milestone, AI nhắc nhẹ |
| Tính năng thiết bị? | Biometric auth, widget đếm ngược home screen |
| Tuân thủ App Store? | Apple IAP + Google Play Billing cho subscription |

### Yêu cầu nền tảng

| Nền tảng | Phiên bản tối thiểu | Ghi chú |
|----------|---------------------|--------|
| iOS | 15.0+ | ~95% iPhone VN |
| Android | 10.0+ (API 29) | ~90% Android VN |
| Web dashboard | Chrome/Safari mới nhất | Phase 2 — Đợt 3 |

### Quyền thiết bị

| Quyền | Khi nào hỏi | Bắt buộc? |
|-------|------------|----------|
| Internet | Luôn luôn | Có |
| Push notifications | Sau onboarding xong | Có |
| Biometric | Khi bật bảo mật | Không |

### Chế độ ngoại tuyến

| Tính năng | Offline? | Đồng bộ khi có mạng |
|----------|----------|---------------------|
| Xem đếm ngược | ✅ Có | Tự động |
| Xem tháp kỹ năng | ✅ Có | Tự động |
| Nhập thu chi | ✅ Có | Đẩy lên khi có mạng |
| AI Companion | ❌ Cần internet | — |
| Cộng đồng | ❌ Cần internet | — |

### Chiến lược Push Notification

| Loại | Ví dụ | Tần suất |
|------|-------|---------|
| Đếm ngược milestone | "Chỉ còn 6 tháng!" | Khi đạt milestone |
| AI nhắc nhẹ | "Hôm nay bạn có muốn cập nhật thu nhập?" | 1-2 lần/tuần |
| Tiến trình | "Thu nhập phụ tháng này +30%!" | Hàng tháng |
| Re-engagement | "Không sao, quay lại khi sẵn sàng" | Sau 7 ngày im |
| **Giới hạn cứng** | Tối đa 3-4 notification/tuần | |

### Tuân thủ App Store

| Yêu cầu | Chi tiết |
|----------|--------|
| Apple IAP | Subscription qua Apple IAP. Apple 30% (năm 1), 15% (năm 2+) |
| Google Play Billing | Tương tự Apple IAP cho Android |
| Nội dung | AI advice cần disclaimer, không claim "tư vấn tài chính" |
| Quyền riêng tư | Privacy policy + data handling disclosure |
| Rating | 12+ |

### Cân nhắc kỹ thuật

| Vấn đề | Quyết định |
|--------|----------|
| Framework | React Native hoặc Flutter (quyết định khi Architecture) |
| Database | Local SQLite (offline) + Cloud sync |
| Widget | iOS WidgetKit + Android Widget cho đếm ngược |

> Các hệ thống tích hợp (Firebase, GPT/Claude, Sentry...) xem chi tiết tại [Tích hợp](#tích-hợp) trong Non-Functional Requirements.

## Project Scoping & Phased Development

### Chiến lược MVP

**Loại MVP:** Problem-Solving — chứng minh "đếm ngược tự do + AI companion" THẬT SỰ giúp người dùng hành động.

**Đội ngũ tối thiểu:** 3-5 người (Mobile dev 1-2, AI/Backend 1, UX/UI 1 part-time, Product/Founder 1). Hoặc 1-2 người nếu founder code được.

**Thời gian MVP:** 8-12 tuần

### MVP Feature Set (Phase 1)

**Hành trình hỗ trợ:** Minh (happy + edge) + Free→Paid

| # | Tính năng | Tại sao bắt buộc | Không có thì sao |
|---|-----------|------------------|------------------|
| 1 | 🔢 Đếm ngược tự do | Hook #1, lý do tải app | App vô nghĩa |
| 2 | 📊 Máy tính tài chính (3 câu hỏi) | Giá trị cốt lõi trong 60 giây | Không có WOW moment |
| 3 | 🌙 AI Companion (cơ bản) | Điểm khác biệt #1 | Chỉ là máy tính |
| 4 | 🎯 Tháp kỹ năng (AI gợi ý) | Lộ trình hành động cụ thể | Biết bao lâu nhưng không biết LÀM GÌ |
| 5 | 🕵️ Chế độ kiếm thêm (cơ bản) | Thu nhập phụ → đếm ngược giảm | Chỉ xem mà không hành động |
| 6 | 👤 Auth + Profile | Lưu dữ liệu | Mất data = mất user |
| 7 | 💰 Subscription (freemium) | Doanh thu | Không bền vững |

**Có thể LÀM TAY trong MVP:** Cộng đồng (Telegram/Discord), Nội dung kỹ năng (Google Sheets → API), Admin (Firebase Console + Mixpanel)

### Post-MVP Features

**Phase 2 — Đợt 2 (tháng 4-6):** Gương soi thành công, Giải mã DNA, Lá chắn cô đơn, Chế độ dài hạn (Persona Hùng + Phúc)

**Phase 3 — Đợt 3 (tháng 7-12):** AI Agents dashboard, Revenue Autopilot, Web dashboard, Premium tier 299K (Persona Linh)

### Chiến lược giảm rủi ro

| Loại | Rủi ro | Giảm thiểu |
|------|--------|----------|
| Kỹ thuật | AI response chậm/sai | Claude/GPT API + cache + fallback templates |
| Kỹ thuật | Countdown algorithm | V1 dùng công thức đơn giản, tinh chỉnh sau |
| Thị trường | Không đủ người dùng | Landing page + waitlist TRƯỚC khi build |
| Thị trường | 99K quá đắt? | A/B test: 49K vs 99K vs 149K |
| Tài nguyên | Ít dev | Phiên bản cắt giảm: Countdown + Calculator + Auth (3 tuần) |
| Tài nguyên | Hết tiền | Budget buffer 30% + phiên bản tối thiểu |

## Functional Requirements

### 1. Quản lý tài khoản

- **FR1:** Người dùng có thể đăng ký bằng email hoặc mạng xã hội
- **FR2:** Người dùng có thể đăng nhập/đăng xuất
- **FR3:** Người dùng có thể bảo mật tài khoản bằng vân tay/Face ID
- **FR4:** Người dùng có thể tạo và chỉnh sửa hồ sơ cá nhân (tên, nghề nghiệp, mục tiêu)
- **FR5:** Hệ thống có thể xóa toàn bộ dữ liệu người dùng khi được yêu cầu

### 2. Đếm ngược tự do

- **FR6:** Người dùng có thể nhập thông tin tài chính (lương, chi tiêu, tiết kiệm) trong dưới 60 giây
- **FR7:** Hệ thống có thể tính và hiển thị đếm ngược dựa trên dữ liệu tài chính
- **FR8:** Đếm ngược tự động cập nhật khi thu nhập phụ thay đổi
- **FR9:** Người dùng có thể xem đếm ngược trên widget màn hình chính (iOS + Android)
- **FR10:** Người dùng có thể chỉnh sửa thông tin tài chính bất kỳ lúc nào
- **FR11:** Hệ thống hiển thị % thay đổi so với kế hoạch ban đầu

### 3. AI Companion

- **FR12:** Người dùng có thể trò chuyện với AI bằng tiếng Việt
- **FR13:** AI có thể phân tích kỹ năng và sở thích để gợi ý hướng đi
- **FR14:** AI có thể hỗ trợ về mặt cảm xúc (sợ, cô đơn, tự ti)
- **FR15:** AI hiển thị disclaimer "Không phải tư vấn tài chính/pháp lý chuyên nghiệp"
- **FR16:** AI có thể tham khảo dữ liệu cộng đồng ẩn danh ("X người giống bạn đã thành công")
- **FR17:** Người dùng có thể đánh giá chất lượng phản hồi AI (👍/👎)

### 4. Tháp kỹ năng

- **FR18:** AI có thể đề xuất kỹ năng cần học dựa trên phân tích cá nhân
- **FR19:** Người dùng có thể xem lộ trình kỹ năng với thời gian ước tính
- **FR20:** Người dùng có thể đánh dấu kỹ năng đã hoàn thành
- **FR21:** Hệ thống cập nhật tháp kỹ năng khi hoàn thành hoặc thêm mới

### 5. Chế độ kiếm thêm (Stealth Hustle)

- **FR22:** AI có thể gợi ý side-hustle phù hợp dựa trên kỹ năng và ngành nghề
- **FR23:** AI lọc gợi ý để tránh xung đột NDA/công việc hiện tại
- **FR24:** Người dùng có thể theo dõi thu nhập phụ hàng tháng
- **FR25:** Hệ thống tự động cập nhật đếm ngược khi nhập thu nhập phụ mới
- **FR26:** Người dùng có thể xem lịch sử thu nhập phụ theo thời gian

### 6. Subscription & Thanh toán (MVP — Freemium giả)

- **FR27:** Người dùng có thể dùng miễn phí với tính năng giới hạn (đếm ngược + calculator cơ bản)
- **FR28:** Người dùng có thể kích hoạt premium qua mã khuyến mãi hoặc nút kích hoạt (Apple IAP/Google Play Billing bổ sung sau MVP)
- **FR29:** Hệ thống hiển thị paywall tại điểm trigger tự nhiên — đo % bấm nâng cấp
- **FR30:** Hệ thống quản lý trạng thái free/premium cho từng tính năng

### 7. Thông báo & Re-engagement

- **FR31:** Hệ thống gửi thông báo khi đạt milestone đếm ngược
- **FR32:** Hệ thống gửi nhắc nhẹ (tối đa 3-4 lần/tuần)
- **FR33:** Hệ thống gửi thông báo re-engagement sau 7 ngày không dùng
- **FR34:** Khi quay lại app, người dùng thấy màn hình welcome back

### 8. Dữ liệu & Đồng bộ

- **FR35:** Dữ liệu người dùng được lưu cục bộ và đồng bộ lên cloud
- **FR36:** Người dùng có thể xem đếm ngược và tháp kỹ năng khi không có internet
- **FR37:** Dữ liệu tài chính được mã hóa at-rest và in-transit
- **FR38:** Người dùng có thể nhập thu chi khi offline, đồng bộ khi có mạng

## Non-Functional Requirements

### Hiệu năng

| Chỉ số | Mục tiêu | Tại sao |
|--------|---------|--------|
| Mở app → thấy đếm ngược | < 2 giây | Trải nghiệm mượt |
| Onboarding → kết quả | < 60 giây (UX) | Thời gian đến giá trị đầu tiên |
| AI Companion phản hồi | < 5 giây | Nhanh hơn = tự nhiên hơn |
| Cập nhật đếm ngược | < 1 giây | Cảm giác real-time |
| Crash rate | < 1% | App Store yêu cầu |

### Bảo mật

| Yêu cầu | Chi tiết |
|----------|--------|
| Mã hóa dữ liệu | AES-256 at-rest, TLS 1.3 in-transit |
| Xác thực | JWT tokens + biometric optional |
| Dữ liệu tài chính | Không lưu trên thiết bị dưới dạng plaintext |
| AI conversation logs | Mã hóa, ẩn danh hóa khi dùng cho training |
| Xóa tài khoản | Xóa toàn bộ trong 30 ngày |
| API security | Rate limiting, API key rotation, không expose AI key phía client |

### Khả năng mở rộng

| Giai đoạn | Người dùng đồng thời | Ghi chú |
|-----------|---------------------|--------|
| MVP launch | 500 | Beta |
| 3 tháng | 5,000 | Mở rộng |
| 12 tháng | 50,000 | Auto-scaling |
| Kiến trúc | Scale 10x không đổi kiến trúc | |

### Tích hợp

| Hệ thống | Mục đích | Mức độ |
|----------|---------|--------|
| GPT/Claude API | AI Companion | Bắt buộc |
| Firebase Auth | Đăng nhập/đăng ký | Bắt buộc |
| Firebase Cloud | Đồng bộ dữ liệu | Bắt buộc |
| Mixpanel/Analytics | Tracking hành vi | Bắt buộc |
| Sentry | Crash reporting | Bắt buộc |
| Apple IAP / Google Play | Thanh toán | Sau MVP |

### Trợ năng (cơ bản)

| Yêu cầu | Chi tiết |
|----------|--------|
| Font size | Hỗ trợ Dynamic Type (iOS) / Font Scale (Android) |
| Contrast | Đủ contrast ratio cho đếm ngược |
| Screen reader | Label cho các nút chính (cơ bản) |

## Giả định & Phụ thuộc

### Giả định

| # | Giả định | Nếu sai thì |
|---|----------|-------------|
| 1 | Người dùng có smartphone (iOS 15+ hoặc Android 10+) | Giảm thị trường khả dụng |
| 2 | Người dùng có internet ổn định (cho AI Companion) | AI offline cần fallback |
| 3 | Người dùng biết đọc tiếng Việt | Không cần đa ngôn ngữ MVP |
| 4 | Người dùng sẵn sàng nhập dữ liệu tài chính | Nếu không → đếm ngược không hoạt động |
| 5 | 5-8 triệu người VN muốn thoát việc = thị trường đủ lớn | Validate qua landing page trước |

### Phụ thuộc

| Hệ thống | Tại sao phụ thuộc | Rủi ro nếu lỗi |
|----------|-------------------|----------------|
| GPT/Claude API | AI Companion không hoạt động nếu API down | Fallback: template responses |
| Firebase | Auth + Cloud sync ngừng → app mất dữ liệu | SLA 99.95% — rủi ro thấp |
| Apple App Store | Review time 1-7 ngày, có thể reject | Tuân thủ guidelines từ đầu |
| Google Play Store | Review time 1-3 ngày | Tương tự Apple |

