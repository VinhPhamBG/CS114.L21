# **ĐỒ ÁN MÔN HỌC**
## **ĐỀ TÀI:**   PHÁP HIỆN VÀ NHẬN DẠNG CẢM XÚC  KHUÔN MẶT TRONG THỜI GIAN THỰC VỚI WEBCAM

## **GIỚI THIỆU MÔN HỌC**
* **Tên môn học**: Máy học - MACHINE LEARNING
* **Mã môn học**: CS114
* **Lớp học**: CS114.L21
* **Năm học**: 2020-2021

## **GIẢNG VIÊN HƯỚNG DẪN**
* PGS.TS. **Lê Đình Duy** - *duydl@uit.edu.vn*
* ThS. **Phạm Nguyễn Trường An** *truonganpn@uit.edu.vn*

## **THÀNH VIÊN NHÓM**

| STT    | MSSV          | Họ và Tên           | Email                   |
| ------ |---------------| --------------------|-------------------------|
| 1      | 19522526      | Phạm Quang Vinh     |19522526@gm.uit.edu.vn   |
| 2      | 19522389      | Nguyễn Minh Trí     |19522389@gm.uit.edu.vn   |
| 3      | 19521759      | Trương Xuân Linh    |19521759@gm.uit.edu.vn   |

## **LÝ DO CHỌN ĐỀ TÀI:**
* Cảm xúc của con người là một trạng thái tâm lý sinh học vô cùng phức tạp, thể hiện tâm trạng, suy nghĩ, phản ứng hành vi của con người biểu hiện qua nhiều khía cạnh và phương tiện khác nhau.
* Khuôn mặt là phương tiện đầu tiên và tự nhiên nhất của con người trong truyền đạt thể hiện cảm xúc. Không như ngôn ngữ khuôn mặt thể hiện cảm xúc một cách phổ quát và bẩm sinh nhất, không bị phụ thuộc vào chủng tộc, giới tính hay trình đô.
* Việc nhận diện cảm xúc khuôn mặt rất có nhiều ứng dụng đặt biệt hữu ích trong đời sống xã hội ở nhiều lĩnh vực khác nhau của cuộc sống.
  - **Trong giáo dục:** để đo lường độ hiệu quả của cách thức giảng dạy hay bài giảng thì việc đánh giá cảm xúc của người học trong thời gian thực là điều vô cùng quan trọng đặc biệt là trong thời kỳ dịch bệnh như hiện nay buộc chúng ta phải học tập online.
  - **Trong y tế:** có nhiều ứng dụng đặc biệt là trong chăm sóc sức khỏe tinh thần giúp các bác sỉ có thể tự đọng hóa trong việc phân tích cảm xúc của người bệnh.
  - **Trong an ninh và bảo mật:** giúp xác định hành vi nghi ngờ trong đám đông hay phát hiện nói dối từ đó dự đoán hành vi chuẩn bị phạm tội giúp ngăn chặn tội phạm, khủng bốbố.
  - **Trong tiếp thị:** giúp các công ty sản xuất có thể phân tích được cách mà khách hàng phản ứng với sản phẩm, thiết kế bao bì hay quảng cáo của họ từ đó diều chỉnh cho phù hợp với thị hiếu của thị trường.
  - **Trong ngành dịch vụ:** đây là lĩnh vực mà cảm xúc ha sự hài lòng của khách hàng là một trong những yếu tố qua trọng nhật, việc ứng dụng nhận diện cảm xúc khuôn mặt giúp điều chỉnh cách thức phục vụ hay tạo ra các dịch vụ tự động.
* Chính vì những ứng dụng to lớn và rộng khắp trong nhiều lĩnh vực trên nên nhóm chúng em chọn chủ đề này đề làm chủ đề cho đồ án cuối kì.

## **NỘI DUNG ĐỒ ÁN:**
### **I. MÔ TẢ BÀI TOÁN:**
 Với đề tài này chúng em mong muốn xây dựng một model máy học có thể thực hiện hai việc là ***phát hiện khuôn mặt*** (face detection) và ***nhận diện cảm xúc*** (emotion recognition) với:
* **Input:** video trực tiếp từ webcam máy tính hoặc một video từ một file video quay trước, cụ thể là từng frame hình trong video nói trên.
* **Output:** đoạn video với bbounding box bao quanh các khuôn mặt và dòng text ghi cảm xúc của khuôn mặt đó.

### **II. MÔ TẢ BỘ DỮ LIỆU:**
* Hiện tại nhóm đang trong quá trình thu thập dữ liệu, do tình hình dịch bệnh và thời gian có hạn nên nhóm không thể thu chụp ảnh thực tế được, nên hiện tại nhóm đang tìm kiếm các các nguồn dataset khuôn mặt trên mạng.
* Chúng em có tìm được dataset của một challenge trên kaggle: ***Challenges in Representation Learning: Facial Expression Recognition Challenge 2013***
  - Link: https://www.kaggle.com/c/challenges-in-representation-learning-facial-expression-recognition-challenge/data
* Dữ liệu bao gồm 35,887 bức ảnh xám khuôn mặt người được cân giữa với kích thước 48x48 pixel với Features là integers 0-255. Bộ dữ liệu gồm 7 categories được đánh số từ 0 đến 6 (0=Angry, 1=Disgust, 2=Fear, 3=Happy, 4=Sad, 5=Surprise, 6=Neutral) với số lượng từng class như sau:


| Classes| Files |
|------- |-------|
|Angry   |4953   |
|Disgust |547    |
|Fear    |5121   |
|Happy   |8989   |
|Sad     |6077   |
|Surprise|4002   |
|Neutral |6198   |
  
* **Nhận xét:** Nhận thấy dữ liệu trên không cân về số lượng ảnh của các  categories cụ thể là ở nhóm Disgust rất ít còn Happy lại rất nhiều. Hiện tại chúng em đề ra phương pháp và đang tìm thêm nguồn ảnh khác để bù thêm cho nhóm Disgust.

### **III. MÔ TẢ ĐẶC TRƯNG DỮ LIỆU:**

#### **1. Phân chia dữ liệu:**
* Dataset được nhóm phân chia cụ thể như sau: Trainset với 28,709 bức ảnh, Testset với 7,178 bức ảnh.

| Label | Train | Test |
|-------|-------|------|
|Angry  |3995   |958   |
|Disgust|436    |111  |
|Fear   |4097   |1024   |
|Happy  |7215   |1774   |
|Sad    |4830   |1247  |
|Surprise|3171  |831  |
|Neutral|4965   |1233   |

* Trong Trainset chúng em lấy 20% làm Validation set tức 22,968 ảnh Trainset và 5741 Validation set 

#### **2. Feature Engineering:**

* Chúng em đang thực hiện các phương phápháp khác nhau trong quá trình rút trích đặc trưng ảnh như và xử dụng các mô hình học sâu (Deep learning)
* Co ảnh bằng các rescale ảnh bằng cách chia mỗi pixel cho 255 để dễ hội tụ hơnhơn, lật ảnh, xoa ảnh để có thêm dữ liệu sau đó đưa và mô hình deep learning để rút trích đặc trưng cụ thể nhóm đang sử dụng và so sánh hai mô hình Resnet50 và VGG16 có sử dụng thêm phương pháp Regularization cụ thể là Batch Normalization để chuẩn hóa features giảm overfitoverfitingoverfiting
