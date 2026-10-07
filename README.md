# Lab 21 — Phân tích rủi ro AI qua case study thực tế

- Họ và tên: Thân Thị Kim Chi
- MSSV / mã học viên: 2A202602797
- Lớp: Track 1
- Ngành đã chọn: Tuyển dụng & Quản trị Nhân sự (HR Tech & Talent Acquisition)

---

### 1. Industry Risk Snapshot

| Nội dung | Đánh giá của tôi và lý do |
| --- | --- |
| Những tác hại chính có thể xảy ra | **Bất bình đẳng và tước đoạt cơ hội việc làm/sinh kế có hệ thống.**<br>Ứng viên bị tước mất cơ hội nghề nghiệp mà không được giải trình minh bạch; củng cố các định kiến xã hội đối với phụ nữ, người da màu, người lớn tuổi và người khuyết tật. Về phía doanh nghiệp, việc phân loại sai khiến họ bỏ lỡ nhân tài và đối mặt với rủi ro pháp lý/kiện tụng nghiêm trọng. |
| Mức độ high-stakes | **Cao (High-Stakes Category theo Phân loại của EU AI Act).**<br>Việc làm và thu nhập quyết định trực tiếp tới sinh kế, an sinh xã hội và phẩm giá con người. Một quyết định tự động loại hồ sơ ở quy mô lớn có thể loại trừ vĩnh viễn một nhóm người khỏi thị trường lao động mà họ không có quyền khiếu nại. |
| Dữ liệu nhạy cảm có thể được sử dụng | **Dữ liệu nhân thân & thuộc tính được bảo vệ (Protected Attributes):**<br>- Thông tin cá nhân (PII): Họ tên, địa chỉ, tuổi tác, giới tính, trường học.<br>- Dữ liệu sinh trắc học & phi ngôn ngữ: Video phỏng vấn ghi nhận biểu cảm cơ mặt (micro-expressions), cao độ giọng nói, ngữ điệu.<br>- Dữ liệu sức khỏe/khuyết tật: Lịch sử y tế, tình trạng khuyết tật thần kinh/vận động. *(Bài làm không sử dụng dữ liệu thật của cá nhân).* |
| Nhu cầu human review | **Cao (Bắt buộc phải có Human-in-the-loop ở khâu quyết định cuối cùng).**<br>Chuyên viên tuyển dụng (HR Recruiter) phải kiểm tra danh sách ứng viên trước khi gửi thư từ chối; AI chỉ được đóng vai trò hỗ trợ gợi ý (decision-support). Cần kiểm toán định kỳ tỷ lệ ứng viên bị loại theo nhóm nhân khẩu học để phát hiện thiên kiến kịp thời. |

---

### 2. Case study 1 — Amazon AI Recruitment Tool (2014 – 2018)

#### Brief Case
- Tổ chức / sản phẩm AI: Amazon / Công cụ máy học tự động sàng lọc và xếp hạng hồ sơ ứng viên (Automated Applicant Screening Tool).
- Thời gian, địa điểm / bối cảnh: Giai đoạn 2014 – 2017 tại Amazon (Mỹ và Anh); được Reuters phanh phui và chính thức giải tán vào năm 2018.
- AI được dùng để làm gì: Tự động chấm điểm CV của ứng viên trên thang từ 1 đến 5 sao nhằm chọn ra top 5 ứng viên tiềm năng nhất cho các vị trí kỹ sư phần mềm.
- Vấn đề hoặc sự kiện đáng chú ý: Thuật toán tự học từ dữ liệu tuyển dụng 10 năm trước của ngành công nghệ (vốn do nam giới áp đảo), từ đó tự hình thành quy tắc phạt điểm các CV có chứa từ *"women's"* (như *"women's chess club"*) và hạ điểm sinh viên tốt nghiệp các trường nữ sinh.
- Số liệu có nguồn:
  - Sử dụng dữ liệu huấn luyện gồm hồ sơ tuyển dụng nộp vào Amazon trong **10 năm** (2004–2014).
  - Đội ngũ kỹ sư đã thử nghiệm khoảng **500 mô hình máy học** trên hàng ngàn vị trí công việc.
  - Amazon đã chính thức **giải tán nhóm dự án vào đầu năm 2018** sau khi nhận thấy không thể loại bỏ triệt để thiên kiến giới tính trong thuật toán.
