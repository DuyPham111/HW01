# Appendix A — Prompt Log (AI Conversation Record)

| Trường | Nội dung |
|--------|----------|
| **Môn học** | CS423 / CSC15003 — Software Testing (AI-augmented · 2026) |
| **Bài tập** | HW01-AI |
| **Sinh viên** | Phạm Vũ Ngọc Duy — 23127183 — KTPM4 |
| **AI Tool sử dụng** | Claude Sonnet 4.6 — claude.ai |
| **Ngày thực hiện** | 04/06/2026 |
| **Tổng số prompt** | 16 |
| **Mục đích log** | Minh chứng sử dụng AI + tự đánh giá mức độ thành thạo AI theo thời gian |

---

> **Cách đọc log này:**
> - *Prompt gửi* = nội dung chính xác (hoặc gần đúng) bạn gửi cho AI.
> - *Claude cung cấp* = mô tả đủ nội dung Claude trả về — không tóm tắt quá mức.
> - *Output chính* = artifact cụ thể được sinh ra trong lượt đó.
> - *Loại tác vụ* = phân loại để tự đánh giá kỹ năng sử dụng AI.
> - ⚠️ Điền chính xác [HH:MM] theo thời gian thực khi bạn gửi prompt.

---

## Prompt #01 — Đọc 2 file PDF và lập lộ trình làm bài HW01

- **Thời gian:** [18:15] 03/06/2026
- **Tool:** Claude Sonnet 4.6 — claude.ai
- **Loại tác vụ:** Planning / Roadmap generation
- **Bloom-AI Level:** G9.1 (Understand) + G9.5 (Create — tổng hợp kế hoạch)

**Prompt gửi:**
> *[Upload file: ___2026_Homework_Policies.pdf + 2026_HW01_Jobs_Defects_PhysicalProduct_En.pdf]*
> "Tôi có bài tập hw01 này và file policy hãy đọc 2 file đó và lập lộ trình làm cho tôi và xây dựng khung tổng quát để tôi làm, kèm hướng dẫn từng bước để tôi làm"

**Claude cung cấp:**
Claude đọc cả 2 PDF (Homework Policies + HW01 spec) và trước khi sinh file đã cảnh báo 5 điểm quan trọng cần lưu ý ngay:
1. Điểm R3 lệch nhau giữa phần mô tả (40pt) và rubric thật (25pt) → đúng là 25pt.
2. 4 artifact TUYỆT ĐỐI không được AI tạo (ảnh thiết bị+thẻ SV, video giọng mình, ảnh login job platform, prompt log) kèm hậu quả nếu vi phạm.
3. Prompt log phải ghi MỌI prompt kể cả cuộc trò chuyện này — bắt đầu ngay.
4. 3 edge case "AI không tìm ra" phải thật sự do sinh viên tìm.
5. Mantis đã bỏ → dùng GitHub Issues.

Claude sinh file `HW01_LoTrinh_KhungLamBai.md` gồm:
- Bảng tóm tắt luật chơi (format, nộp, git, AI, academic integrity).
- Bảng điểm chính xác theo rubric (40+20+25+8+4+3 = 100).
- Lộ trình 5 giờ phân bổ theo trọng số điểm (R1=75ph, R2=60ph, R3=90ph, AI compliance=30ph, đóng gói=30ph).
- Cấu trúc thư mục + quy tắc Git commit (mỗi bước nhỏ = 1 commit, message rõ).
- Hướng dẫn từng bước cho R1, R2, R3.
- Khung AI Compliance (Audit Report 5-section, Critique 200-300 từ, Disclosure template).
- Khung báo cáo chính với đầy đủ heading.
- Checklist nộp bài 15 mục.

**Output chính:** File `HW01_LoTrinh_KhungLamBai.md`

---

## Prompt #02 — Hướng dẫn chi tiết Requirement 1 kèm link nền tảng tuyển dụng

- **Thời gian:** [08:15] 04/06/2026
- **Tool:** Claude Sonnet 4.6 — claude.ai
- **Loại tác vụ:** Research guidance + Link aggregation
- **Bloom-AI Level:** G9.1 (Understand — hướng dẫn quy trình)

**Prompt gửi:**
> "Rất tốt giờ hãy hướng dẫn tôi chi tiết phần 1 đi cho tôi link chi tiết của các bên để tôi truy cập và các thông tin liên quan, trước hết tôi đã tạo folder các file .md để ghi report và push lên github repo mới giờ hãy hướng dẫn tôi step by step các phần tiếp theo"

**Claude cung cấp:**
Claude tìm kiếm web xác nhận ITviec hiển thị "Posted X days ago" và có tag AI skills, rồi cung cấp:

**Danh sách nền tảng + link lọc sẵn:**
- ITviec: `https://itviec.com/it-jobs/qa-qc/ho-chi-minh-hcm` (ưu tiên nhất vì có nhãn ngày rõ)
- TopCV: `https://www.topcv.vn/tim-viec-lam-qa-qc-tat-tphcm-kl1`
- VietnamWorks: `https://www.vietnamworks.com/qa-qc-jobs-in-ho-chi-minh-i32-l29`
- LinkedIn: `https://www.linkedin.com/jobs/search/?keywords=QA%20QC%20tester&location=Ho%20Chi%20Minh%20City`
- Indeed VN: `https://vn.indeed.com/jobs?q=QA+QC+tester&l=Ho+Chi+Minh`

**Hướng dẫn 7 bước chi tiết:**
1. Cách lọc theo ngày ≤60 ngày (ITviec: đọc label "X days ago" · LinkedIn: "Past month" filter · TopCV: sort by "Mới nhất").
2. Từ khóa để tìm ≥3 tin AI: `AI`, `LLM`, `automation AI`, `Generative AI`, `Playwright AI`, `self-healing test`.
3. Cách chụp screenshot đúng anti-cheat: full màn hình có username/avatar ở góc nav + nhãn ngày đăng.
4. Template markdown mỗi job (6 trường: link · ngày+ảnh · AI? · mô tả · kỹ năng · lương).
5. Bảng tổng hợp 10 dòng để thêm vào cuối R1.
6. Cách viết AI Impact Analysis 1-2 câu (replace/assist/cannot replace) + 3 ví dụ mẫu.
7. Git commit message gợi ý theo từng bước.

**Output chính:** Hướng dẫn inline + template markdown Job block + ví dụ AI Impact Analysis

---

## Prompt #03 — Điền mẫu Job 01 từ link PNJ

- **Thời gian:** [09:15] 04/06/2026
- **Tool:** Claude Sonnet 4.6 — claude.ai
- **Loại tác vụ:** Content generation from URL
- **Bloom-AI Level:** G9.3 (Analyse — phân tích JD + viết AI Impact)

**Prompt gửi:**
> "tôi vừa kiếm được và đây là phần đầu report của tôi hãy hoàn thiện xuống dưới 1 job này để tôi tự làm tương tự https://itviec.com/viec-lam-it/senior-qc-automation-tester-qa-qc-pnj-5542"
> *[Kèm phần đầu report.md đã viết]*

**Claude cung cấp:**
Claude fetch URL ITviec và đọc toàn bộ JD tin PNJ, xác nhận:
- Tin đăng 15 ngày trước → trong cửa sổ 60 ngày ✔
- Có tag kỹ năng "AI" → tính là 1 trong ≥3 tin AI ✔
- Lương ẩn (cần đăng nhập) → hướng dẫn điền sau khi login

Claude sinh block Job 01 hoàn chỉnh với:
- Link, ngày đăng (≈20/05/2026), địa điểm (170 Phan Đăng Lưu, HCM), AI?: ✔ Có.
- Mô tả tóm tắt: kiểm thử sản phẩm truyền thống + AI (accuracy/reliability/fairness of AI outputs, edge case/misuse testing, LLM evaluation tools, synthetic data, CI/CD).
- Kỹ năng: Tester, QA QC, Automation Test, API, A/B testing, AI; tối thiểu 4 năm có ứng dụng AI; ISTQB/Agile ưu tiên.
- AI Impact Analysis: phân tích rõ đây là vị trí "sinh ra nhờ AI" — AI hỗ trợ phần lặp lại (script, synthetic data, LLM eval) nhưng thẩm định độ tin cậy/công bằng AI output và thiết kế misuse cases vẫn cần con người.
- Nhắc: commit `git commit -m "R1: add job 01 (PNJ Senior QC) + AI impact"`.

**Output chính:** Block markdown Job 01 hoàn chỉnh (6 trường + AI Impact Analysis)

---

## Prompt #04 — Điền mẫu Job 02 từ JD TeenUp paste vào

- **Thời gian:** [09:50] 04/06/2026
- **Tool:** Claude Sonnet 4.6 — claude.ai
- **Loại tác vụ:** Content generation from pasted JD
- **Bloom-AI Level:** G9.3 (Analyse — đánh giá AI skill requirement)

**Prompt gửi:**
> *[Paste toàn bộ JD của TEENUP từ ITviec]*
> "giúp tôi tạo cho https://itviec.com/viec-lam-it/product-tester-qa-qc-jira-trello-cong-ty-tnhh-teenup-1256"

**Claude cung cấp:**
Trước khi điền, Claude cảnh báo 2 điểm quan trọng:
1. Vị trí đặt tại **Hà Nội** (không phải HCM) — vẫn hợp lệ vì đề không giới hạn địa điểm.
2. Tin này **KHÔNG tính vào ≥3 tin AI** — tags chỉ có `QA QC, Jira, Trello`; product là TeenCare AI nhưng vị trí không yêu cầu kỹ năng AI/LLM cụ thể.

