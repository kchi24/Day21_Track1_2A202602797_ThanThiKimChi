# BÁO CÁO LAB DAY 21 — TRACK 1: AI ETHICS, AI SAFETY & RESPONSIBLE AI

* **Học viên:** Thân Thị Kim Chi
* **Mã số học viên (MSSV):** 2A202602797
* **Tên Repository:** `DAY21_Track1_2A202602797_ThanThiKimChi`
* **Ngành được chọn:** Tuyển dụng & Quản trị Nhân sự (HR Tech & Talent Acquisition)

---

## PHẦN 1: INDUSTRY RISK SNAPSHOT

| Tiêu chí | Đánh giá & Phân tích chi tiết |
| :--- | :--- |
| **Ngành được chọn** | **Tuyển dụng & Quản trị Nhân sự (HR Tech & Talent Acquisition)** |
| **Tác hại chính (Primary Harm)** | **Bất bình đẳng và tước đoạt cơ hội việc làm/sinh kế có hệ thống.**<br>Khi hệ thống AI mắc lỗi thiên kiến hoặc phân loại sai, ứng viên bị tước bỏ cơ hội tiếp cận việc làm mà không hề hay biết; đồng thời doanh nghiệp mất đi nhân tài và củng cố thêm các định kiến phân biệt đối xử trong xã hội (giới tính, chủng tộc, độ tuổi, khuyết tật). |
| **Mức độ High-stakes** | **RẤT CAO (High-Stakes Category theo EU AI Act).**<br>Việc làm quyết định trực tiếp đến thu nhập, an sinh xã hội, sự phát triển cá nhân và bình đẳng kinh tế. Một quyết định sa thải hoặc từ chối hồ sơ tự động ở quy mô lớn có thể hủy hoại lộ trình nghề nghiệp của hàng ngàn con người mà không có cơ chế khiếu nại minh bạch. |
| **Dữ liệu nhạy cảm (Sensitive Data)** | 1. **Dữ liệu nhân thân & PII:** Họ tên, ngày sinh, địa chỉ, số điện thoại, tình trạng hôn nhân.<br>2. **Dữ liệu nhân khẩu học & thuộc tính được bảo vệ (Protected Attributes):** Giới tính, chủng tộc/sắc tộc, quốc tịch, tôn giáo, xu hướng tính dục.<br>3. **Dữ liệu sinh trắc học & phi ngôn ngữ:** Video phỏng vấn ghi nhận biểu cảm khuôn mặt (facial micro-expressions), cao độ giọng nói, ngữ điệu, cử chỉ mắt.<br>4. **Dữ liệu y tế/sức khỏe:** Tình trạng khuyết tật (khuyết tật vận động, thần kinh, giọng nói). |
| **Nhu cầu Human-in-the-loop (HITL)** | **BẮT BUỘC Ở KHÂU QUYẾT ĐỊNH CUỐI CÙNG (Decision Stage).**<br>- AI chỉ được đóng vai trò là công cụ hỗ trợ gợi ý (Decision-support system), tuyệt đối không để AI tự động loại bỏ (Auto-rejection) mà không có sự kiểm tra của con người.<br>- Chuyên viên tuyển dụng (HR Recruiter) phải kiểm toán định kỳ danh sách ứng viên bị AI đánh giá thấp để phát hiện mẫu sai lệch (bias patterns).<br>- Phải có cơ chế giải trình (Explainability) và cổng khiếu nại dành cho ứng viên nếu nghi ngờ bị thuật toán đối xử bất công. |

---

## PHẦN 2: BRIEF CASE (3 CASE STUDY AI CÓ THẬT)

### 📌 Case Study 1: Amazon AI Recruitment Tool (2014 – 2018)
* **Hệ thống AI:** Công cụ tự động sàng lọc và xếp hạng CV ứng viên bằng Machine Learning.
* **Đơn vị phát triển/triển khai:** Amazon (Nhóm kỹ sư máy học tại văn phòng Edinburgh, Scotland).
* **Mục đích sử dụng:** Tự động hóa quá trình đánh giá hàng trăm ngàn CV nộp vào Amazon, chấm điểm từ 1 đến 5 sao để tìm ra các lập trình viên và kỹ sư phần mềm xuất sắc nhất.
* **Sự cố thực tế:** Thuật toán tự học trên tập dữ liệu hồ sơ tuyển dụng trong vòng 10 năm trước đó của ngành công nghệ (vốn do nam giới áp đảo). Kết quả là AI tự hình thành quy tắc phạt điểm và hạ bậc bất kỳ CV nào có chứa từ *"women's"* (ví dụ: *"women's chess club captain"*) và hạ thấp điểm của sinh viên tốt nghiệp từ hai trường đại học nữ sinh.
* **Số liệu cụ thể:** Nhóm dự án phát hiện hệ thống phân biệt đối xử với ứng viên nữ ngay cả khi đã cố gắng loại bỏ biến số giới tính trực tiếp. Đến năm 2017, ban lãnh đạo Amazon nhận thấy không thể khắc phục triệt để tính thiên lệch của thuật toán và đã chính thức giải tán dự án vào đầu năm 2018 mà không đưa vào sản xuất đại trà.
* **Nguồn kiểm chứng:** Điều tra độc quyền của hãng thông tấn **Reuters** bởi nhà báo Jeffrey Dastin: *"Amazon scraps secret AI recruiting tool that showed bias against women"* (Xuất bản ngày 10/10/2018).