- Nguồn: Bài báo điều tra độc quyền: *"Amazon scraps secret AI recruiting tool that showed bias against women"* — Tác giả: Jeffrey Dastin — Đơn vị: Reuters — Ngày công bố: 10/10/2018 — URL: https://www.reuters.com/article/us-amazon-com-jobs-automation-insight-idUSKCN1MK08G
- Phân biệt bằng chứng và nhận định:
  - *Điều nguồn xác nhận (Bằng chứng):* Amazon đã phát triển công cụ này từ năm 2014, mô hình tự động phạt điểm hồ sơ có từ khóa của nữ giới, và dự án đã bị hủy bỏ vì lo ngại phân biệt đối xử.
  - *Điều tôi suy luận (Nhận định):* Dù Amazon tuyên bố công cụ chưa từng được dùng độc lập để ra quyết định tuyển dụng chính thức, việc thử nghiệm nội bộ có thể đã tạo ra sự thiên vị vô thức cho các chuyên viên nhân sự tiếp cận kết quả chấm điểm.

#### Harm Map Worksheet
| Trường | Phân tích của tôi |
| --- | --- |
| High-risk moment | Giai đoạn sàng lọc hồ sơ ban đầu (Pre-screening) — AI tự động chấm điểm và xếp hạng từ 1 đến 5 sao trước khi hồ sơ đến tay nhà tuyển dụng. |
| Stakeholder bị ảnh hưởng | Ứng viên nữ nộp đơn vào vị trí kỹ sư phần mềm; đội ngũ tuyển dụng Amazon; uy tín thương hiệu của Amazon về đa dạng và hòa nhập (DEI). |
| Failure mode | Historical Bias & Algorithmic Gender Discrimination (Thiên kiến lịch sử và phân biệt đối xử theo giới tính). |
| Layer bắt đầu lỗi | **Model Layer & Data Layer** (Dữ liệu huấn luyện lịch sử mất cân đối nghiêm trọng; hàm mục tiêu tối ưu sao chép mẫu tuyển dụng quá khứ). |
| Harm xảy ra là gì? | - *Đã xảy ra:* Lãng phí tài nguyên công nghệ; tổn hại danh tiếng doanh nghiệp khi sự việc bị phanh phui trước công chúng.<br>- *Nguy cơ được ngăn chặn:* Hàng ngàn ứng viên nữ có nguy cơ bị loại bỏ bất công ở vòng sơ tuyển nếu hệ thống được triển khai trên quy mô lớn. |
| Harm lens | Representational Harm (Tác hại định kiến đại diện) & Allocative Harm (Tác hại phân bổ cơ hội kinh tế). |
| Severity | **High** (Tác động trực tiếp đến bình đẳng giới và cơ hội việc làm tại tập đoàn công nghệ lớn nhất thế giới). |
| Scale | **Medium to Large** (Hàng ngàn hồ sơ ứng tuyển kỹ thuật mỗi đợt; 500 mô hình được thử nghiệm; phạm vi toàn cầu của Amazon). |
| Probability | **Certain** (Đã xảy ra trong môi trường thử nghiệm nội bộ của Amazon). |
| Frequency | **High** (Xuất hiện liên tục mỗi khi CV của ứng viên nữ có chứa các từ khóa đặc thù giới tính đi qua bộ lọc). |
| Vì sao? | Đánh giá dựa trên báo cáo điều tra độc quyền của Reuters với lời xác nhận của các cựu kỹ sư Amazon; nguyên nhân cốt lõi là máy học sao chép cơ học sự bất bình đẳng giới vốn có trong lịch sử ngành công nghệ. |

---

### 3. Case study 2 — HireVue AI Facial & Speech Video Analysis (2019 – 2021)