Claude sinh block Job 02 với: AI?: ✘ Không · Lương: 800–1,500 USD · Mô tả: kiểm thử functional/regression/integration/UAT trên web+mobile cho nền tảng TeenCare AI · AI Impact Analysis: mặc dù JD không yêu cầu kỹ năng AI, việc kiểm thử sản phẩm AI đặt ra thách thức đánh giá "chất lượng quyết định" AI mà công cụ AI khó tự động hóa hoàn toàn.

**Output chính:** Block markdown Job 02 hoàn chỉnh

---

## Prompt #05 — Upload HW01_Report.md để rà soát Requirement 1

- **Thời gian:** [13:15] 04/06/2026
- **Tool:** Claude Sonnet 4.6 — claude.ai
- **Loại tác vụ:** Review / QA
- **Bloom-AI Level:** G9.4 (Evaluate — đánh giá theo rubric)

**Prompt gửi:**
> *[Upload file HW01_Report.md]*
> "Hãy check REQUIREMENT 1 tôi đã làm này xem đã oke chưa để qua phần 2"

**Claude cung cấp:**
Claude đọc toàn bộ file và rà soát 10 job entries (Jobs 01–10: PNJ, Nakivo, Evolus, Mercatus, TeenUp, ABBANK, MiTek, DTS Software, Kingfoodmart, SABITECH).

**Kết quả rà soát:**
- ✅ Đủ 10 tin, tất cả ≤60 ngày (max 23 ngày) ✔
- ✅ Đủ 6 trường mỗi tin ✔
- ✅ AI Impact Analysis đủ cả 10 tin ✔
- ✅ 3 tin AI rõ ràng: Jobs 01 (PNJ), 02 (Nakivo), 09 (Kingfoodmart) ✔

**3 vấn đề cần sửa:**
1. **Job 05 (TeenUp) đánh dấu AI: Có nhưng không đủ cơ sở** — tag chỉ có `QA QC, Jira, Trello`, không có AI skill requirement. Khuyến nghị đổi thành Không (vẫn đủ ≥3 AI với 3 tin kia).
2. **Thiếu bảng tổng hợp** — Claude cung cấp template bảng 10 dòng đầy đủ cột để thêm vào cuối R1.
3. **Screenshots cần kiểm tra thủ công** — tự xác nhận mỗi ảnh hiện username/avatar.

**Output chính:** Kết quả review chi tiết + template bảng tổng hợp 10 job

---

## Prompt #06 — Chuyển sang Requirement 2

- **Thời gian:** [13:30] 04/06/2026
- **Tool:** Claude Sonnet 4.6 — claude.ai
- **Loại tác vụ:** Planning + Research guidance
- **Bloom-AI Level:** G9.1 (Understand — nắm quy trình R2)

**Prompt gửi:**
> "Chuyển sang Requirement 2"

**Claude cung cấp:**
Claude tìm kiếm web về AI Incident Database và sự cố AI 2025, rồi cung cấp:

**Nhắc lại twist quan trọng của R2:** với MỖI trong 20 lỗi, phải nhờ AI giải thích → chỉ ra 1 chỗ AI bị bias/hallucinate → 20 instances tổng cộng. Đây là dữ liệu cho AI Audit Report.

**Nguồn tra cứu với link:**
- NVD: `https://nvd.nist.gov/vuln/search`
- CVE.org: `https://www.cve.org`
- CISA KEV: `https://www.cisa.gov/known-exploited-vulnerabilities-catalog`
- AI Incident Database: `https://incidentdatabase.ai`
- AIAAIC: `https://www.aiaaic.org/aiaaic-repository`

**Danh sách ứng viên defect gợi ý:**
- AI/LLM (≥5 cần): Air Canada chatbot (2024), Bard JWST (2023), ChatGPT Redis leak (2023), Mata v. Avianca (2023), Replit AI xóa DB (2025), Chicago Sun-Times sách ma (2025), Chevrolet chatbot $1 (2023), Google AI Overviews (2024), Gemini image generation (2024).
- Non-AI: CrowdStrike (2024), Log4Shell (2022), MOVEit (2023), XZ Utils (2024), Southwest meltdown (2022).

**Template mỗi defect:** 8 trường (Loại, Nguồn, Ngày, Mô tả, Severity, Hậu quả, Giải pháp, 🔍 AI bias/hallucination).

**Bí quyết tìm hallucination:** ép AI nói số liệu cụ thể (ngày, CVE, số tiền, số thiết bị) rồi đối chiếu với nguồn gốc.

**Output chính:** Hướng dẫn R2 + nguồn tra cứu + danh sách ứng viên + template defect

