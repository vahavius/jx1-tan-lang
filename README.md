# Tần Lăng Bí Bảo - JX LINUX

Tính Năng Tần Lăng

![image](https://github.com/user-attachments/assets/355ead4d-90ba-41a2-8601-e8ee3335e065)

![image](https://github.com/user-attachments/assets/9025ebd7-71a7-4491-8813-e79fc44cc802)

![image](https://github.com/user-attachments/assets/c4bacce1-01bc-43df-8f1b-93df87e7eb20)

![image](https://github.com/user-attachments/assets/c13d235c-09ab-4d4f-9923-21bc7972e308)

![image](https://github.com/user-attachments/assets/6287c2d3-47d9-47fa-af5e-5f06ef662548)

![image](https://github.com/user-attachments/assets/33ce8858-2c88-46d7-a078-9d0cba4bcddf)


# A- Hướng Dẫn Cài Đặt
### Lưu ý:

-   Tính năng được viết trên nền JX Linux 8.0 vì vậy chỉ đảm bảo tương thích với bản 8.0 còn bản 6.0 sẽ cập nhật sau.
  
-   Backup những file sửa đổi để phòng trừ khả năng phát sinh lỗi.
 
### Bước 1: Download
#### Thủ công
-   Tải file: [TanLang](https://github.com/cjgawatama/jx1-tan-lang/archive/refs/heads/main.zip)
-   Giải Nén và Dùng WinSCP up lên thư mục gốc `jxser`.
  
-   Tải file:[boss_pain002_tth.zip](https://github.com/user-attachments/files/16439423/boss_pain002_tth.zip)
-   Giải nén ở client  `\spr\npcres\boss`.
#### Tự động (Dành cho các bạn đang chạy bản 1click của bác [Vinh TTN](https://www.facebook.com/groups/800085930700601/user/1576281122)

![](https://github.com/vinh-ttn/materials/blob/main/simcity/caidat_capnhat_simcity.gif)


Yêu cầu game server của bạn phải có kết nối internet

1\) Trong app QuanLyServer, hãy chắc chắn đúng phiên bản server đang sử dụng, sau đó nhấn nút **Up** màu đỏ

2\) Cửa sổ xác nhận sẽ hiện ra, gõ **co** và enter khi gặp câu hỏi xác nhận

3\) Sau đó điền vào **cjgawatama/jx1-tan-lang** và enter để cập nhật từ github này

Xong, khởi động lại game server.

### Bước 2: Cài Đặt 
#### KHAI BÁO NPC

-   Tải file: [addnpc.xlsx](https://github.com/user-attachments/files/16438826/addnpc.xlsx)

-   Mở file bằng excel: `/home/jxser/server1/settings/npcs.txt`
    Coppy  toàn bộ nội dung hàng A1 > A6 trong file `addnpc.xlsx` đã tải phía trên vào  cuối file `npcs.txt`
    ![image](https://github.com/user-attachments/assets/3900fb58-af44-4015-9ddc-27e18e7b79a7)
    Ghi nhớ những  số thứ tự trong file npcs.txt chính là ID boss + 2
    ![image](https://github.com/user-attachments/assets/acb158cd-730a-4db5-bd02-1c51e13086e9)
    Ví dụ trong ảnh: ID Long Mạch  sẽ là: 2061-2 >> 2059 ; tương tự ta có id Bạch Hổ,Thanh Long, Huyền Vũ, Chu Tước, Tần Thuỷ Hoàng  lần lượt là : 2260,2661,2662,2663,2664
    
-   Mở file bằng excel: `/home/jxser/server1/settings/npcres/ÈËÎïÀàÐÍ.txt`
    ![image](https://github.com/user-attachments/assets/b1c64270-7bcb-45d7-8f3d-aa7764ad9680)
    Coppy  toàn bộ nội dung hàng A8 > A9 trong file `addnpc.xlsx` đã tải phía trên vào  cuối file `ÈËÎïÀàÐÍ.txt`
    
-   Mở file bằng excel: `/home/jxser/server1/settings/npcres/ÆÕÍ¨npc×ÊÔ´.txt`
    ![image](https://github.com/user-attachments/assets/05bf3373-ddde-4526-855f-9864072c6bbe)
    Coppy  toàn bộ nội dung hàng A13 > A14 trong file `addnpc.xlsx` đã tải phía trên vào  cuối file `ÆÕÍ¨npc×ÊÔ´.txt`
    
-   Mở file bằng excel: `/home/jxser/server1/settings/npcres/ÆÕÍ¨npc×ÊÔ´ÐÅÏ¢.txt`
    ![image](https://github.com/user-attachments/assets/d8adc63a-d63c-42fa-8d95-0f19808b6af4)
    Coppy  toàn bộ nội dung hàng A17 > A18 trong file `addnpc.xlsx` đã tải phía trên vào  cuối file `ÆÕÍ¨npc×ÊÔ´ÐÅÏ¢.txt`
-   Dùng WinSCP đồng bộ 4 file trên với client
  
#### KHAI BÁO TASK GATEWAY
-   Mở file `tasklist.ini` tại đường dẫn `\gateway\s3relay\relaysetting\task`
-   Kéo xuống cuối cùng và thêm vào 2 dòng:
-   `Task_216]` Thay thế 216 bằng số liền kề task phía trên
-   `TaskFile=tanlang\tg_tanglang.lua `
-   ![image](https://github.com/user-attachments/assets/e388d622-08d7-4e97-866a-d26fec764ae0)
-   Lưu và thoát file `tasklist.ini`
-   
#### KHAI BÁO LỐI VÀO
-   Mở file `autoexec.lua` tại đường dẫn `jxser/server1/script/global/autoexec.lua`
-   Tìm dòng `function main`
-   Thêm vào phía trên: `Include("\\script\\global\\tgiang_dev\\3_chuc_nang\\1_bibaotanlang\fun_tanlang_main.lua")`
-   Thêm vào phía dưới: `add_loivaotanlang()`
#### THAY ĐỔI IDNPC
-   Mở File `fun_tanlang_config.lua` đường dẫn `jxser/server1/script/global/tgiang_dev/3_chuc_nang/1_bibaotanlang/fun_tanlang_config.lua`
-   ![image](https://github.com/user-attachments/assets/aab84959-62ae-4234-831b-75b2ba670519)
-   Thay đổi ID lối vào, và 5 boss (trong ví dụ:2659,2660,2661,2662,2663,2664)  đúng với ID đã khai báo ở bước [KHAI BÁO NPC](https://github.com/cjgawatama/jx1-tan-lang/tree/main?tab=readme-ov-file#khai-b%C3%A1o-npc)

        
### Bước 3: Điều Chỉnh
#### ĐIỀU CHỈNH FILE CONFIG
-   File `fun_tanlang_config.lua` đường dẫn `jxser/server1/script/global/tgiang_dev/3_chuc_nang/1_bibaotanlang/fun_tanlang_config.lua`
-   `CONFIG_TL_ISOPEN = 1` đỏi lại = `0` nếu bạn muốn tắt tính năng
-   `EXP_TL_THANHTHU`,`EXP_TL_THANHTHU_NEAR`,`EXP_TL_TTH`,`EXP_TL_TTH_NEAR` quy định EXP thưởng khi tiêu diệt và đứng gần thánh thú, tần thuỷ hoàng.
-   `tbBossThanhThuItemDropAward` quy định phần thường tiêu diệt 4 thánh thú và Tần Thuỷ Hoàng
-   `tbBossTTHItemDropAward` quy định phần thưởng thêm khi tiêu diệt Tần Thuỷ Hoàng
#### ĐIỀU CHỈNH THỜI GIAN MỞ SỰ KIỆN
-   Hiện tại sụ kiện được mở tự động lúc 20:30 mỗi ngày để thay đổi các bạn thay đổi như sau:
-   Mở file `tg_tanglang.lua` tại đường dẫn `\gateway\s3relay\relaysetting\task\tanlang\tg_tanglang.lua`
-   Điều chỉnh dòng `TaskTime(20, 30);` Thành thời gian bạn muốn
-   Thay đổi mỗi ngày thành ngày chỉ định: **updating**

### VIDEO HƯỚNG DẪN FULL
**UPDATING**
# B- Thông Tin Thêm
