# nhat-ky-tim-hacker
nhat ky tim hacker

hacker sửa file index.php
#có 2 cách => 
+ cách 1 vào phpmyadmin => sửa nội dung bài viết
+ cách 2 sửa trực tiếp ndung file index.php

+ Cách 1 thì khó attach vì mọi thứ là của phpmyadmin dựng sẵn lên
+ Cách 2, nó scan hoặc bằng cách nào đó, nó có được user và pass của con wp-admin, từ đó nó dùng file manager plugin , upload file shell lên (wp-includes/min.php)

### Đưa ra kết luận đó vì:
#### 1.Dựa vào last change của file index.php => quét log trong thời gian đó
log access của apache tại 
/var/log/apache2 (Sau sẽ làm web hỗ trợ tìm kiếm log)
Dựa vào khung thời gian last change index => thấy được có file min.php được truy cập lúc đó => file min chính là file tạo ra file index

#### 2. Lại mở xem file min được tạo ra lúc nào => quét ra thì nó dùng file manager plugin

#### 3. Quét ra thấy ô con login wp-admin
