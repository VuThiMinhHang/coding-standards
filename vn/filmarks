#Các quy định về viết code Ruby của dự án Filmarks

##Lề (Indent)
* Độ rộng của lề là 2 khoảng trắng
* Chỉ được dùng space, không được dùng tab

##Số kí tự trên 1 dòng
* Số kí tự tối đa được viết trên 1 dòng là 80 (mỗi kí tự full-width được tính là 2 kí tự)

##Dòng trống
* Thêm dòng trống để ngăn cách các thành phần của cấu trúc, nhưng không được để dòng trống ở trước thành phần đầu tiên và sau thành phần cuối cùng
* Không để dòng trống ở đầu file
* Không để dòng trống ở cuối file

Ví dụ:

```ruby
class Tsumiki
  attr_accessor :user

  def filmarks
  end #filmarks

  def mangamarks
  end #mangamarks

  def dramamarks
  end #dramamarks
end #Tsumiki
```

##Khoảng trắng
* Không để khoảng trắng ở cuối dòng

##Comment
* Giải thích cơ chế của class, module, public method theo style của RDoc

##Mã hóa kí tự
* Dùng dạng mã hóa UTF-8
* Từ Ruby 2.0 trở đi UTF-8 đã trở thành dạng mã hóa mặc định nên không cần phải viết magic comment trong trường hợp dạng mã hóa là UTF-8
* Nếu cần thiết phải dùng magic comment thì viết như dưới:

  ```ruby
  # coding: utf-8
  ```

##Tên module, class
* Đặt tên theo dạng `UpperCamelCase` (Pascal Case)
* Trong trường hợp dùng module như 1 namespace thì sử dụng thư mục để thể hiện cấu trúc phân cấp

##Tên file
* Chỉ sử dụng kí tự thường theo dạng `snake_case`
* Dùng tên của class chính trong file để đặt tên cho file

##Tên method
* Chỉ sử dụng kí tự thường theo dạng `snake_case`
* Về cơ bản thì nên sử dụng động từ
* Đối với những method trả về giá trị `true/false` thì thêm `?` vào ngay sau tên method

##Tên hằng số
* Chỉ sử dụng kí tự viết hoa theo dạng `SNAKE_CASE`

##Tên biến số
* Chỉ sử dụng kí tự thường theo dạng `snake_case`
* Tên biến không được dùng dạng viết tắt tiếng Anh, tuy nhiên trong trường hợp tên biến quá dài, có thể rút ngắn bằng cách giữ lại chữ cái đầu tiên của các từ và bỏ phần còn lại (nên dùng các tên viết tắt thông dụng)
* Có thể sử dụng những tên biến quen thuộc như i, j, k trong vòng lặp...

##Các thành phần của class
1. Include module
2. Định nghĩa hằng số
3. Định nghĩa class variable hoặc instance variable của class
4. Định nghĩa public class method
5. Định nghĩa accessor
6. Định nghĩa initialize
7. Định nghĩa public instance method
8. Định nghĩa protected class method
9. Định nghĩa protected accessor
10. Định nghĩa protected instance method
11. Định nghĩa private class method
12. Định nghĩa private accessor
13. Định nghĩa private instance method

##Định nghĩa class, module
* Sau `end` thêm 1 khoảng trắng rồi viết `#ClassName`

  ```ruby
  class Filmarks
  end #Filmarks
  ```

* Khi muốn alias 1 method, để thống nhất, không dùng `alias` mà dùng `alias_method`
* Khi sử dụng `private`, `protected`, `public` mà không có đối số thì căn lề như định nghĩa method, thêm vào trước sau mỗi từ khóa 1 dòng trống
* Không định nghĩa 1 class thực hiện nhiều nhiệm vụ khác nhau

##Định nghĩa method
* Sau `end` thêm 1 khoảng trắng rồi viết `#method_name`

  ```ruby
  def get_user_age
  end #get_user_age
  ```

* Không được bỏ `()` ở trước và sau danh sách các đối số
* Trong trường hợp không có đối số thì bỏ `()`
* Không thêm khoảng trắng và giữa tên method và `()` của đối số
* 1 method không viết quá 30 dòng
* Không viết 1 method làm nhiều chức năng khác nhau
* Không thay đổi giá trị các đối số
* Sử dụng `self` trong định nghĩa class method

##Định nghĩa biến
* Không tạo thêm các biến global (như `$foo`)
* Không dùng class variable (như `@@bar`). Thay vào đó hãy dùng `class_attribute`
* Không dùng đi dùng lại 1 biến cho nhiều mục đích khác nhau

##Gọi method
* Về cơ bản khi gọi method thì cần cho danh sách các đối số vào trong cặp ngoặc `()`
* Trong trường hợp không có đối số thì bỏ `()`
* Những method dùng cho DSL như dưới đây cũng có thể bỏ `()`
  * Những hàm global như `p`, `print`, `puts`, `require`...
  * Những method mang tính khai báo dùng trong định nghĩa class, module như `attr_reader`, `private`,...
  * Những method được cung cấp bởi ActionController dùng để khai báo xử lí tiếp theo đối với action như `redirect_to`, `render`,...
  * Những method khác được dùng cho DSL...

* Không thêm khoảng trắng và giữa tên method và `()` của đối số
* Khi gọi những method có nhận vào block thì viết block theo cú pháp `do/end`
* Khi cần xử lí giá trị trả về của những method có nhận vào block thì viết block theo cú pháp `{}`
* Khi gọi những method có nhận vào block và viết trên 1 dòng thì viết block theo cú pháp `{}`

##Dấu chấm phẩy
* Không viết dấu chấm phẩy ở cuối dòng

##return
* Khi method trả về giá trị thì nhất định phải có `return`
* Bỏ cặp `()` của `return`

##Accessor
* Dùng `attr_accessor` / `attr_reader` / `attr_writer`, không dùng `attr`

##Phân nhánh điều kiện
* Bỏ `then` của câu lệnh `if`
* Đổi `if !x` thành `unless x`
* Không dùng dạng `unless ? else`
* Nếu có thể viết trên 1 dòng thì có thể đưa `if` ra phía sau
* Bỏ `then` và `:` của `case`

##Vòng lặp
* Bỏ `do` và `:` của `while` và `until`
* Đổi `while !x` thành `until x`
* Nếu có thể viết trên 1 dòng thì có thể đưa `while` ra phía sau

##Toán tử
* Dùng `!` / `&&` / `||`, không dùng `not` / `and` / `or`
* Thêm khoảng trắng vào trước và sau mỗi toán tử

##Biểu thức gán
* Thêm khoảng trắng vào trước và sau kí hiệu phép gán
* Không viết biểu thức gán trong biểu thức điều kiện

##Chuỗi kí tự
* Viết chuỗi kí tự trong cặp dấu nháy đơn
* Trong trường hợp 1 dòng không có escape và thức khai triển thì viết chuỗi kí tự trong cặp dấu nháy đơn
* Trong trường hợp có escape hoặc thức khai triển thì viết chuỗi kí tự trong cặp dấu nháy kép

##Array
* Không dùng `Array.new` cho mảng không có phần tử mà phải dùng `[]`

##Hash
* Không dùng `Hash.new` cho hash không có phần tử mà phải dùng `{}`
