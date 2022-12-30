#  Giới thiệu thư viện Pandas

## 1. Giới thiệu
### 1.1 Pandas là gì?

+ Là thư viện Python mã nguồn mở theo BSD-licensed, hiệu suất cao.
+ Cung cấp các công cụ phân tích dữ liệu, cấu trúc dữ liệu dễ dàng sử dụng cho NNLT Python.
+ Python với Pandas được sử dụng trong nhiều lĩnh vực, bao gồm khoa học, kinh tế, phân tích thống kê, ...
+ Cài đặt: `pip install pandas`
+ Import thư viện để sử dụng: `import pandas as pd`

**Pandas có 3 kiểu cấu trúc dữ liệu:**
+ Series
+ DataFrame
+ Panel

Các cấu trúc dữ liệu này được xây dựng trên NumPy array, có tốc độ nhanh.

### 1.2 Ưu điểm
+ Hỗ trợ đa dạng dữ liệu
+ Tích hợp dữ liệu
+ Chuyển đổi dữ liệu
+ Hỗ trợ dữ liệu time series
+ Thống kê mô tả

**Kích thước (Dimension) và mô tả:** có thể xem Data Frame là một container của series, Panel là một container của Data Frame.

## 2. Series
### 2.1 Series là gì?
**Series** là **mảng một chiều có gán nhãn**, có khả năng chứa các phần tử với kiểu dữ liệu khác nhau (integer, string, float, python objects, ...)

Các axis label của Series được gọi là index.
### 2.2 Phương thức tạo series
`pandas.Series(data, index, dtype, copy)`
**Trong đó:**
+ Data: dữ liệu từ nhiều dạng khác nhau như ndarray, list, constants
+ Index: giá trị của index là duy nhất và số lượng index = số lượng phần tử. Mặc định sẽ có giá trị trong `np.arrange(n)` nếu người dùng không tự tạo index.
+ dtype: kiểu dữ liệu (tuỳ chọn)
+ copy: tạo bản copy (tuỳ chọn)

### Hàm thống kê
+ `count()`: Trả về số lượng các phần tử khác null.
+ `sum()`: Trả về tổng các giá trị.
+ `mean()`: Trả về giá trị tủn bình.
+ `median()`: Trả về giá trị trung vị (hay trung bình giữa của các giá trị).
+ `mode()`: Trả về giá trị có tần suất xuất hiện nhiều nhất.
+ `std()`: Trả về độ lệch chuẩn các giá trị.
+ `min()`: Trả về giá trị nhỏ nhất.
+ `max()`: Trả về giá trị lớn nhất.
+ `abs`: Trả về giá trị tuyệt đối.
+ `prod`: Product of Values.
+ `cumsum()`: Trả về tổng tích luỹ (Cumulative Sum).
+ `cumprod()`: Cumulative Product.

Thông tin thống kê chung, dùng: `describe()`

## 3. DataFrame
### 3.1 DataFrame là gì?

DataFrame là một cấu trúc dữ liệu 2D (two-dimensional), dữ liệu được tổ chức theo dòng và cột.

**Đặc điểm:**
+ Các cột có nhiều kiểu dữ liệu khác nhau
+ Kích thước có thể thay đổi
+ Trục được gán nhãn (dòng và cột)
+ Có thể thực hiện các phép tính số học theo dòng và cột

### 3.2 Phương thức tạo DataFrame
`pandas.DataFrame(Data, index, columns, dtype, copy)`

**Trong đó:**
+ **data**: dữ liệu (list, dict, series, ndarray, dataframe)
+ **index**: danh sách các dòng; index = ["tên dòng 1", "tên dòng 2"]
+ **columns**: danh sách các cột, columns = ["tên cột 1", "tên cột 2"]
+ **dtype**: kiểu dữ liệu các cột
+ **copy**: copy dữ liệu hay không, mặc định là **False**.

### 3.3 Thao tác trên cột
+ Lấy dữ liệu theo cột
+ Thêm cột
+ Xoá cột, dùng: `del/pop()`
+ Xem danh sách các cột, dùng `columns`
+ Lấy dữ liệu theo dòng
+ Cập nhật dữ liệu của dòng
+ Lấy dữ liệu theo điều kiện
+ Thêm dòng, dùng `append()`
+ Xoá dòng, dùng `drop()`
+ Sắp xếp: theo index, dùng `sort_index()`. Theo giá trị, dùng `sort_values()`
+ Xếp hạng, dùng `rank()`
+ Xem thông tin data frame, dùng `info()`