---

## Prompt #07 — Tạo đoạn md R2 và làm mẫu 3 defect AI + 3 non-AI

- **Thời gian:** [15:25] 04/06/2026
- **Tool:** Claude Sonnet 4.6 — claude.ai
- **Loại tác vụ:** Content generation (structured markdown)
- **Bloom-AI Level:** G9.5 (Create — tạo cấu trúc + nội dung)

**Prompt gửi:**
> "Hãy tạo giúp tôi đoạn md cho Requirement 2 và làm mẫu 3 cái cho ai và non-ai cho tôi"

**Claude cung cấp:**
Claude xác minh số liệu trước (Air Canada $812.02 CAD, Optus 9.8M) rồi sinh đoạn markdown hoàn chỉnh gồm:

**6 defect mẫu đầy đủ 8 trường:**
- Defect 01: Air Canada Chatbot (AI) — $812,02 CAD = 650,88+36,14+125 CAD
- Defect 02: Google Bard JWST Error (AI) — ~100 tỷ USD vốn hóa
- Defect 03: ChatGPT Redis Data Leak (AI) — lỗi redis-py library
- Defect 04: Log4Shell CVE-2021-44228 (Non-AI) — CVSS 10.0
- Defect 05: MOVEit Transfer CVE-2023-34362 (Non-AI) — Cl0p
- Defect 06: XZ Utils CVE-2024-3094 (Non-AI) — Andres Freund

Mỗi defect có trường "🔍 AI bias/hallucination" với: prompt gợi ý + chỗ cần soi + ô `[ ]` để điền output thật + ảnh. Kèm cảnh báo rõ: bạn phải tự chạy AI và điền output thật — không được để Claude viết hộ phần này.

**Output chính:** 6 defect mẫu markdown + bảng tổng hợp skeleton + Defects 07–20 placeholder

---

## Prompt #08 — Hoàn thiện đủ 20 defect

- **Thời gian:** [16:35] 04/06/2026
- **Tool:** Claude Sonnet 4.6 — claude.ai
- **Loại tác vụ:** Content generation (bulk)
- **Bloom-AI Level:** G9.5 (Create)

**Prompt gửi:**
> "rất tốt hoàn thiện đủ 20 lỗi cho tôi"

**Claude cung cấp:**
Claude tìm kiếm web xác minh: Mata v. Avianca ($5,000 / Judge Castel / 6 án lệ giả), Optus (9.8M), rồi sinh thêm 14 defect (Defects 07–20):

**Defects 07–11 (AI/LLM thêm):**
- 07: Mata v. Avianca (2023) — 6 án lệ giả, phạt $5,000, Judge P. Kevin Castel
- 08: Chevrolet Dealership Chatbot (2023) — prompt injection, "bán xe $1 ràng buộc pháp lý"
- 09: Replit AI Agent xóa DB SaaStr (2025) — agent mất kiểm soát
- 10: Google AI Overviews glue pizza (2024) — lấy nội dung châm biếm Reddit
- 11: Chicago Sun-Times/Philadelphia Inquirer sách ma (2025)

**Defects 12–20 (Non-AI thêm):**
- 12: CrowdStrike Falcon Outage (19/7/2024) — 8.5M thiết bị
- 13: Southwest Airlines meltdown (12/2022) — 16,700 chuyến hủy, phạt $140M
- 14: regreSSHion CVE-2024-6387 (2024) — Qualys, Linux/glibc
- 15: Optus Breach (2022) — ~9.8M, API không xác thực
- 16: Rogers Outage (8/7/2022) — ~12M người, lỗi config
- 17: LastPass Breach (2022) — vault backup, kỹ sư DevOps
- 18: Ivanti CVE-2023-46805 + CVE-2024-21887 (2024) — chained zero-days
- 19: Toyota Plant Halt (29/8/2023) — thiếu disk space, 14 nhà máy
- 20: Okta Support Breach (10/2023) — HAR files, session tokens

Bảng tổng hợp 20 dòng đầy đủ + tổng kết: 8/20 lỗi AI (≥5 ✔).

**Output chính:** 14 defect mới + bảng tổng hợp 20 dòng hoàn chỉnh

---

## Prompt #09 — Tìm link chính xác cho Defect 07

- **Thời gian:** [16:45] 04/06/2026
- **Tool:** Claude Sonnet 4.6 — claude.ai
- **Loại tác vụ:** Research / Source verification
- **Bloom-AI Level:** G9.1 (Understand — tìm nguồn đáng tin)

**Prompt gửi:**
> "giúp tôi tìm link bài viết chính xác cho defect 7"