#### Brief Case
- Tổ chức / sản phẩm AI: HireVue / Nền tảng phỏng vấn video tích hợp AI chấm điểm năng lực ứng viên (Assessments AI).
- Thời gian, địa điểm / bối cảnh: Giai đoạn 2014 – 2021 tại Mỹ và toàn cầu; phục vụ hơn 700 khách hàng doanh nghiệp lớn (như Unilever, Hilton, Goldman Sachs).
- AI được dùng để làm gì: Phân tích biểu cảm cơ mặt (micro-expressions), cao độ giọng nói, ngữ điệu và từ vựng của ứng viên qua webcam khi trả lời câu hỏi tự động, từ đó xuất ra điểm số "khả năng làm việc" (employability score).
- Vấn đề hoặc sự kiện đáng chú ý: Hệ thống bị giới khoa học và tổ chức nhân quyền chỉ trích là "ngụy khoa học" (pseudoscience). Thuật toán phân biệt đối xử với ứng viên có biểu cảm khuôn mặt khác biệt, người mắc chứng tự kỷ, người bị liệt mặt, hoặc người nói tiếng Anh không mang giọng chuẩn bản xứ.
- Số liệu có nguồn:
  - Hơn **1 triệu cuộc phỏng vấn AI** được thực hiện trên toàn cầu mỗi năm.
  - Tháng 11/2019, Tổ chức EPIC đã nộp đơn khiếu nại chính thức dài **34 trang** lên FTC cáo buộc vi phạm Mục 5 Đạo luật FTC (hành vi thương mại gian lận và không công bằng).
  - Đầu năm 2021, sau cuộc kiểm toán thuật toán độc lập của công ty tư vấn ORCAA, HireVue đã chính thức **loại bỏ hoàn toàn tính năng phân tích khuôn mặt (facial analysis)** khỏi sản phẩm.
- Nguồn:
  - Đơn khiếu nại pháp lý: *EPIC Complaint to the Federal Trade Commission in the Matter of HireVue, Inc.* — Đơn vị: Electronic Privacy Information Center (EPIC) — Ngày nộp: 06/11/2019 — URL: https://epic.org/documents/in-the-matter-of-hirevue-inc/
  - Báo cáo kiểm toán: *"A popular algorithm used to screen job applicants was tested for bias. The results weren’t pretty"* — Tác giả: Drew Harwell — Báo: The Washington Post — Ngày: 25/02/2021 — URL: https://www.washingtonpost.com/technology/2021/02/25/hirevue-facial-analysis-screening/
- Phân biệt bằng chứng và nhận định:
  - *Điều nguồn xác nhận (Bằng chứng):* EPIC đã gửi đơn khiếu nại chính thức lên FTC; HireVue đã công khai tuyên bố gỡ bỏ tính năng phân tích khuôn mặt từ năm 2021 sau báo cáo kiểm toán của ORCAA.
  - *Điều tôi suy luận (Nhận định):* Dù HireVue khẳng định thuật toán đánh giá đa chiều, việc gán ghép chuyển động cơ mặt với năng lực trí tuệ là thiếu cơ sở khoa học, gây tổn hại nặng nề đến người khuyết tật.