---

### 📌 Case Study 2: HireVue AI Facial & Speech Analysis Video Interview (2019 – 2021)
* **Hệ thống AI:** Nền tảng phỏng vấn video tích hợp AI tự động chấm điểm độ phù hợp của ứng viên (Employability score) qua nhận diện khuôn mặt và xử lý ngôn ngữ tự nhiên.
* **Đơn vị phát triển/triển khai:** HireVue (được hàng trăm tập đoàn toàn cầu như Hilton, Unilever, Goldman Sachs sử dụng).
* **Mục đích sử dụng:** Cho phép ứng viên ghi hình câu trả lời video, sau đó AI phân tích biểu cảm vi mô (micro-expressions), chuyển động cơ mặt, ngữ điệu giọng nói và lựa chọn từ ngữ để xếp hạng ứng viên.
* **Sự cố thực tế:** Hệ thống bị các nhà khoa học máy tính và tổ chức nhân quyền chỉ trích là "khoa học giả tưởng nguy hiểm" (pseudoscience). Thuật toán gây bất lợi nghiêm trọng cho những người có biểu cảm khuôn mặt khác biệt, người mắc chứng tự kỷ, người bị liệt mặt, hoặc người nói tiếng Anh không phải tiếng mẹ đẻ.
* **Số liệu cụ thể:** Tháng 11/2019, Tổ chức Trung tâm Thông tin Quyền riêng tư Điện tử (**EPIC**) đã nộp đơn khiếu nại chính thức lên Ủy ban Thương mại Liên bang Mỹ (**FTC**), cáo buộc HireVue thực hiện hành vi thương mại gian lận và không công bằng. Sau cuộc kiểm toán thuật toán độc lập của công ty tư vấn ORCAA (do nhà toán học Cathy O'Neil dẫn dắt), HireVue đã buộc phải **tuyên bố loại bỏ hoàn toàn tính năng phân tích khuôn mặt (facial analysis)** vào đầu năm 2021.
* **Nguồn kiểm chứng:** 
  1. Đơn khiếu nại FTC của EPIC: *EPIC v. HireVue Complaint (FTC Matter No. 2020)*.
  2. Báo cáo kiểm toán độc lập ORCAA / Tạp chí *Washington Post*: *"A popular algorithm used to screen job applicants was tested for bias. The results weren’t pretty"* (2021).

---

### 📌 Case Study 3: Vụ kiện Phân biệt đối xử Thuật toán Workday — Mobley v. Workday, Inc. (2023 – 2024)
* **Hệ thống AI:** Bộ công cụ sàng lọc và tuyển dụng ứng viên bằng AI tích hợp trên nền tảng đám mây Workday HCM.
* **Đơn vị phát triển/triển khai:** Workday, Inc. (phục vụ hơn 60 triệu người dùng và đa số các doanh nghiệp Fortune 500).
* **Mục đích sử dụng:** Tự động phân loại, lọc và đề xuất ứng viên đạt tiêu chuẩn từ hàng triệu hồ sơ xin việc của các khách hàng doanh nghiệp.
* **Sự cố thực tế:** Thuật toán của Workday bị cáo buộc tạo ra tác động sai lệch có tính hệ thống (disparate impact), tự động loại trừ các ứng viên là người da màu, người trên 40 tuổi và người khuyết tật dù họ đáp ứng đầy đủ yêu cầu chuyên môn.
* **Số liệu cụ thể:** Nguyên đơn Derek Mobley (một ứng viên da màu, trên 40 tuổi, mắc chứng lo âu/trầm cảm) đã nộp đơn ứng tuyển vào **hơn 100 vị trí** tại các công ty sử dụng phần mềm Workday (như HP, Comcast, AT&T) và bị hệ thống tự động gửi thư từ chối trong thời gian ngắn kỷ lục, thường là vào ban đêm chỉ sau vài giờ nộp đơn. Tháng 7/2024, Thẩm phán Tòa án Liên bang Rita Lin đã ra phán quyết bác bỏ nỗ lực hủy vụ kiện của Workday, xác lập tiền lệ pháp lý quan trọng: Nhà cung cấp phần mềm AI có thể bị kiện như một "Đại lý tuyển dụng" (Employment Agency) theo Đạo luật Dân quyền Mỹ Title VII, ADEA và ADA.
* **Nguồn kiểm chứng:**
  1. Hồ sơ Tòa án Liên bang Quận Bắc California: *Mobley v. Workday, Inc., Case No. 23-cv-00770-RFL (Order Denying Motion to Dismiss, July 2024)*.
  2. Phân tích pháp lý từ *Bloomberg Law* & *Reuters Legal*: *"Workday must face AI hiring bias lawsuit, judge rules"* (15/07/2024).

---

## PHẦN 3: HARM MAP WORKSHEET

### 📋 Harm Map 1: Amazon AI Recruitment Tool

| Trường phân tích | Nội dung chi tiết |
| :--- | :--- |
| **Tên Case Study** | Amazon AI Recruiting Tool Bias |
| **Failure Layer** | **Model Layer & Data Layer** (Dữ liệu lịch sử bị thiên lệch + Hàm mục tiêu tối ưu hóa sai lệch) |
| **Failure Mode** | **Historical Bias & Algorithmic Discrimination** (Thiên kiến lịch sử dẫn đến phân biệt giới tính) |
| **Root Cause (Nguyên nhân cốt lõi)** | Mô hình được huấn luyện trên 10 năm CV nộp vào Amazon - thời kỳ ngành công nghệ hoàn toàn do nam giới thống trị. Thuật toán học theo mẫu này và coi "yếu tố nam giới" là tiêu chí đại diện cho sự thành công của một kỹ sư. |
| **Sự kiện thực tế có nguồn (Fact)** | - Thuật toán tự động hạ điểm các CV có cụm từ liên quan đến nữ giới như *"women's rugby"*, *"women's technology club"*.<br>- Amazon phải từ bỏ hoàn toàn dự án vào năm 2017/2018 sau khi xác nhận không thể loại bỏ triệt để bias *(Nguồn: Reuters, 2018)*. |
| **Tác hại giả định/tiềm ẩn (Assumption)** | Nếu hệ thống này được triển khai chính thức trên quy mô toàn cầu của Amazon, hàng chục ngàn kỹ sư nữ tài năng sẽ bị loại khỏi vòng sơ tuyển, triệt tiêu nỗ lực đa dạng hóa lực lượng lao động (DEI) và tạo ra rào cản bất bình đẳng giới sâu sắc trong ngành công nghệ. |
| **Human-in-the-loop & Rào chắn khắc phục** | - **Data Pre-processing:** Cân bằng lại tập dữ liệu huấn luyện, loại bỏ các biến số gián tiếp (proxy variables) liên quan đến giới tính.<br>- **Pre-screening Human Review:** Không để AI tự động đánh rớt hồ sơ; con người phải đối soát tỷ lệ giới tính ở danh sách trúng tuyển sơ bộ.<br>- **Algorithmic Auditing:** Kiểm toán định kỳ bằng phương pháp Disparate Impact Ratio (quy tắc 4/5). |

---

### 📋 Harm Map 2: HireVue Facial Analysis

| Trường phân tích | Nội dung chi tiết |
| :--- | :--- |
| **Tên Case Study** | HireVue AI Facial & Speech Video Analysis |
| **Failure Layer** | **Grounding Layer & UX/Product Design Layer** (Khoa học nền tảng không có cơ sở xác thực - Pseudoscience) |
| **Failure Mode** | **Lack of Grounding / Unfair Discrimination Against Disabilities & Minorities** |
| **Root Cause (Nguyên nhân cốt lõi)** | Giả định sai lầm rằng biểu cảm cơ mặt và âm điệu giọng nói thể hiện năng lực làm việc hoặc sự tận tụy của ứng viên. Dữ liệu chuẩn mực (benchmark) được xây dựng trên nhóm người bình thường, không tính đến đặc thù của người khuyết tật và các nền văn hóa phi phương Tây. |
| **Sự kiện thực tế có nguồn (Fact)** | - Tổ chức EPIC đệ đơn khiếu nại chính thức lên FTC vào năm 2019 vì vi phạm quyền người tiêu dùng.<br>- Báo cáo kiểm toán của ORCAA chỉ ra tính năng này tiềm ẩn rủi ro thiên kiến lớn, buộc HireVue phải xóa bỏ tính năng phân tích khuôn mặt vào đầu năm 2021 *(Nguồn: FTC, ORCAA, Washington Post)*. |
| **Tác hại giả định/tiềm ẩn (Assumption)** | Ứng viên mắc bệnh lý thần kinh, tự kỷ, biến dạng cơ mặt hoặc người hướng nội có thể vĩnh viễn bị đánh trượt trong các cuộc phỏng vấn tuyển dụng tự động dù họ có chuyên môn kỹ thuật xuất sắc. |
| **Human-in-the-loop & Rào chắn khắc phục** | - **Cấm sử dụng sinh trắc học cảm xúc (Emotion AI Ban):** Tuân thủ các quy định quốc tế (như EU AI Act cấm sử dụng AI nhận diện cảm xúc tại nơi làm việc).<br>- **Human Evaluation:** Video phỏng vấn chỉ nên được lưu lại để người phỏng vấn thật xem và đánh giá nội dung câu trả lời.<br>- **Quyền lựa chọn hình thức thay thế:** Cho phép ứng viên khuyết tật lựa chọn hình thức phỏng vấn truyền thống. |

---

### 📋 Harm Map 3: Workday AI Screening Lawsuit (Mobley v. Workday)

| Trường phân tích | Nội dung chi tiết |
| :--- | :--- |
| **Tên Case Study** | Workday AI Recruitment Disparate Impact Lawsuit |
| **Failure Layer** | **Model Layer & Safety/Governance Layer** (Thiếu rào chắn kiểm toán độc lập và cơ chế giám sát tuân thủ luật lao động) |
| **Failure Mode** | **Systemic Disparate Impact & Age/Race/Disability Discrimination** |
| **Root Cause (Nguyên nhân cốt lõi)** | Thuật toán tối ưu hóa theo các chỉ số thành công trong quá khứ của các tập đoàn khách hàng, vô tình sử dụng các đặc trưng gián tiếp (như năm tốt nghiệp đại học để suy ra tuổi tác, từ vựng hoặc khoảng trống trong CV để suy ra tình trạng khuyết tật). |
| **Sự kiện thực tế có nguồn (Fact)** | - Nguyên đơn nộp hồ sơ vào hơn 100 vị trí và bị loại tự động hàng loạt trong thời gian ngắn.<br>- Tòa án Liên bang Quận Bắc California bác bỏ đề nghị bãi bỏ vụ kiện của Workday vào tháng 7/2024, công nhận trách nhiệm pháp lý của nhà cung cấp phần mềm tuyển dụng *(Nguồn: US District Court Northern District of California, 2024)*. |
| **Tác hại giả định/tiềm ẩn (Assumption)** | Hàng triệu người lao động lớn tuổi hoặc người thuộc nhóm yếu thế bị "vô hình hóa" trên thị trường lao động, tạo ra một thế hệ lao động bị đào thải phi lý bởi các thuật toán quản trị nhân sự đám mây. |
| **Human-in-the-loop & Rào chắn khắc phục** | - **Bắt buộc Human-Signoff:** Mọi quyết định từ chối hồ sơ phải có chữ ký/phê duyệt của chuyên viên tuyển dụng người thật.<br>- **Minh bạch hóa thuật toán (Algorithmic Transparency):** Cung cấp lý do cụ thể vì sao hồ sơ không phù hợp (ví dụ: thiếu chứng chỉ chuyên môn cụ thể nào) thay vì một thông báo từ chối chung chung.<br>- **Third-party Bias Audit:** Kiểm toán định kỳ hàng năm bởi bên thứ ba độc lập theo tiêu chuẩn Luật NYC Local Law 144 (về công cụ tuyển dụng tự động). |

---

## PHẦN 4: TỔNG KẾT BÀI HỌC VỀ RESPONSIBLE AI TRONG HR TECH

1. **AI không bao giờ trung lập nếu dữ liệu lịch sử mang định kiến:** Máy học không tạo ra sự công bằng một cách tự nhiên; nó sao chép và khuếch đại những thiên kiến có sẵn trong xã hội với tốc độ và quy mô công nghiệp.
2. **Nguyên tắc High-Risk AI System:** Ngành tuyển dụng tác động trực tiếp đến quyền con người và sinh kế, do đó bắt buộc phải áp dụng tiêu chuẩn kiểm toán thuật toán nghiêm ngặt nhất (Fairness Metrics, Explainability, Red-teaming).
3. **Trách nhiệm pháp lý không thể ủy thác cho thuật toán:** Phán quyết vụ *Mobley v. Workday* cho thấy cả doanh nghiệp sử dụng và nhà phát triển nền tảng AI đều phải chịu trách nhiệm trước pháp luật nếu hệ thống tạo ra sự phân biệt đối xử.
4. **Human-in-the-loop là yêu cầu đạo đức tối thượng:** AI chỉ nên đóng vai trò là "trợ lý tóm tắt" và "hỗ trợ tìm kiếm", còn quyết định tuyển chọn và trao cơ hội phải thuộc về sự thấu cảm và trách nhiệm của con người.
