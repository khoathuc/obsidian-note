# Program path - đường dẫ chương trình
## Đường dẫn thực thi (execution path)
Đường dẫn hiện tại đang thực thi
## Đường dẫn đích (target path)
Đường dẫn cần sinh dữ liệu kiểm thử

# Các tiêu chí kiểm thử về bài toàn điều khiển luồng dữ liệu
## Bao phủ tập lệnh (statement coverage)
> Là phải tìm các đường dẫn chương trình sao cho, tất cả các câu lệnh được thực hiện ít nhất là một lần ~ tập đỉnh củ đồ thị xuất hiện ít nhất một lần

## Bao phủ quyết định / bao phủ nhánh (branch coverage)
> Đảm bảo tìm hết tất cả các đường dẫn sao cho tất cả các điểm quyết định (là điểm tại đó có rẽ nhánh) trong chương trình được thực hiện ít nhất một lần mỗi nhánh true/false của nó

## Vét cạn (tất cả các path - All-path coverage)
> Tất cả các nhánh được kiểm tra ít nhất một lần

```
bool AccClient(ageType : age; gndrType : gender)
bool accept
	if (gender=famale){
		accept := age < 85;	
	} else {
		accept := age < 80;
	}
```

### Các nước thực hiện
#### Step 1: Dựng sơ đồ điều khiển
#### Step 2: Từ tiêu chí kiểm thưc -> Tìm tập đường dẫn phù hợp
#### Step 3: Với mỗi đường dẫn ! 1 testcase (Inpute + Expected Result)

### Kiểm thử hộp đen
Lớp tương đương
- Male | Age [0, 80]
- Male | Age[81, 99]
- Female | Age [0, 85]
- Female Age [86, 99]
4TC Valid, 2TC Invalid

### Kiểm thử hộp trắng
> Sơ đồ luồng điều khiển
> ![[Pasted image 20221205132011.png]]


#### Bao phủ lệnh (bao phủ tập đỉnh)

####  Bao phủ nhánh 
- Xác định các điểm quyết định không nhất thiết phải là true/false, các câu lệnh rẽ nhánh đều là điểm quyết định
- Mỗi điểm quyết định  được kiểm thử cả 2 nhánh true và false
Các điểm quyết định
(9)(T/F): 
(7)(T/F): 
(4)(c/h):
(6)(e/f):

#### Bao phủ tập lệnh
Các lệnh dược đi qua một lần

# GACC : General Active Clause Coverage
Laf tiêu chí phụ được đưa ra để kết hợp với ACC để cho các giá trị cho mệnh đề phụ khi có sự nhập nhằng
- Thỏa mãn ACC
- Xác định các giá trị của mệnh đề phụ
	- Với mọi mệnh đề phụ Cj là mệnh đề phụ khi xem xét Ci là mệnh đề chính
		- Cj(Ci = true) = Cj(Ci = false) với mọi Cj
		- Cj(Ci = true) != Cj(Ci = false) với mọi Cj