#### Harm Map Worksheet
| Trường | Phân tích của tôi |
| --- | --- |
| High-risk moment | Giai đoạn phỏng vấn video sơ loại bất đồng bộ (Asynchronous Video Interview) — AI chấm điểm khuôn mặt và giọng nói để quyết định ứng viên nào được vào vòng tiếp theo. |
| Stakeholder bị ảnh hưởng | Ứng viên xin việc (đặc biệt là người khuyết tật cơ mặt, người tự kỷ, người thiểu số nói tiếng Anh không chuẩn giọng bản xứ); các doanh nghiệp khách hàng của HireVue. |
| Failure mode | Lack of Grounding & Discrimination Against Disabilities / Minorities (Thiếu cơ sở khoa học xác thực và phân biệt đối xử với người khuyết tật/thiểu số). |
| Layer bắt đầu lỗi | **Grounding Layer & UX/Product Design Layer** (Khoa học nền tảng sai lầm khi coi biểu cảm khuôn mặt phản ánh năng lực chuyên môn; thiết kế tương tác thiếu khả năng tiếp cận). |
| Harm xảy ra là gì? | - *Đã xảy ra:* Hàng ngàn ứng viên bị đánh giá thấp một cách bất công mà không rõ lý do; gây căng thẳng tâm lý tột độ cho người tìm việc; khiếu nại pháp lý lên FTC.<br>- *Nguy cơ:* Bình thường hóa việc sử dụng "công nghệ nhận diện cảm xúc" vô căn cứ tại nơi làm việc. |
| Harm lens | Psychological Harm (Tổn thương tâm lý) & Allocative Harm (Tác hại phân bổ cơ hội) & Accessibility Discrimination. |
| Severity | **High** (Xâm phạm dữ liệu sinh trắc học cá nhân và tước đoạt cơ hội của nhóm người yếu thế/khuyết tật). |
| Scale | **Large** (Hơn 1 triệu cuộc phỏng vấn mỗi năm tại hàng trăm tập đoàn đa quốc gia). |
| Probability | **Certain** (Đã xảy ra và dẫn đến hành động pháp lý của EPIC cùng quyết định loại bỏ tính năng từ phía HireVue). |
| Frequency | **Continuous** (Diễn ra liên tục trên mọi phiên phỏng vấn sử dụng tính năng phân tích nét mặt trước năm 2021). |
| Vì sao? | Đánh giá dựa trên văn bản khiếu nại chính thức của EPIC gửi FTC và cuộc kiểm toán độc lập của chuyên gia toán học Cathy O'Neil (ORCAA) được Washington Post đưa tin. |

---

### 4. Case study 3 — Workday AI Screening Discrimination Lawsuit (2023 – 2024)

#### Brief Case
- Tổ chức / sản phẩm AI: Workday, Inc. / Bộ công cụ AI sàng lọc và tuyển dụng ứng viên trên nền tảng đám mây Workday Human Capital Management (HCM).
- Thời gian, địa điểm / bối cảnh: Giai đoạn 2023 – 2024 tại Tòa án Liên bang Quận Bắc California (Mỹ). Vụ kiện tập thể tiêu biểu về phân biệt đối xử thuật toán.
- AI được dùng để làm gì: Tự động phân loại, lọc và đề xuất ứng viên đạt tiêu chuẩn từ hàng triệu hồ sơ xin việc của các khách hàng doanh nghiệp thuộc nhóm Fortune 500.
- Vấn đề hoặc sự kiện đáng chú ý: Hệ thống bị cáo buộc tạo ra tác động sai lệch có tính hệ thống (disparate impact), tự động từ chối hồ sơ của các ứng viên là người da màu, người trên 40 tuổi và người có tiền sử khuyết tật dù họ đáp ứng đầy đủ yêu cầu chuyên môn.
- Số liệu có nguồn:
  - Nguyên đơn Derek Mobley (ứng viên da màu, trên 40 tuổi, mắc chứng lo âu/trầm cảm) đã nộp đơn ứng tuyển vào **hơn 100 vị trí** tại các công ty dùng Workday (như HP, AT&T, Comcast) và bị hệ thống tự động từ chối trong thời gian cực ngắn (thường vào ban đêm sau vài giờ nộp đơn).
  - Workday phục vụ hơn **65 triệu người dùng** và hơn **50% doanh nghiệp thuộc danh sách Fortune 500**.
  - Tháng 7/2024, Thẩm phán Liên bang Rita Lin đã ra **phán quyết bác bỏ yêu cầu hủy vụ kiện của Workday**, xác lập tiền lệ pháp lý: Nhà cung cấp phần mềm AI tuyển dụng có thể bị kiện như một "Đại lý tuyển dụng" (Employment Agency) theo Đạo luật Dân quyền Mỹ (Title VII, ADEA, ADA).
