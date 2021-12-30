# Đồ án Triển khai Web thương mại điện tử Wordpress trên lightsail
## 1. Khởi tạo một phiên bản:
#### Trên instances tab của trang chủ Lightsail, chọn Create instance.
![image](https://user-images.githubusercontent.com/89646624/147724150-72c8eef9-2af1-4648-a769-e3ceeea73128.png)

#### Chọn khu vực AWS và khu vực phù hợp với nhu cầu.
![image](https://user-images.githubusercontent.com/89646624/147724167-04885178-c766-41b4-a13f-8d379c977f4e.png)

#### Chọn nền tảng ứng dụng bạn muốn triển khai ( Ở đây là wordpress )
![image](https://user-images.githubusercontent.com/89646624/147724209-9a4b743e-34d6-4fa9-bba0-cb4a4e1bcd60.png)

#### Chọn cấu hình phù hợp với nhu cầu và kinh phí của bạn.
![image](https://user-images.githubusercontent.com/89646624/147724227-f843cc2d-e948-4e4d-9e3a-9e733e39904c.png)

#### Đặt tên phiên bản thõa các điều kiện sau:

   •	Phải là duy nhất trong mỗi khu vực AWS trong tài khoản Lightsail.
   
   •	Chứa từ 2 đến 255 kí tự.
  
   •	Bắt đầu và kết thúc bằng kí tự hoặc chữ số
  
   •	Có thể bao gồm các ký tự chữ và số, dấu chấm, dấu phẩy, dấu gạch ngang, dấu gạch dưới.
  
#### Sau đó nhấn Create instance để tạo phiên bản.
![image](https://user-images.githubusercontent.com/89646624/147724263-47eeafbe-4367-467c-95db-91f89687d934.png)

## 2.Thiết lập IP tĩnh:
#### Chọn phiên bản bạn muốn tạo ip tĩnh trên trang chủ và sang tab Networking. Sau đó nhấn Create static IP.
![image](https://user-images.githubusercontent.com/89646624/147724530-dbc46ab5-09f1-4379-9926-49871776abc6.png)

#### Đặt tên và nhấn Create.
![image](https://user-images.githubusercontent.com/89646624/147724540-973040f7-95f1-4b2b-bc82-6f2f742a244a.png)

## 3. Kết nối SSH:
#### Chọn phiên bản ở trang chủ Lightsail và nhấn connect using SSH để kết nối.
![image](https://user-images.githubusercontent.com/89646624/147724661-5c62f100-c8be-4b4a-97a0-8db8242af384.png)

#### Một cửa sổ sẽ hiển thị lên. Ở đây bạn nhâp lệnh "cat $HOME/bitnami_application_password" để lấy mật khẩu tài khoản admin để bạn đăng nhập vào trang quản trị wordpress.
![image](https://user-images.githubusercontent.com/89646624/147724703-e5724499-f014-48e8-9dac-2fca3eb3bd1e.png)

## 4. Tạo vùng DNS và ánh xạ đến tên miền.
#### Ở trang chủ Lightsail bạn qua tab Networking và nhấn Create DNS zone.
![image](https://user-images.githubusercontent.com/89646624/147724944-c329c295-42c2-49f4-8e1e-dc78d4928c43.png)

#### Nhập tên miền mà bạn có và nhấn Create.
![image](https://user-images.githubusercontent.com/89646624/147724959-57af0166-2bf8-4515-8cea-7454f23af02c.png)

#### Ghi lại các địa chỉ máy chủ định danh được liệt kê trên trang, thêm các máy chủ định danh này vào máy chủ đăng ký tên miền của bạn.
![image](https://user-images.githubusercontent.com/89646624/147724972-c48793fe-9b4e-4b77-abf9-e3839950053b.png)

#### Sau khi thêm các địa chỉ máy chủ định danh bạn tạo một bản ghi A record để trỏ tên miền của bạn về phiên bản wordpress của bạn.
![image](https://user-images.githubusercontent.com/89646624/147724981-5e523094-f9bb-4c40-960c-26e9632e61f9.png)

## 5. Triển khai ứng dụng: 
#### Ta vào địa chỉ IP này.
![image](https://user-images.githubusercontent.com/89646624/147725375-57de57d3-f638-44ed-9c1e-d2ad6ff9eebd.png)
![image](https://user-images.githubusercontent.com/89646624/147725378-fe5f8047-ca8f-4587-8aac-32156c405808.png)

#### Ta thấy trang web của ta đã được triển khai.
#### Ta hãy truy cập: "3.90.21.162/wp-login.php" để vào trang quản trị.
#### Tại đây nhập tài khoản là user còn password ta đã lấy ở bước kết nối với SSH. Ta đã vào giao diện quản trị của wordpress.
![image](https://user-images.githubusercontent.com/89646624/147725409-20182143-071d-4fe3-afb1-4c315a86a7f5.png)

#### Ta đã vào giao diện quản trị của wordpress.
![image](https://user-images.githubusercontent.com/89646624/147725548-b5a2c096-665e-4236-b1f6-dde4ddec91c0.png)

#### Xuống tab Appearance và chọn Add New.
#### Chọn Themes về thương mại điện tử bạn muốn và chọn Insatll. Sau khi tải xong bấm Actice.
![image](https://user-images.githubusercontent.com/89646624/147725746-9a17ece1-dbf8-4c1e-ab1c-f9b4846b1389.png)
## 5.1 Cài đặt 
#### Ở đây ta sẽ cài themes thương mại điện tử tên "ocean wp"
![image](https://user-images.githubusercontent.com/89646624/147726078-f9a59753-fdeb-48a3-99c5-1a998bdab8e9.png)

#### Sau khi dowload xong và nhấn acctive sẽ hiện lên lời nhắc:
![image](https://user-images.githubusercontent.com/89646624/147726166-15280f2f-df84-4222-a242-cf54485c98a0.png)

#### Themes này đề xuất thêm một số plugins khác thì ta bấm "Begin installing plugin" và cài đặt.
#### Sau đó ta sẽ cài thêm các plugins cần thiết cho trang web thương mại điện tử Ocean như:

   •	Ocean Product Sharing

   •	Ocean Custom Sidebar

   •	Ocean Social Sharing

   •	Ocean Stick Anything

   •	Contact Form 7

   •	WooCommerce

   •	WooCommerce Variation Swatches

   •	WooCommerce Wishlist

   •	Custom Sidebars

   •	Elementor Addons & Templates – Sizzify Lite

   •	Essential Addons for Elementor

   •	Premium Addons for Elementor

   •	Elementor Website Builder
#### Sau khi cài đặt xong ta kích hoạt tất cả plugins đã cài đặt.
#### Xuống tab Settings để cài đặt một số thông tin cơ bản cho trang web của bạn.
![image](https://user-images.githubusercontent.com/89646624/147726982-6aa93d66-4b6f-4b56-a8b1-7292b230792c.png)

#### Sau đó lên tab WooCommerce, chọn settings để cài đặt một số thông tin về cửa hàng của bạn.
![image](https://user-images.githubusercontent.com/89646624/147727113-0e452015-2a61-47ab-9f46-ffb3c4d9192d.png)

#### Ở tab Product, chọn categories để thêm các danh mục cho sản phẩm.
![image](https://user-images.githubusercontent.com/89646624/147727378-1a54d70b-767c-4cb0-8cb1-f02a6f71c012.png)

#### Sau khi thêm danh mục cho sản phẩm, ta thêm mới một số sản phẩm ở mục Add new.

## 5.2 Thiết kế trang chủ.
#### Ở tab Page chọn Add new 
![image](https://user-images.githubusercontent.com/89646624/147727679-b67de9ce-5dd3-4a62-856b-63935c295412.png)
#### Đặt tên tiltle là Trang chủ và settings các mục như sau:
![image](https://user-images.githubusercontent.com/89646624/147727812-6aaf979d-2aff-43f8-8611-852f4722c4d1.png)
![image](https://user-images.githubusercontent.com/89646624/147727845-052cf55d-f724-4bc6-ade3-aa52d94bf887.png)
![image](https://user-images.githubusercontent.com/89646624/147727860-1ff568e0-4678-45a3-9e8c-1407e3153837.png)
#### Sau khi cài đặt xong và lưu, chọn Edit with Elementor để thiết kế giao diện trang chủ.
![image](https://user-images.githubusercontent.com/89646624/147727957-ed778cb9-8f63-4cd4-a6a2-c8125983b446.png)
#### Sử dụng Edit with Elementor kéo thả để thiết kế giao diện.
![image](https://user-images.githubusercontent.com/89646624/147728182-be2a6ee1-62e0-4f13-b38b-bb5559cd6908.png)

## 5.3 Xây dựng thanh menu:
#### Ở tab Appearance, chọn Menus để xây dụng menu.
![image](https://user-images.githubusercontent.com/89646624/147728379-e4c7fb61-8168-4185-89d0-9d9c6c186134.png)

## 5.4 Cài đặt Trang chủ.
#### Ở tab Appearance, chọn Customize
![image](https://user-images.githubusercontent.com/89646624/147728517-69e5c799-76cd-461b-a574-c9a757171618.png)
#### Chọn Homepage Settings
![image](https://user-images.githubusercontent.com/89646624/147728602-27e6166f-6e78-4a8b-baab-f004e3d4a4a2.png)
#### Chọn static page và chọn Trang chủ ở mục Homepage.
![image](https://user-images.githubusercontent.com/89646624/147728665-db5fc92e-c3be-49a2-ab8e-cb405b171e59.png)

## 6. Tạo snapshots cho trang web.
#### Ở trang chủ Lightsail vào phiên bản của bạn và sang tab Snapshots, sau đó nhấn Create snapshot
![image](https://user-images.githubusercontent.com/89646624/147728922-d0a35010-fb7c-4f7e-9ce2-94f38a46ee92.png)