**Claude cung cấp:**
Claude tìm kiếm và xác nhận 3 nguồn tốt nhất cho Mata v. Avianca:
1. **Primary source (tốt nhất):** `https://law.justia.com/cases/federal/district-courts/new-york/nysdce/1:2022cv01461/575368/54/` — phán quyết gốc của tòa, 22/06/2023.
2. **AI Incident Database #541:** `https://incidentdatabase.ai/cite/541/`
3. **Wikipedia:** `https://en.wikipedia.org/wiki/Mata_v._Avianca,_Inc.`

**Output chính:** 3 link nguồn xác minh + hướng dẫn dùng link nào làm primary source

---

## Prompt #10 — Hoàn thiện Defect 07 từ 2 link nguồn

- **Thời gian:** [16:55] 04/06/2026
- **Tool:** Claude Sonnet 4.6 — claude.ai
- **Loại tác vụ:** Content generation from fetched URLs
- **Bloom-AI Level:** G9.3 (Analyse — đọc văn bản pháp lý + phân tích)

**Prompt gửi:**
> "Hãy dựa vào 2 link bài viết đó hoàn thiện defect 07 giúp tôi"

**Claude cung cấp:**
Claude fetch cả 2 URL (Justia + AIID #541) và đọc toàn văn phán quyết, rồi sinh Defect 07 hoàn chỉnh 100% từ nguồn gốc:

**Các dữ kiện chính xác từ văn bản tòa:**
- Case: Roberto Mata v. Avianca, Inc., 22-cv-1461 (PKC), S.D.N.Y.
- 6 án lệ giả: Varghese, Shaboon, Petersen, Martinez, Durden, Miller
- Phán quyết: $5,000 USD (liên đới Schwartz + LoDuca + Levidow, Levidow & Oberman)
- Các luật sư "double down" hơn 2 tháng trước khi thừa nhận (25/05/2023)
- Bắt buộc gửi thư đính chính đến từng thẩm phán bị gán tên giả

**Trường AI hallucination:** prompt gợi ý "hỏi 4 câu về số án lệ/tên/mức phạt/thẩm phán" + chỉ rõ AI hay sai số lượng (7-9 thay vì 6) và thổi phồng mức phạt (10,000–50,000 thay vì 5,000).

**Output chính:** Block Defect 07 hoàn chỉnh với dữ kiện 100% từ nguồn gốc

---

## Prompt #11 — Upload report, rà R2, sửa bảng, hoàn thiện 20 AI Hallucination

- **Thời gian:** [17:15] 04/06/2026
- **Tool:** Claude Sonnet 4.6 — claude.ai
- **Loại tác vụ:** Review + Bulk content generation
- **Bloom-AI Level:** G9.4 (Evaluate) + G9.5 (Create)

**Prompt gửi:**
> *[Upload HW01_Report.md]*
> "tôi vừa thay đổi vài defect hãy sửa lại bảng tổng hợp và check xem còn sai thiếu gì không và hoàn thiện các phần AI Bias/Hallucination ở mỗi defect giúp tôi, có phần tôi đã làm AI Bias/Hallucination hãy từ đó hoàn thiện tất cả phần req 2 cho tôi"

**Claude cung cấp:**
Claude đọc toàn bộ file, phát hiện người dùng đã đổi nhiều defect (XZ→T-Mobile, regreSSHion→KakaoTalk, Rogers/LastPass/Ivanti→Okta/IHG/MGM, Okta→Toyota Cloud).

**Kết quả kiểm tra:**
- Lỗi nghiêm trọng: Defect 07 (Mata/Avianca) thiếu hẳn phần AI Hallucination.
- Bảng tổng hợp SAI HOÀN TOÀN — vẫn liệt kê defect cũ đã bị thay.
- 2 format lẫn lộn (template checkboxes vs prose).
- Rủi ro: Log4Shell công bố 12/2021, ngoài khung "2022–2026" của đề.
- Cần kiểm chứng: $40M MGM (thực tế ~$10M one-time + ~$100M Q3 impact).

Claude sinh file `R2_AI_Hallucination_blocks_and_table.md` gồm:
- 20 block AI Bias/Hallucination thống nhất prose format, giữ nguyên nội dung đã tốt (03/06/14/16/17/18/20), viết mới phần thiếu (01/02/04/05/07/08/09/10/11/12/13/15/19).
- Bảng tổng hợp 20 dòng đã cập nhật theo defect thật.
- Chú thích rõ: bạn vẫn phải chạy prompt thật + chụp màn hình.

**Output chính:** File `R2_AI_Hallucination_blocks_and_table.md`

---

## Prompt #12 — Chuyển sang Requirement 3

- **Thời gian:** [17:40] 04/06/2026
- **Tool:** Claude Sonnet 4.6 — claude.ai
- **Loại tác vụ:** Planning + Process guidance
- **Bloom-AI Level:** G9.1 (Understand)

**Prompt gửi:**
> "Chuyển sang Requirement 3"

**Claude cung cấp:**
Hướng dẫn toàn bộ R3 theo 6 bước + bảng điểm nội bộ (video 5pt, TC 12pt, edge case 6pt, defect 2pt):

1. **Bước 1 — Thiết bị + ảnh chống gian lận:** quy tắc chụp ảnh, khai báo serial.
2. **Bước 2 — 15 TC chiến lược:** phân bổ (happy path 5-6, boundary 3-4, negative 2-3, edge ≥3); template bảng 7 cột; quy trình đúng (AI sinh trước → screenshot → bạn thêm edge cases).
3. **Bước 3 — Edge case AI bỏ sót:** bảng 6 loại AI thường bỏ sót (mất điện đột ngột, nhiệt khắc nghiệt, bấm nhiều nút, điện áp VN, hành vi lạ, dùng lâu) + quy trình 3 bước (hỏi AI → chụp màn hình → giải thích ISTQB-based).
4. **Bước 4 — Thực thi + video:** ≤60s, giọng bạn, YouTube Unlisted.
5. **Bước 5 — GitHub Issues:** template issue + ảnh chụp Issues page.
6. **Bước 6 — Excel 3 sheet:** Test Cases / Checklist / Test Summary Report.

Kết thúc bằng câu hỏi: "Bạn đang dùng thiết bị nào?"

**Output chính:** Hướng dẫn R3 toàn diện + template bảng TC + template GitHub Issue

---

## Prompt #13 — Upload ảnh thiết bị (Senko L1638) + tạo phần khai báo

- **Thời gian:** [19:10] 04/06/2026
- **Tool:** Claude Sonnet 4.6 — claude.ai
- **Loại tác vụ:** Data extraction from image + Content generation
- **Bloom-AI Level:** G9.5 (Create — tổng hợp từ ảnh sang markdown)

**Prompt gửi:**
> *[Upload IMG_1422.jpeg (nhãn spec) + IMG_1423.jpeg (nhãn năng lượng)]*
> "Giúp tôi làm phần đầu req3 md : add device photo + declaration"

**Claude cung cấp:**
Claude đọc cả 2 nhãn từ ảnh và trích xuất đầy đủ thông tin:

**Thông số đọc được:**
- Nhãn năng lượng: Hãng TNHH Tân Tiến SENKO, Mã SP L1638, 47W, lưu lượng 64.4 m³/min, 5 sao TCVN 7827:2015.
- Nhãn spec: QUẠT LỜ, cánh 39cm, 220V/50Hz/47W, max 70°C, cấp E, QUACERT 0028-22, Lô SX 109, Tháng SX 09-2024, ISO 9001:2015, Thương hiệu Quốc gia, Bảo hành động cơ 24 tháng, TCVN 5699-2-80:2007.

**Cảnh báo:** 2 ảnh chỉ là nhãn — còn thiếu ảnh bắt buộc (thiết bị + thẻ SV cùng khung).

Sinh đoạn markdown phần khai báo với bảng thông số 12 dòng, link ảnh placeholder, ghi chú serial number (Lô SX: 1**XX**9 — thiết bị không in serial riêng).

**Output chính:** Block markdown khai báo thiết bị hoàn chỉnh

---

## Prompt #14 — Tạo 12 test case cho Quạt Lờ Senko L1638

- **Thời gian:** [19:25] 04/06/2026
- **Tool:** Claude Sonnet 4.6 — claude.ai
- **Loại tác vụ:** Test case design (AI-assisted)
- **Bloom-AI Level:** G9.3 (Analyse) + G9.5 (Create)

**Prompt gửi:**
> "tôi đã xong hãy tạo 12 testcase còn 3 testcase còn lại tôi sẽ tự làm"

**Claude cung cấp:**
Dựa vào thông số kỹ thuật thực tế (39cm, 120 nan, 3 tốc độ, 47W, 70°C max, cấp E), Claude sinh file `R3_TestCases_Senko_L1638.md` với 12 TC đầy đủ 7 cột:

| TC | Nhóm | Mô tả |
|----|------|-------|
| TC01 | Happy path | Khởi động Tốc 1 — kiểm tra cơ bản |
| TC02 | Happy path | Tốc 2 — luồng gió tăng hơn Tốc 1 |
| TC03 ⭐ | Happy path | Tốc 3 full load 47W — tờ giấy 1m + kiểm tra nhiệt |
| TC04 | Happy path | Chuyển tuần tự 1→2→3→Off |
| TC05 ⭐ | Boundary | Dừng đột ngột từ Tốc 3 — kiểm tra an toàn |
| TC06 ⭐ | Boundary | Chạy liên tục 30 phút — giới hạn nhiệt 70°C |
| TC07 | Boundary | Độ rung/cân bằng cánh 39cm ở Tốc 3 |
| TC08 ⭐ | Durability | Bật tắt 10 lần liên tiếp — độ bền công tắc |
| TC09 | Safety | Lồng bảo vệ 120 nan — kiểm tra tĩnh |
| TC10 | Stability | Tiếng ồn từng mức — phòng yên tĩnh |
| TC11 | Environment | Ổ nối dài 5m — so sánh với cắm trực tiếp |
| TC12 | Environment | Đặt sát tường 20cm — kiểm tra hiệu suất + nhiệt |

Kèm: bảng 5 TC ưu tiên quay video + gợi ý hướng 3 edge case bạn tự làm (mất điện đột ngột, điện áp thấp, vật cản phía trước, bật ngay sau tắt <5s, HCMC 35°C+ẩm cao).

**Output chính:** File `R3_TestCases_Senko_L1638.md`

---

## Prompt #15 — Tạo khung các phần còn lại của Requirement 3

- **Thời gian:** [22:15] 04/06/2026
- **Tool:** Claude Sonnet 4.6 — claude.ai
- **Loại tác vụ:** Template/Framework generation
- **Bloom-AI Level:** G9.5 (Create)

**Prompt gửi:**
> "Hãy viết khung những phần còn lại của req3 để tôi bỏ vào hoàn thiện luôn phần req3 này"

**Claude cung cấp:**
Sinh file `R3_Framework_Remaining.md` với 5 section hoàn chỉnh:

**Section 3.3 — Edge Cases AI Bỏ Sót:**
- Template 3 slot EC01/EC02/EC03.
- Mỗi slot: prompt đã hỏi AI + link ảnh hội thoại + bảng mô tả TC + giải thích tại sao AI bỏ sót (trích ISTQB "experience-based testing").

**Section 3.4 — Kết Quả Thực Thi + Video:**
- Bảng 5 dòng (TC01/03/04/06/08) với cột: Actual · Verdict · Link YouTube Unlisted · Defect?
- Bảng thống kê nhanh (pass/fail/blocked/defect count).

**Section 3.5 — Defect Log GitHub Issues:**
- Bảng 5+ dòng: DFT-# · TC · Tiêu đề · Severity · GitHub link · Status.
- Template tạo GitHub Issue chuẩn (Steps/Expected/Actual/Severity/Video/Ảnh).

**Section 3.6 — Test Summary Report:**
- Bảng 15 trường (thiết bị, ngày, người thực hiện, TC stats, defect stats, video count, edge case count).
- Ô kết luận kiểm thử.

**Section 4 — QA/QC Role Mindmap + 3 Mistakes (G9.1):**
- Placeholder ảnh mindmap AI sinh.
- Template bảng 3 lỗi (vị trí · AI viết · Lý do sai · Đúng phải là · Nguồn đối chiếu ISTQB).

**Checklist hoàn thiện R3:** 15 mục chia 3 giai đoạn (trước/trong/sau thực thi).

**Output chính:** File `R3_Framework_Remaining.md`

---

## Prompt #16 — Export toàn bộ cuộc trò chuyện ra Markdown

- **Thời gian:** [23:10] 04/06/2026
- **Tool:** Claude Sonnet 4.6 — claude.ai
- **Loại tác vụ:** Documentation / Log export
- **Bloom-AI Level:** G9.4 (Evaluate — tự nhìn lại quá trình sử dụng AI)

**Prompt gửi:**
> "nãy giờ trao đổi gì thì export hết ra Markdown, đừng compact nhiều quá. Trên tinh thần là có dùng thì có log lại, một là để minh chứng, hai là để qua thời gian, mình dùng log đó để đánh giá mức độ thành thạo sử dụng AI của mình."

**Claude cung cấp:**
File này — toàn bộ 16 lượt trao đổi được ghi lại đầy đủ theo format: thời gian · tool · loại tác vụ · Bloom-AI level · prompt gửi · nội dung Claude cung cấp (không tóm tắt quá mức) · output chính.

**Output chính:** File `Appendix_A_Prompt_Log.md` (file này)

---

## Tổng kết sử dụng AI — HW01

| Chỉ số | Giá trị |
|--------|---------|
| Tổng số prompt | 16 |
| Thời gian session | 04/06/2026 |
| AI Tool | Claude Sonnet 4.6 (claude.ai) |
| Loại tác vụ chủ yếu | Content generation, Review, Research guidance |
| Bloom-AI level cao nhất đạt | G9.5 (Create) |

### Phân bổ tác vụ AI

| Loại tác vụ | Số prompt | Ví dụ |
|-------------|-----------|-------|
| Content generation | 7 | TC, defect entries, job blocks, framework |
| Review / QA | 2 | Rà soát R1, R2 |
| Planning / Guidance | 3 | Lộ trình, R2 guidance, R3 guidance |
| Research / Source verification | 2 | Link defect, xác minh số liệu |
| Data extraction from image | 1 | Đọc nhãn thiết bị |
| Documentation export | 1 | File này |

### Tự đánh giá mức độ thành thạo AI

| Tiêu chí | Nhận xét |
|----------|----------|
| **Prompt rõ ràng** | Phần lớn prompt ngắn gọn nhưng context đủ (upload file kèm câu hỏi cụ thể). |
| **Biết khi nào dùng AI** | Dùng AI cho drafting, review, research; tự làm phần anti-cheat (ảnh, video, edge cases). |
| **Biết khi nào KHÔNG dùng AI** | Hiểu 4 artifact cấm AI; tự thiết kế TC13-15 edge case. |
| **Kiểm chứng output AI** | Nhờ Claude xác minh số liệu trước khi dùng (Air Canada, Optus, Avianca). |
| **Iteration / Follow-up** | Biết upload lại file để Claude review và sửa (R1 check, R2 bulk fix). |
| **Điểm cần cải thiện** | Nên đặt prompt chi tiết hơn từ đầu (vd ghi rõ device model khi hỏi TC) để giảm lượt trao đổi. |

# Prompt Log ChatGPT

## [15:00]

đây là form câu 1 của tôi hãy từ đó giúp tôi làm các phần sau:

## REQUIREMENT 1: QA/QC Job Market 2026+

---

## [09:20 04/06/2026]

đây là job 2 tôi kiếm được hãy làm giúp tôi để tôi copy bỏ vào file .md:
https://itviec.com/viec-lam-it/automation-qa-engineer-qa-qc-tester-automation-test-nakivo-0115

---

## [09:25 04/06/2026]

rất tốt tương tự cho
https://itviec.com/viec-lam-it/qc-engineer-tester-qa-qc-for-web-up-to-1500-evolus-planv-5225

---

## [09:30 04/06/2026]

tương tự:
https://itviec.com/viec-lam-it/automation-tester-qa-qc-mercatus-4125

---

## [09:35 04/06/2026]

tương tự cho:
https://itviec.com/viec-lam-it/automation-tester-qa-qc-abbank-0039

---

## [09:40 04/06/2026]

giúp tôi tạo cho:
https://itviec.com/viec-lam-it/product-tester-qa-qc-jira-trello-cong-ty-tnhh-teenup-1256

---

## [ 09:45 04/06/2026]

https://itviec.com/viec-lam-it/manual-automation-tester-quality-analyst-qa-qc-mitek-vietnam-0005

---

## [09:50 04/06/2026]

https://itviec.com/viec-lam-it/tester-sub-leader-tieng-nhat-n2-dts-software-vietnam-4240

---

## [09:55 04/06/2026]

https://itviec.com/viec-lam-it/chuyen-vien-qc-phan-mem-qc-executive-kingfoodmart-0249

---

## [10:00 04/06/2026]

https://itviec.com/it-jobs/process-quality-assurance-qa-qc-agile-scrum-jira-sabitech-cong-ty-co-phan-cong-nghe-sabi-1415

---

## [15:50 04/06/2026]

giúp tôi tạo file .md trình bày phần req2 cho 20 lỗi này

---

## [16:10 04/06/2026]

trong đoạn sau hãy giúp tôi tìm AI bias/hallucination

---

## [16:15 04/06/2026]

trong đoạn này có bị hallucination không

---

## [16:30 04/06/2026]

Hãy đọc tham khảo phần này và giúp tôi thay đổi nội dung req2 dưới đây lựa chọn và đổi lại cho tôi các mục 4,5,6,7,14,16,17,18,20 và phần thay thế viết tiếng việt

---

## [16:35 04/06/2026]

chuyển các phần thay thế thành dưới dạng .md để tôi copy bỏ vào

---

## [23:10 04/06/2026]

Tham khảo câu trả lời dưới đây giúp tôi làm "G9.1 Ask AI Tool for ISTQB mindmap and correct it"

---

## [23:15 04/06/2026]

fix lại diagram vì sao lại không hoạt động và viết bằng tiếng việt cho tôi

---

## [23:25 04/06/2026]

nãy giờ trao đổi gì thì export hết ra Markdown, đừng compact nhiều quá.

---

## [23:30 04/06/2026]

ở đây k cần giải thích chỉ liệt kê ra mỗi lần tôi prompt hỏi thôi không cần giải thích nhiều:
Prompt log .md with timestamps for every AI prompt you sent.

---

## [23:35 04/06/2026]

Hãy để timestamp đúng với những gì tôi hỏi theo thứ tự từ trên xuống dưới và prompt tôi ghi thế nào để thế ấy

---

## [23:40 04/06/2026]

export chat md