- Nguồn:
  - Văn bản phán quyết tòa án: *Mobley v. Workday, Inc., Case No. 23-cv-00770-RFL (Order Denying Motion to Dismiss)* — Tòa án Liên bang Quận Bắc California — Ngày: 12/07/2024 — URL: https://law.justia.com/cases/federal/district-courts/california/candce/3:2023cv00770/408892/103/
  - Báo chí pháp lý: *"Workday Must Face Lawsuit Over AI Bias in Hiring, Judge Rules"* — Báo: Bloomberg Law — Ngày: 15/07/2024 — URL: https://news.bloomberglaw.com/daily-labor-report/workday-must-face-lawsuit-over-ai-bias-in-hiring-judge-rules
- Phân biệt bằng chứng và nhận định:
  - *Điều nguồn xác nhận (Bằng chứng):* Đơn kiện tập thể đã được Tòa án Liên bang thụ lý và Thẩm phán bác bỏ yêu cầu đình chỉ của Workday, xác lập cơ sở pháp lý về trách nhiệm của bên phát triển AI.
  - *Điều tôi suy luận (Nhận định):* Dù Workday phủ nhận hành vi sai trái và vụ kiện đang trong giai đoạn cung cấp chứng cứ (discovery), tần suất từ chối tự động hàng loạt cho thấy khả năng cao mô hình sử dụng các biến số gián tiếp (như năm tốt nghiệp đại học) để suy luận độ tuổi của ứng viên.

#### Harm Map Worksheet
| Trường | Phân tích của tôi |
| --- | --- |
| High-risk moment | Giai đoạn tự động lọc và loại hồ sơ (Automated Rejection) ở quy mô hàng loạt mà không có sự kiểm tra thực tế của nhân sự con người. |
| Stakeholder bị ảnh hưởng | Hàng triệu người tìm việc là người da màu, lao động lớn tuổi (trên 40 tuổi), người khuyết tật; các tập đoàn sử dụng Workday; uy tín của Workday. |
| Failure mode | Systemic Disparate Impact & Age/Race/Disability Discrimination (Tác động sai lệch hệ thống và phân biệt đối xử theo tuổi tác/chủng tộc/khuyết tật). |
| Layer bắt đầu lỗi | **Model Layer & Safety/Governance Layer** (Thiếu rào chắn kiểm toán thiên kiến độc lập và thiếu cơ chế bảo đảm tuân thủ luật chống phân biệt đối xử). |
| Harm xảy ra là gì? | - *Đã xảy ra:* Ứng viên bị tước quyền tiếp cận việc làm hàng loạt; rủi ro pháp lý và chi phí kiện tụng tập thể khổng lồ cho Workday; tiền lệ pháp lý mở rộng trách nhiệm của AI vendor.<br>- *Nguy cơ:* Đào thải một thế hệ lao động lớn tuổi và người yếu thế ra khỏi thị trường việc làm hiện đại. |
| Harm lens | Economic/Allocative Harm (Tác hại phân bổ cơ hội kinh tế) & Legal Harm & Systematic Social Exclusion. |
| Severity | **Critical** (Ảnh hưởng ở quy mô hàng chục triệu người lao động và hàng trăm tập đoàn lớn nhất thế giới). |
| Scale | **Very Large (Doanh nghiệp toàn cầu)** (Hơn 65 triệu người dùng và hơn 50% doanh nghiệp Fortune 500 chịu ảnh hưởng từ nền tảng Workday). |
| Probability | **High** (Căn cứ vào quyết định thụ lý của Tòa án Liên bang xác nhận các cáo buộc ban đầu có đầy đủ cơ sở pháp lý). |
| Frequency | **Continuous** (Diễn ra hàng ngày trên mọi quy trình tuyển dụng tự động của các công ty khách hàng Workday). |
| Vì sao? | Đánh giá dựa trên phán quyết chính thức của Thẩm phán Liên bang Rita Lin và hồ sơ tòa án công khai; tính chất tập trung hóa của các nền tảng đám mây khiến rủi ro phân biệt đối xử nhân rộng theo cấp số nhân. |
