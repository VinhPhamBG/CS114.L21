# Câu hỏi quá trình:
 Tìm ví dụ về bài toán regression ***TRONG THỰC TẾ***
 
 **Yêu cầu:** Ghi rõ input, output và cách thu thập + xử lý data
 
# Bài làm:
## Ví dụ 1: Dự đoán lượng khí thải CO2 của một chiếc xe hơi dựa trên kích thước của động cơ
* **Input:** Thể tích( int ), trọng lượng của xe( int )
* **Output:** Lượng khí Co2 thải ra trong vòng 1 năm( float )
* **Thu thập & xử lý dữ liệu:** Thu thập thông tin thể tích, trọng lượng, khí thải dưa trên công bố của các hãng xe hơi thành một file CVS
## Ví dụ 2: Dự đoán số tiền công ty bảo hiểm phải trả cho một người 
* **Input:** Tuổi (int), cân nặng (int), BMI-chỉ số khối cơ thể (float), tình trạng hôn nhân (bool), nghiện thuốc (bool).
* **Output:** số tiền công ty bảo hiểm sẻ phải trả cho người đó trong năm.
* **Thu thập & xử lý dữ liệu:** file CSV thông tin hóa đơn mà công ty bảo hiểm chi trả trong 10 năm gần nhất với các thuộc tính nói trên. 
## Ví dụ 3: Dự đoán lượng mưa trong năm tại TP.HCM
* **Input:** Nhiệt độ trung bình (float), độ ẩm trung bình (float) của 3 tháng đầu năm.
* **Output:** Lượng mưa trung bình trong năm (float)
* **Thu thập & xử lý dữ liệu:** file CSV bao gồm Nhiệt độ trung bình (float), độ ẩm trung bình (float) của 3 tháng đầu năm và lượng mưa trung bình trong năm (float) của 20 năm gần nhất từ dữ liệu của Trung tâm Dự báo Khí tượng Thủy vân quốc gia.
## Ví dụ 4: Dự đoán sản lượng lúa trong năm tại Đồng Tháp
* **Input:** Nhiệt độ trung bình (float), độ ẩm trung bình (float) trong 2 tháng trước mùa vụ, giống lúa (text)
* **Output:** Sản lượng lúa (float)
* **Thu thập & xử lý dữ liệu:** file CSV gồm Nhiệt độ trung bình (float), độ ẩm trung bình (float) trong 2 tháng trước mùa vụ, giống lúa (text), sản lượng lúa (float) của 50 mùa vụ trước từ dữ liệu của Bộ Nông nghiệp & Phát triển Nông thôn.
