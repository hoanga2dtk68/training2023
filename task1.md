# Introductory Research Walkthrough
**Task 2  Example Research Question**
*In the Burp Suite Program that ships with Kali Linux, what mode would you use to manually send a request (often repeating a captured request numerous times)?:*
https://brainly.com/question/25315695?cb=1676085236358
![image](https://user-images.githubusercontent.com/110059218/218236273-1d42e7d7-135b-4c64-87e1-712278ee9945.png)
*What hash format are modern Windows login passwords stored in?:*
![image](https://user-images.githubusercontent.com/110059218/218236351-82c73e80-edec-4c70-a900-b7f39052a4a3.png)
> The user passwords are stored in a hashed format in a registry hive either as an LM hash or as an NTLM hash.
> >các password được mã hóa ở dạng LM hash hoặc NTLM hash nhưng LM hash có tính bảo mật yếu hơn nên thường sẽ dùng NTLM hash.
> >LAN Manager authentication uses a particularly weak method of hashing a user's password known as the LM hash algorithm, stemming from the mid 1980s when viruses transmitted by floppy disks were the major concern.[6] Although it is based on DES, a well-studied block cipher, the LM hash has several weaknesses in its design.[7] This makes such hashes crackable in a matter of seconds using rainbow tables, or in a few minutes using brute force. Starting with Windows NT, it was replaced by NTLM, which is still vulnerable to rainbow tables, and brute force attacks unless long, unpredictable passwords are used, see password cracking.
> >vậy câu trả lời sẽ là NTLM
*What are automated tasks called in Linux?*
![image](https://user-images.githubusercontent.com/110059218/218236655-aa1912b9-865a-4474-8a0c-884ffef0e8cb.png)
>cron jobs có tác dụng giúp bạn làm những công việc định kì, tự động hóa trên linux
*What number base could you use as a shorthand for base 2 (binary)?*
>hệ cơ số hexa 2^4 nên chúng ta có thể nhóm 4 bit của hệ 2 thành 1 số trong hệ cơ số hexa
*If a password hash starts with $6$, what format is it (Unix variant)?*
![image](https://user-images.githubusercontent.com/110059218/218236799-927738c9-f9ac-4340-8667-b29cad901e09.png)
*What is the CVE for the 2020 Cross-Site Scripting (XSS) vulnerability found in WPForms?*
> search CVE mitre: WPForms 2020 thu được:
![image](https://user-images.githubusercontent.com/110059218/218236946-534f28da-409b-419d-8579-971ae38d9107.png)
*There was a Local Privilege Escalation vulnerability found in the Debian version of Apache Tomcat, back in 2016. What's the CVE for this vulnerability?*
![image](https://user-images.githubusercontent.com/110059218/218236984-92bd9700-3c2f-4310-9d40-37482641da6c.png)
*What is the very first CVE found in the VLC media player?*
![image](https://user-images.githubusercontent.com/110059218/218237057-5acda158-390a-480c-8f27-2f738bcc9f57.png)
*If you wanted to exploit a 2020 buffer overflow in the sudo program, which CVE would you use?*
![image](https://user-images.githubusercontent.com/110059218/218237293-0824820d-e33e-49d6-9bdf-87799b4df425.png)
![image](https://user-images.githubusercontent.com/110059218/218237305-f4461940-ee75-4d3d-ae5b-bf8c27f737b3.png)
![image](https://user-images.githubusercontent.com/110059218/218237311-4390d6cd-d86c-4521-893d-22b360d0cfd2.png)
**Manual Pages:**
![image](https://user-images.githubusercontent.com/110059218/218237404-efa2a482-6d70-4a76-86d0-bc1175c0f1ad.png)
>fdisk is a command used to view and alter the partitioning scheme used on your hard drive.
*What switch would you use to list the current partitions?:*
sử dụng pipe(đường ống) kết hợp cùng grep(tìm 1 chuỗi) để có kết quả
![image](https://user-images.githubusercontent.com/110059218/218237507-1b83ce5c-d937-40d0-ba8c-edbfdf3016c8.png)
*nano is an easy-to-use text editor for Linux. There are arguably better editors (Vim, being the obvious choice); however, nano is a great one to start with.*
*What switch would you use to make a backup when opening a file with nano?*
![image](https://user-images.githubusercontent.com/110059218/218237886-b0595467-f575-4182-b5ed-f175e4045dad.png)
*Netcat is a basic tool used to manually send and receive network requests. What command would you use to start netcat in listen mode, using port 12345?*
![image](https://user-images.githubusercontent.com/110059218/219766515-9a5d2f19-0b21-49ac-b67a-b58983dcde43.png)
![image](https://user-images.githubusercontent.com/110059218/219766542-50f4bf9e-5a09-4c8c-9a16-f512e06489bd.png)
* đáp án nc -p -l 12345
# LinuxFundamentalsPart1
**A Bit of Background on Linux**
*Research: What year was the first release of a Linux operating system?*
![image](https://user-images.githubusercontent.com/110059218/218238086-078971af-62db-455e-b6ec-af3ad562656e.png)
*Running Your First few Commands*
>If we wanted to output the text "TryHackMe", what would our command be?: echo TryHackMe

*What is the username of who you're logged in as on your deployed Linux machine?*
sử dụng câu lệnh whoami để kiểm tra user mình đang sử dụng
cd: thay đổi thư mục mà chúng ta đang đứng
![image](https://user-images.githubusercontent.com/110059218/218238176-5ba9abf4-df6b-479b-9da0-4fc37e920f2d.png)

**Interacting With the Filesystem!**
ls: liệt kê các file và folder(không bao gồm các file ẩn)
cat: đọc một file hoặc có thể ghép nội dung các file lại với nhau, ghi đè hoặc tạo một file mới
pwd: kiểm tra thư mục mà mình đang đứng

![image](https://user-images.githubusercontent.com/110059218/218238443-4ee66114-e8f0-4f22-ad3b-437034ab09c8.png)
* question 1
dùng lệnh ls để kiểm tra số thư mục đang có
* question 2
thực hiện cd vào từng thư mục để kiểm tra hoặc dùng lệnh ls để kiểm tra với option -R
![image](https://user-images.githubusercontent.com/110059218/218238464-4a5fe5a2-4c5a-4308-a1cc-3eab106880f5.png)

**Searching for Files**
&: thực hiện chạy ngầm task
>: ghi đè nội dùng file
>>: ghi tiếp vào cuối file
![image](https://user-images.githubusercontent.com/110059218/218238552-31c07662-ec7a-4154-8c99-c1199811a29c.png)
![image](https://user-images.githubusercontent.com/110059218/218238559-6d9467fb-4cd1-4f14-8072-f778d8244070.png)
**An Introduction to Shell Operators**
![image](https://user-images.githubusercontent.com/110059218/218238892-d55b3c5c-ba23-46d0-9618-154db8c2084d.png)
# LinuxFundamentalsPart2
**Introduction to Flags and Switches**
![image](https://user-images.githubusercontent.com/110059218/218239973-9ee543ea-7fa5-4767-a47c-fbf406e58894.png)
![image](https://user-images.githubusercontent.com/110059218/218239982-b6104382-bb8b-438e-8646-681e91092641.png)
**Filesystem Interaction Continued**
touch: tạo 1 file rỗng mới
file: kiểm tra định dạng của file
cat: đọc file
![image](https://user-images.githubusercontent.com/110059218/218240133-ca643b49-4b57-47eb-ab3b-406dee3075b1.png)
**Permissions 101**
![image](https://user-images.githubusercontent.com/110059218/218240189-fb864f8d-ce0b-4da0-809f-866fa7627089.png)
**Common Directories**
![image](https://user-images.githubusercontent.com/110059218/218242522-a56b74c1-059e-4e4a-b084-6d2b8b6b35b2.png)
# LinuxFundamentalsPart3
**Terminal Text Editors**
![image](https://user-images.githubusercontent.com/110059218/218243016-2f2cc41a-861b-4764-9a28-3c0e0593105a.png)
**General/Useful Utilities**
![image](https://user-images.githubusercontent.com/110059218/218243425-ffe9d3bd-0554-441d-933c-9ceace45fb49.png)
**Processes 101**
![image](https://user-images.githubusercontent.com/110059218/218244391-5bebce7d-114f-404e-a877-2a2d9d0d6366.png)
**Maintaining Your System: Automation**
![image](https://user-images.githubusercontent.com/110059218/218244906-f4a417c8-e0ba-4cf9-bbef-706576f2b7a2.png)
**Maintaining Your System: Package Management**
![image](https://user-images.githubusercontent.com/110059218/218245541-11fffe93-48a3-481f-afef-8eae35b67279.png)
# Google Dorking
**Let's Learn About Crawlers**
![image](https://user-images.githubusercontent.com/110059218/218246728-2b8bf15c-d6b9-4933-8a02-03903e762cb2.png)
![image](https://user-images.githubusercontent.com/110059218/218246732-3d9aa3db-5874-426c-a57f-f5da43e3bb4d.png)
**Beepboop - Robots.txt**
phần này thì em đọc và làm giống hướng dẫn thôi
![image](https://user-images.githubusercontent.com/110059218/218534425-32d320f2-3a24-47ac-8d4e-014f6f118a6a.png)
![image](https://user-images.githubusercontent.com/110059218/218535447-dcea6fda-778b-4d7e-8c7b-7d0cb4175e6f.png)
**Sitemaps**
![image](https://user-images.githubusercontent.com/110059218/218536416-f1829537-47ba-428b-99a6-647c4022a1b3.png)
**What is Google Dorking?**
![image](https://user-images.githubusercontent.com/110059218/218537266-34571ccc-0aef-446a-951d-b7fea0ad0340.png)
**Enter: Search Engine Optimisation**
![image](https://user-images.githubusercontent.com/110059218/218669620-f00784aa-9b84-437f-abff-72e7edbdbc56.png)
![image](https://user-images.githubusercontent.com/110059218/218671293-54888b01-f393-4c39-8b1f-1f6ef6779f1c.png)
# OhSint
**What is this users avatar of?**
dùng exiftool:
![image](https://user-images.githubusercontent.com/110059218/218248344-485e2cf5-49a5-45bc-8b04-6e5862f0668e.png)
thu được tên người dùng là OWoodflint
tìm được thấy twitter có hình đại diện là một con mèo nên câu trả lời đầu tiên sẽ là cat
**What city is this person in?**
**Whats the SSID of the WAP he connected to?**
>dùng chức năng advance search của wigle.net
![image](https://user-images.githubusercontent.com/110059218/218248388-2ec35045-0e6a-49a2-9e8a-e846f05262aa.png)
tìm được câu trả lời cho câu hỏi 2 và 3 lần lượt là LonDon và UnileverWiFi
**What is his personal email address?**
![image](https://user-images.githubusercontent.com/110059218/218248570-d6205208-d552-481d-ad2f-6c3fe1539545.png)
vào github lấy được gmail của chủ sở hữu :OWoodflint@gmail.com
**What site did you find his email address on?:github**
**Where has he gone on holiday?**
google tìm thấy một trang wordpress của owoodflint có nội dung 
![image](https://user-images.githubusercontent.com/110059218/218248780-4dc94591-8e4a-4062-98e8-a6c5ee8772fc.png)
-> New York
**What is this persons password?**
do wordpress là trang của người dùng phải tự giấu thông tin nên nó khả nghi nhất trong khi twtitter và github bảo mật về mật khẩu khá tốt em check từng phần trong web thì phần dưới có để màu trắng
![image](https://user-images.githubusercontent.com/110059218/218249259-067514f6-5927-47f0-a184-0ece916af016.png)
# shodan
**Filters**
![image](https://user-images.githubusercontent.com/110059218/218293604-69585a9b-7015-4512-8e9d-4792e5ff563b.png)
![image](https://user-images.githubusercontent.com/110059218/218293599-5fdc9e75-7046-4657-afaf-ac4211901893.png)
**Google & Filtering**
*What is the 2nd most popular country for MYSQL servers in Google's ASN?*
![image](https://user-images.githubusercontent.com/110059218/218820411-d672994c-b0cf-4f8b-9287-176632313d94.png)
*What is the top operating system for MYSQL servers in Google's ASN?*
![image](https://user-images.githubusercontent.com/110059218/218821064-7b9258f3-58c4-47e4-8c0d-196541f1806b.png)
![image](https://user-images.githubusercontent.com/110059218/218821081-fd415c94-4995-4f6f-9861-51727394558c.png)
* cái này em dùng kết quả của hint do bài ra từ khoảng năm 2021 nên chắc có thể đã được update
*Under Google's ASN, which is more popular for nginx, Hypertext Transfer Protocol or Hypertext Transfer Protocol with SSL?*
![image](https://user-images.githubusercontent.com/110059218/218821737-1a61b7c4-d044-41b0-8613-44ab2f1cefaa.png)
* giao thức này cũng khá là phổ biến nên em nghĩ không cần nói gì thêm
*Under Google's ASN, what is the most popular city?*
![image](https://user-images.githubusercontent.com/110059218/218824440-a2fbe7c3-699c-4290-a654-e393f54f21ab.png)
* câu này lại ra kq khác có lẽ tryhackme lâu không update bài này
*Under Google's ASN in Los Angeles, what is the top operating system according to Shodan?*
![image](https://user-images.githubusercontent.com/110059218/218826869-bb70a119-03b4-4b7c-81bb-5a7221008d5e.png)
![image](https://user-images.githubusercontent.com/110059218/218826928-da33bd1c-926b-487d-b377-eb8d88664fd2.png)
* có lẽ đây vẫn là câu tryhackme chưa cập nhật
*Using the top Webcam search from the explore page, does Google's ASN have any webcams? Yay / nay.*
![image](https://user-images.githubusercontent.com/110059218/218827185-82cb021b-9ad7-4a38-bb20-1c62a37b2057.png)
* tiếp tục là 1 câu sai của tryhackme
![image](https://user-images.githubusercontent.com/110059218/218827346-fea7c475-95b4-4948-b959-66a370f2427e.png)
**Shodan Monitor**
* câu này chỉ đơn giản là copy đường link phía trên
![image](https://user-images.githubusercontent.com/110059218/218827595-757829f9-b61e-46cc-bb25-6b31ff64cf72.png)
**Shodan Dorking**
![image](https://user-images.githubusercontent.com/110059218/218827744-22f5d0bb-1196-48a3-84cd-f274e3a711ed.png)
# Introdigitalforensics
**Introduction To Digital Forensics**
![image](https://user-images.githubusercontent.com/110059218/218290750-5ccffa7e-14da-4ec4-bc95-a59eab729bed.png)
**Digital Forensics Process**
![image](https://user-images.githubusercontent.com/110059218/218290759-8a760866-8405-4456-8c85-08a0aaf18b27.png)
![image](https://user-images.githubusercontent.com/110059218/218290768-f32cd132-5ae9-4bb8-ab8b-046b7e094f0a.png)
**Practical Example of Digital Forensics**
![image](https://user-images.githubusercontent.com/110059218/218291015-9870ec1e-966f-46da-ac42-526d25ba0191.png)
![image](https://user-images.githubusercontent.com/110059218/218290897-16916b22-d5a4-4f50-aeef-511faa114a00.png)
![image](https://user-images.githubusercontent.com/110059218/218290987-d736f16f-2477-4a2b-9ac8-a67bbfaaead7.png)
![image](https://user-images.githubusercontent.com/110059218/218290978-ab691994-6d7f-45ce-82c5-c4424a906054.png)
![image](https://user-images.githubusercontent.com/110059218/218291121-10e42fcb-906a-4e7c-bbcf-8d5372ea3363.png)
![image](https://user-images.githubusercontent.com/110059218/218291126-7580afc9-a232-436a-8812-ca7a7aa0bc93.png)
![image](https://user-images.githubusercontent.com/110059218/218291130-f7a05871-7abe-4e35-aa67-767968852520.png)
# Windows Fundamentals 1
**Windows Editions**
![image](https://user-images.githubusercontent.com/110059218/218509423-3470dd29-2cb3-4af0-bbf5-1ad22c264b14.png)
![image](https://user-images.githubusercontent.com/110059218/218509535-5492c60f-1221-4791-8518-d8460fbbcc39.png)
search google dễ dàng thấy được câu trả lời là bitlocker
**The Desktop (GUI)**
![image](https://user-images.githubusercontent.com/110059218/218511782-42ebbf3c-187d-4e35-9891-d0d5d7c6b01d.png)
**The File System**
![image](https://user-images.githubusercontent.com/110059218/218520063-c9b335c6-5383-43b3-9407-fc3eca3e56f3.png)
![image](https://user-images.githubusercontent.com/110059218/218520141-94d8fcc1-f7b5-4410-9da7-8e683da8d3dd.png)
**The Windows\System32 Folders**
![image](https://user-images.githubusercontent.com/110059218/218520581-a1175be8-2a9a-49b3-a214-9b9c48602847.png)
![image](https://user-images.githubusercontent.com/110059218/218520646-40eec3f5-ff82-41ad-a5be-cc4ee833693f.png)
**User Accounts, Profiles, and Permissions**
![image](https://user-images.githubusercontent.com/110059218/218521343-b4307fd6-5a22-4418-b4ee-7fff7a06e584.png)
![image](https://user-images.githubusercontent.com/110059218/218521377-0ad608a5-92c7-4687-86c2-91e4a02560fd.png)
![image](https://user-images.githubusercontent.com/110059218/218521769-1afc17f2-27b9-4f71-9474-6a8014be6a9e.png)
![image](https://user-images.githubusercontent.com/110059218/218522045-ac666ecf-8b6d-46bc-a34e-259e5c79e821.png)
![image](https://user-images.githubusercontent.com/110059218/218522355-01075a41-7d33-4fe8-9cba-e7cc47bb2c19.png)
**User Account Control**
![image](https://user-images.githubusercontent.com/110059218/218523703-d2f6f53c-f0ad-4ed2-a013-5dced8960ba7.png)
**Settings and the Control Panel**
![image](https://user-images.githubusercontent.com/110059218/218525086-1f46f8e3-8571-415d-a5d6-92f6d506fe49.png)
![image](https://user-images.githubusercontent.com/110059218/218525141-7d5138a9-3730-483e-b3c6-742769ca1a98.png)
**task manager**
![image](https://user-images.githubusercontent.com/110059218/218525849-3f3a837d-51f9-43a6-8891-3e39a347e56d.png)
# Autospy
**What is the MD5 hash of the E01 image?**
mở autospy và dễ dàng tìm được MD5
![image](https://user-images.githubusercontent.com/110059218/218314990-111be3a5-961f-42ae-a0a5-3ac9e2dc3fcd.png)
**What is the computer account name?**
![image](https://user-images.githubusercontent.com/110059218/218315127-6f543616-9646-4e08-a880-693555e13b46.png)
![image](https://user-images.githubusercontent.com/110059218/218315136-44a13230-249b-4f04-b9a2-75214d07c6ba.png)
**List all the user accounts. (alphabetical order)**
tương tự câu trên liệt kê ra các user theo thứ tự bảng chữ cái trừ những user mặc định
![image](https://user-images.githubusercontent.com/110059218/218316374-654c3193-57ee-4725-b979-4087ad9dcb2d.png)
**Who was the last user to log into the computer?**
filter cột data acess thu được
![image](https://user-images.githubusercontent.com/110059218/218316635-8e6407d5-327a-45d1-8daf-aa172b56f895.png)
**What was the IP address of the computer?**
![image](https://user-images.githubusercontent.com/110059218/218467682-aee83f52-bc9a-4eda-bb5b-3a0e1429741d.png)
**What was the MAC address of the computer? (XX-XX-XX-XX-XX-XX)**
![image](https://user-images.githubusercontent.com/110059218/218468000-45597de9-d8ba-413c-83cf-d55766dab0ee.png)
**What is the name of the network card on this computer?**
![image](https://user-images.githubusercontent.com/110059218/218468249-d195ea24-4e03-47a9-8a2a-0fa60be0e7df.png)
![image](https://user-images.githubusercontent.com/110059218/218469751-25f2516a-81a3-4b9a-ac71-9d5b829dbd7e.png)
![image](https://user-images.githubusercontent.com/110059218/218473855-b7b4ccef-db09-4cc5-912d-5a2317f428d3.png)
**A user bookmarked a Google Maps location. What are the coordinates of the location?**
>theo link bookmarked thôi :v
![image](https://user-images.githubusercontent.com/110059218/218480050-07821a41-a336-4398-a6fb-45e7025c34c6.png)
**A user has his full name printed on his desktop wallpaper. What is the user's full name?**
![image](https://user-images.githubusercontent.com/110059218/218832182-0342537e-7131-40a7-9e21-dfb594e070e6.png)
**câu này đơn giản là xuất ảnh và ngồi check thì có thấy joshwa có 1 tấm hình được viết tên ở trên góc mở anh lên và có câu trả lời**
![image](https://user-images.githubusercontent.com/110059218/218832739-44017db9-4caf-47b4-a4d8-0f320a203371.png)
**A user had a file on her desktop. It had a flag but she changed the flag using PowerShell. What was the first flag**
![image](https://user-images.githubusercontent.com/110059218/218832897-e50519b1-d405-4615-90e7-95d3e63f90da.png)
* cái này thì em ngồi check từng user một thôi
![image](https://user-images.githubusercontent.com/110059218/218835024-c135bd9b-05b2-438d-90a4-26f4ac614b07.png)
![image](https://user-images.githubusercontent.com/110059218/218835639-9942b2ce-f8df-4bc0-8972-7ccbff15035a.png)
![image](https://user-images.githubusercontent.com/110059218/218835997-d4aca901-553e-450a-bb2e-874b64755ee2.png)
**The same user found an exploit to escalate privileges on the computer. What was the message to the device owner?**
![image](https://user-images.githubusercontent.com/110059218/218836444-e498e8cf-e05a-4a76-aaf8-d043540a7301.png)
* vẫn thực hiện check đúng trên user đó
**The same user found an exploit to escalate privileges on the computer. What was the message to the device owner?**
thường các tool sẽ bị windows denfender lưu lại giờ chỉ cần tìm path về lịch sử thôi
![image](https://user-images.githubusercontent.com/110059218/218838203-7309d7ca-6dbd-4cc6-b347-1bc9f80bce52.png)
dễ dàng tìm thấy mimikatz và tên 1 tool khác nữa
**There is a YARA file on the computer. Inspect the file. What is the name of the author?**
câu này dùng tính năng keyword search về thu được kết quả path bên dưới
![image](https://user-images.githubusercontent.com/110059218/218838819-1eb126c8-95b0-44b1-bb34-3846b4238fd9.png)
![image](https://user-images.githubusercontent.com/110059218/218839388-1e375ab9-b1f9-44e1-a53b-2336440c4fdd.png)
**One of the users wanted to exploit a domain controller with an MS-NRPC based exploit. What is the filename of the archive that you found? (include the spaces in your answer)** 
search MS-NRPC thì cho kết quả là netlogon sau khi đọc một lúc và có thử search keyword netlogon không ra thì thấy exp;oit này có tên gọi chung là zerologon
dùng tính năng search file name của autospy
![image](https://user-images.githubusercontent.com/110059218/218845730-7baca908-0541-499f-8875-9428749fa724.png)
-> done
# volatility
**Obtaining Memory Samples**
![image](https://user-images.githubusercontent.com/110059218/218677413-bbed680f-2e2e-4ef8-af5f-dbbf7461b86a.png)
![image](https://user-images.githubusercontent.com/110059218/218677510-c489e752-4487-4321-81a3-8f92f4487d50.png)
![image](https://user-images.githubusercontent.com/110059218/218677545-67d65dd6-6f06-4b70-9c4f-c66ea6feb8e8.png)
**Examining Our Patient**
*Running the imageinfo command in Volatility will provide us with a number of profiles we can test with, however, only one will be correct. We can test these profiles using the pslist command, validating our profile selection by the sheer number of returned results. Do this now with the command `volatility -f MEMORY_FILE.raw --profile=PROFILE pslist`. What profile is correct for this memory image?*
![image](https://user-images.githubusercontent.com/110059218/219040189-be54a3a9-2ba0-4c5d-a0f6-9a2dc9de6b16.png)
*Take a look through the processes within our image. What is the process ID for the smss.exe process? If results are scrolling off-screen, try piping your output into less*
![image](https://user-images.githubusercontent.com/110059218/219040418-ceae7250-5d27-4ce2-bcf9-a08dba70ae6a.png)
*It's fairly common for malware to attempt to hide itself and the process associated with it. That being said, we can view intentionally hidden processes via the command `psxview`. What process has only one 'False' listed?*
![image](https://user-images.githubusercontent.com/110059218/219042003-1e8768e2-af10-424c-9c3d-2a5cef6b4abd.png)
*In addition to viewing hidden processes via psxview, we can also check this with a greater focus via the command 'ldrmodules'. Three columns will appear here in the middle, InLoad, InInit, InMem. If any of these are false, that module has likely been injected which is a really bad thing. On a normal system the grep statement above should return no output. Which process has all three columns listed as 'False' (other than System)?*
![image](https://user-images.githubusercontent.com/110059218/219087791-4b8cea05-dd78-42cf-be2a-dbf36bc0c8a9.png)
* theo ảnh ở question trên thì đáp án là csrss.exe
*Injected code can be a huge issue and is highly indicative of very very bad things. We can check for this with the command `malfind`. Using the full command `volatility -f MEMORY_FILE.raw --profile=PROFILE malfind -D <Destination Directory>` we can not only find this code, but also dump it to our specified directory. Let's do this now! We'll use this dump later for more analysis. How many files does this generate?*
![image](https://user-images.githubusercontent.com/110059218/219276325-0bfdfbcb-54d3-458e-aba8-65bb9412e1c1.png)
![image](https://user-images.githubusercontent.com/110059218/219276443-500b3081-7f75-4bd2-91a3-18c4a4ad3bc0.png)
![image](https://user-images.githubusercontent.com/110059218/219276818-94f57ccc-13d4-4910-bff1-10fbda7450ce.png)
*Now that we've seen all of the DLLs running in memory, let's go a step further and pull them out! Do this now with the command `volatility -f MEMORY_FILE.raw --profile=PROFILE --pid=PID dlldump -D <Destination Directory>` where the PID is the process ID of the infected process we identified earlier (questions five and six). How many DLLs does this end up pulling?*
quay lại ảnh của câu hỏi trước dễ thấy PID của csrss.exe là 584
![image](https://user-images.githubusercontent.com/110059218/219277789-655387c0-6598-4b72-8c3f-70f1593c86b9.png)
**Post Actions**
*Upload the extracted files to VirusTotal for examination.*
![image](https://user-images.githubusercontent.com/110059218/219426302-1357e23f-aa0e-42f1-b5e5-7e838e733607.png)
*What malware has our sample been infected with? You can find this in the results of VirusTotal and Hybrid Anaylsis.*
![image](https://user-images.githubusercontent.com/110059218/219426955-6cafed47-674d-4d72-beba-0f72e51e8f7a.png)
thực hiện search google một lúc thì em có search ra cridex là tên một malware
![image](https://user-images.githubusercontent.com/110059218/219427615-12120fcd-126f-40ac-9823-c6fa15b10d86.png)
# redline
**Introduction**
![image](https://user-images.githubusercontent.com/110059218/218943535-e30335b8-2566-43e9-965b-7b9dfcd6e6e8.png)
**Data Collection**
*What data collection method takes the least amount of time?*
*You are reading a research paper on a new strain of ransomware. You want to run the data collection on your computer based on the patterns provided, such as domains, hashes, IP addresses, filenames, etc. What method would you choose to run a granular data collection against the known indicators?*
![image](https://user-images.githubusercontent.com/110059218/219562316-fb3ed76c-e467-4492-abff-a3987903a1d8.png)
*What script would you run to initiate the data collection process? Please include the file extension.*
![image](https://user-images.githubusercontent.com/110059218/219562409-99b37fed-b420-4e95-a1c7-e647e604c2e1.png)
*If you want to collect the data on Disks and Volumes, under which option can you find it?*
![image](https://user-images.githubusercontent.com/110059218/219562941-4aadbbdb-498a-43d5-be46-cba3863c809a.png)
*What cache does Windows use to maintain a preference for recently executed code?*
![image](https://user-images.githubusercontent.com/110059218/219563250-934f37a4-a270-44bb-8128-aad87d025ee6.png)
phần này chỉ việc đọc hướng dẫn dùng và trả lời
**The Redline Interface**
*Where in the Redline UI can you view information about the Logged in User?*
![image](https://user-images.githubusercontent.com/110059218/219615539-caf140e1-9c94-4128-a317-7219dccba45b.png)
**Where in the Redline UI can you view information about the Logged in User?**
*Provide the Operating System detected for the workstation.*
![image](https://user-images.githubusercontent.com/110059218/219678778-cb0ce58f-2dee-41cb-b14b-9d7695c542f2.png)
*Provide the BIOS Version for the workstation.*
![image](https://user-images.githubusercontent.com/110059218/219678896-5e6c7375-17a4-4ec1-af36-ade3104eba1d.png)
*What is the suspicious scheduled task that got created on the victim's computer?*
![image](https://user-images.githubusercontent.com/110059218/219679123-7ea43149-080f-45c9-a825-c2e140aa46fd.png)
* câu này vào task thì thấy comment hiện khá rõ
*Find the message that the intruder left for you in the task.*
![image](https://user-images.githubusercontent.com/110059218/219679614-951b56c7-49f8-48b7-80b6-4790a53349ac.png)
*There is a new System Event ID created by an intruder with the source name "THM-Redline-User" and the Type "ERROR". Find the Event ID #.*
![image](https://user-images.githubusercontent.com/110059218/219679754-f7c32b81-47da-42bb-be21-6698c1cf26a6.png)
*Provide the message for the Event ID.*
![image](https://user-images.githubusercontent.com/110059218/219679910-2c3b1933-71ce-4e89-932a-8f671d2dcfed.png)
*It looks like the intruder downloaded a file containing the flag for Question 8. Provide the full URL of the website.*
![image](https://user-images.githubusercontent.com/110059218/219680157-194c514e-8b58-4ec1-8e5f-2bc45268d136.png)
*Provide the full path to where the file was downloaded to including the filename.*
* lấy đường dẫn từ ảnh của question trên
*Provide the message the intruder left for you in the file.*
* THM{600D-C@7cH-My-FR1EnD} đi đến thư mục để download xuống và đọc flag thôi
![image](https://user-images.githubusercontent.com/110059218/219681187-29f3e5e5-4979-4e03-9ff7-76a2aaffcf0d.png)
**IOC Search Collector**
*What is the actual filename of the Keylogger? *
* psylog.exe
*What filename is the file masquerading as?*
![image](https://user-images.githubusercontent.com/110059218/219737463-ff53eb27-399d-4074-a8a8-3d7a9a85dac7.png)
* THM1768.exe
*Who is the owner of the file?*
![image](https://user-images.githubusercontent.com/110059218/219738120-68f06b29-f1c4-46ad-b7d2-2ae5267646f7.png)
* câu này lấy kết quả từ cột owner sang
*What is the file size in bytes?* 
![image](https://user-images.githubusercontent.com/110059218/219738952-04a4380f-a461-48b1-b87c-ea78a1a05b54.png)
*Provide the full path of where the .ioc file was placed after the Redline analysis, include the .ioc filename as well*
![image](https://user-images.githubusercontent.com/110059218/219739936-da2edf25-dc89-4bd2-8521-5524ae76f55b.png)
**IOC Search Collector Analysis**
*Provide the path of the file that matched all the artifacts along with the filename.*
![image](https://user-images.githubusercontent.com/110059218/219763824-8e2f4650-266b-43fc-a880-2e197d898a7b.png)
*Provide the path where the file is located without including the filename.*
> C:\Users\Administrator\AppData\Local\Temp\
*Who is the owner of the file?*
> BUILTIN\Administrators(từ ảnh trên)
*Provide the subsystem for the file.*
![image](https://user-images.githubusercontent.com/110059218/219764785-bd28a6c3-f20f-4ad2-a075-be6b3e98441e.png)
*Provide the Device Path where the file is located.*
![image](https://user-images.githubusercontent.com/110059218/219765226-2957a2cf-84b1-4240-872e-94e64a34b1fb.png)
*Provide the hash (SHA-256) for the file.*
* có md5 của mã độc lên virus total hoặc hybrid analyse check hoặc theo gợi ý dùng câu lệnh get file-hash trong cmd
![image](https://user-images.githubusercontent.com/110059218/219766088-eeb9a058-6c6d-4d4d-9af8-40a2008e1320.png)
*The attacker managed to masquerade the real filename. Can you find it having the hash in your arsenal?*
* tìm real name thì hint cũng có gợi ý lên virus total :
![image](https://user-images.githubusercontent.com/110059218/219766281-286a6b63-a4d7-4a5c-ab2c-44b03ff19fe6.png)
**Endpoint Investigation**
*Can you identify the product name of the machine?*
![image](https://user-images.githubusercontent.com/110059218/219742264-5724e331-99a1-4a16-9754-766f638c695e.png)
*Can you find the name of the note left on the Desktop for the "Charles"?*
![image](https://user-images.githubusercontent.com/110059218/219743525-83357787-80f3-46a2-b429-7929d447408d.png)
*Find the Windows Defender service; what is the name of its service DLL?*
![image](https://user-images.githubusercontent.com/110059218/219744160-4621a8f2-d80c-48cc-b41c-933ab4bd92fe.png)
*Provide the filename of the malicious executable that got dropped on the user's Desktop.*
![image](https://user-images.githubusercontent.com/110059218/219744817-2c331368-68a3-4465-8326-098f48d5f838.png)
> vào file download history search .zip và ra kết quả
*Provide the filename of the malicious executable that got dropped on the user's Desktop.*
![image](https://user-images.githubusercontent.com/110059218/219749077-f6fba5d2-4dbb-4d9c-9d00-2775650dc88d.png)
* dùng tính năng search từ khóa
*Provide the MD5 hash for the dropped malicious executable.*
![image](https://user-images.githubusercontent.com/110059218/219749594-092bc593-870e-4109-b2dd-c9a6c408c64e.png)
*What is the name of the ransomware?*
* câu này đơn giản em lấy MD5 hash của nó lên gg search hoặc lấy chính đoạn đuôi của file thực thi
![image](https://user-images.githubusercontent.com/110059218/219750193-a8278eb8-fa35-439a-96d4-b0051144e719.png)
