## Cài đặt

1. xampp
2. Drupal

## Cấu trúc Drupal

### Block layout

- Là các vùng dùng để hiển thị các nội dung của trang web: header, footer, sidebar ...

![1546488506277](C:\Users\USER\AppData\Roaming\Typora\typora-user-images\1546488506277.png)

- Chọn vào Place block để thêm mới các block layout. 

![df](D:\Drupal\image-training-drupal\place-blocks.png)

- Ở mỗi khu vực (regions) có thể thêm nhiều block layout cùng một lúc.

![1546489345423](C:\Users\USER\AppData\Roaming\Typora\typora-user-images\1546489345423.png)

- Chọn vào place block để đặt block vào vị trí mong muốn (ở đây mình đặt ở heder). Sau khi chọn cửa sổ configure block hiện ra

![1546489724313](C:\Users\USER\AppData\Roaming\Typora\typora-user-images\1546489724313.png)

Chọn Save block để lưu lại

- Chọn Configure để chỉnh sửa nội dung của block hoặc thay đổi vị trí hiện thị của nó

![1546489905925](C:\Users\USER\AppData\Roaming\Typora\typora-user-images\1546489905925.png)

- Các block có thể được đặt khác nhau cho mỗi theme 

![1546490284996](C:\Users\USER\AppData\Roaming\Typora\typora-user-images\1546490284996.png)

- Ta cũng có thể set vị trí các block theo thứ tự hiển thị như ý muốn từ trên xuống dưới

![1546490429322](C:\Users\USER\AppData\Roaming\Typora\typora-user-images\1546490429322.png)

- Khi chọn Disable, block sẽ không được hiển thị cho dù đã được enable. Chọn Remove để xóa block

![1546490641432](C:\Users\USER\AppData\Roaming\Typora\typora-user-images\1546490641432.png)

- Custom block library cho phép định nghĩa các block theo ý muốn

![1546490952105](C:\Users\USER\AppData\Roaming\Typora\typora-user-images\1546490952105.png)

### Contact module 

Contact module cho phép người dùng gửi mail cho các người dùng khác hay cho quản trị viên

- Để bật Contact form, Chọn **Menu > Extend** **> Contact module > Click Save**

![1546496843994](C:\Users\USER\AppData\Roaming\Typora\typora-user-images\1546496843994.png)

- Cấu hình Contact form cho toàn bộ trang web

1. Click **Menu > Structure > Contact forms**

2. Click "Add contact form" và nhập các thông tin được yêu cầu

3. Label: Nhập tên form

4. Recipients: Nhập một hoặc nhiều hơn các địa chỉ mail. Mỗi địa chỉ mail cách nhau nhau một dấu phẩy

5. Auto-Reply: Nhập mẫu trả lời tự động. Để trống nếu không muốn trả lời tự động

6. Weights: Đặt thứ tự các biểu mẫu được hiển thị

7. Click "Save".

- Cấu hình Contact form người dùng

1. Chọn **Administration > Configuration > People > Accounts** để kiểm tra xem contact form có được bật cho người dùng theo mặc định hay không
2. Click "Save configuration."

- Menu link

  Nếu muốn hiện thị Contact form trên menu Chọn **Structure → Menus → Footer**. Click **Enable** checkbox. Click **Save**.



  Chọn Edit ở bên phải và ở trường **"Parent link"** để có thể chọn hiển thị ở mục khác nếu muốn. **"weight"** để xét vị trí hiển thị là cao hay thấp



  Nếu muốn dịch Contact form, sử dụng mudule **internationalization** xem tại: [HowTo: Basic Internationalization setup.](https://drupal.org/node/1268692)

  Tạo block nếu muốn add text (name, phone number) vào form 

###  Content types

Trong Drupal, Content types bao gồm các yếu tố chính sau:

- **Base configuration:** định nghĩa hành vi mặc định và thuộc tính của content types

- **Fields:** Content types cho phép tạo ra tập hợp các fields. 

- **Sử dụng Field:** 

  Field được gọi là gì: một field sẽ có một lable (tên hiển thị ở giao diện người dùng), machine name (tên sử dụng nội bộ). lable có thể được sửa lại sau khi đã tạo, còn manchine name thì không



  Kiểu dữ liệu lưu trữ là gì: Mỗi field có thể lưu trữ một loại dữ liệu (text, number, file...). khi định nghĩa một field thì cần phải chọn loại dữ liệu tương ứng với field muốn lưu trữ. Field type không thể sửa lại sau khi đã tạo



  Dữ liệu được nhập và hiển thị như thế nào: Mỗi field type có một hoặc nhiều "widget" được liên kết với nó, mỗi "widget" cung cấp một cơ chế nhập dữ liệu khi chỉnh sửa (text box, select list... ). Mỗi field type cũng có một hoặc tùy chọn hiển thị, xác định cách hiển thị field khi người dùng truy cập trang. Các widget và tùy chọn hiển thị có thể thay đổi sau khi đã tạo field



  Số lượng giá trị field sẽ được lưu trữ: Có thể lưu trữ các giá trị với số lượng tối đa cụ thể hoặc không giới hạn số lượng giá trị trong mỗi trường. Cài đặt này có thể thay đổi sau khi đã tạo field, tuy nhiên nếu giảm số lượng giá trị tối đa đã nhập trước đó, có thể sẽ bị mất thông tin



  Có thể sử dụng field ở nhiều mục, ngoài content type, co thể tạo field cho taxonomy, user account, comment...

- Tái sử dụng Field:

  Khi đã tạo một field với các giá trị xác đinh, và khi cần sử dụng một field với các giá trị giống như một field đã tạo, ta có thể tái sử dụng field đó. Tuy nhiên khi việc phân quyền cho người dùng là khác nhau, một số trường có thể có nhiều cấp truy cập khác nhau, việc này gây khó khăn cho việc tái sử dụng field

- Xóa Field:

  Tiến hành xóa field bình thường. Tuy nhiên có một số module tạo các field một cách tự động và phải gỡ cài đặt để xóa các field của nó. Nếu field không xóa được ngay lập tức, cần chạy lại cron một vài lần

  Việc xóa field thủ công có thể gây lỗi dẫn đến sập trang web, ví dụ như khi hook_field_delete không được gọi. Cách tốt nhất để xóa field là sử dụng Field UI để xóa.

### Menu

- **Tạo menu**

  1. Chọn **Structure > Menus** 

  2. Click **Add menu**.

  3. Trên **Title** field, nhập title

  4. Trên **Administrative summary** field, nhập mô tả ngắn gọn về menu

  5. Click **Save**.


- **Enable menu**
  1. Chọn **Structure > Content type** 
  2. Chọn content type cần bật menu và click **edit**.
  3. Chọn **Menu settings**.
  4. Click the checkbox menu(s) nếu muốn bật menu
  5. (Optional) Set the **Default parent item** to choose a default menu for the content type.



- **Xóa menu**
  1. Chọn **Structure > Menus**
  2. Click **Edit Menu**.
  3. Click **Delete**.
  4. Click **Delete** again to confirm.

- **Mở rộng menu**

  Có thể thêm các menu con cho từng menu cha, để có thể thêm các menu con, các menu cha cần cho phép thêm menu con

![1546509708560](C:\Users\USER\AppData\Roaming\Typora\typora-user-images\1546509708560.png)

​	Các cho phép mở rộng chỉ của từng menu chỉ có phép thêm menu con ngay bên dưới nó. Nghĩa là nếu 			   		menu có 3 cấp, việc cho phép thêm menu con cấp thứ nhất sẽ chỉ cho phép hiển thị các menu con ở cấp thứ 2, không cho phép hiển thị các menu con ở cấp thứ 3. Nếu muốn hiển thị các menu con ở cấp 3 thì lại cần cho phép thêm menu ở cấp 2 -  cấp cha của nó.

​	Mặc định Drupal sẽ chỉ cho phép hiển thị menu 1 cấp, nếu muốn cấp quyền hiển thị menu nhiều cấp thì làm như sau: **Structure > Block layout > Chọn khu vực menu đang tùy chỉnh > và sửa lại cấp độ menu muốn hiển thị**

![1546510138358](C:\Users\USER\AppData\Roaming\Typora\typora-user-images\1546510138358.png)

### Views

- Tổng quan về views

  Sử dụng Views module để lấy content từ cơ sở dữ liệu và hiển thị cho người dùng dưới nhiều dạng như lists, posts, galleries, menu...

  Views UI, một sub module của Views cung cấp giao diện đồ họa và có thể truy cập hầu như mọi thông tin trong cơ sở dữ liệu và hiển thị dưới mọi định dạng

- Thêm bộ lọc vào Views

  Ta có thể configure một view để nó lọc tự động tùy theo nội dung, ví dụ như lọc các bài viết thuộc cùng một tác giả

  Add **relationship** cho views: Khi tạo view từ các bảng cơ sở như comment, content, taxonomy... ta không thể thay đổi sau đó. Khi đó ta chỉ có thể chọn các trường từ các bảng cơ sở đó. Vì thế để có thể get các trường không có sẵn, ta tạo quan hệ (relationship) để join 2 bảng với nhau.

  1. Điều hướng đến màn hình Views, focus tới view cần add relationship > click Edit
  2. Click **Advanced**.
  3. Tại mục Contextual Filters area, click **Add**.
  4. Từ Add Contextual Filters list, chọn một hoặc nhiều filters and click **Apply and Configure Contextual Filters**. 
  5. Tại mục **When the Filter Value is Not Available** section, chọn một hoặc nhiều options:
     - **Display all results for the specified field**
     - **Provide default value**
     - **Hide view**
     - **Display a summary**
     - **Display contents of "No Results Found"**
     - **Display "Access Denied"**
  6. Nếu muốn chỉ định các trường hợp đặc biệt trong các tình huống nhất đinh, tại mục **Exceptions**, chỉ định các giá trị ngoại lệ
  7. Tại mục **When the Filter Value is Available or a Default is Provided**, chọn một hoặc nhiều opption:
     - **Override title**
     - **Override breadcrumb**
     - **Specify validation criteria**
  8. Click **Apply and Continue**. lặp lại bước 5 through 7 for each filter được chọn.

  Add a **display** to a view:

  1. Điều hướng đến màn hình Views
  2. Click **Add+** và lựa chọn từ danh sách các hiển thị.
  3. Thay đổi các hiển thị cần thiết và click **Save**.

  Giới hạn truy cập và display hoặc Views: Ở lựa chọn phía trên bên trái màn hình có lựa chọn **This page** hoặc **All displays**. Với mỗi quyền truy cập khác nhau cần chọn mục tương ứng	

  **View còn nhiều tác vụ khác, tham khảo tại  https://www.drupal.org/docs/8/core/modules/views**

  ### Content

  Gồm các chức năng: thêm content, quản lý comment, file. Chọn **admin > content**

  - Thêm content: Mặc định gồm 2 dạng article và basic page
  - Quản lý commnet: cho phép puslish và unpuslish của users