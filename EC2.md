# EC2 (Elastic Compute Cloud)
## EC2 User Data
- That script is only run once at the instance first start
- EC2 user data is used to automate boot tasks such as install update,software
- EC2 User Data Script runs with the root user
## Instance Type

 ![image](https://github.com/nacdanh98/Yang-AWS/assets/49748262/afeb8596-5f62-429d-a0c9-295128fbd911)
### General Purpose
- Balance between: (Compute, Memory, Networking)
- Thích hợp để chạy web server và code repository
- Một số dòng đại diện gồm :
![image](https://github.com/nacdanh98/Yang-AWS/assets/49748262/5995f885-70b7-43b2-a409-f7169f3dfc83)
### Compute Optimized 
( high performance processors )
- Batch processing workloads
- Media transcoding
- High performance web servers
- High performance computing (HPC)
- Scientific modeling & machine learning
- Dedicated gaming servers
![image](https://github.com/nacdanh98/Yang-AWS/assets/49748262/f30999cc-7415-4762-ba59-ecfe32bb0695)
### Memory Optimized
Fast performance for workloads that process large data sets in memory
- High performance, relational/non-relational databases
- Distributed web scale cache stores
- In-memory databases optimized for BI (business intelligence)
- Applications performing real-time processing of big unstructured data
![image](https://github.com/nacdanh98/Yang-AWS/assets/49748262/c174b77f-14ca-4974-9b4d-45747f5c5bf5)
### Storage Optimized
Great for storage-intensive tasks that require high, sequential read and write
access to large data sets on local storage
- High frequency online transaction processing (OLTP) systems
- Relational & NoSQL databases
- Cache for in-memory databases (for example, Redis)
- Data warehousing applications
- Distributed file systems
![image](https://github.com/nacdanh98/Yang-AWS/assets/49748262/f22eaa0d-7470-4a63-9531-767d1319886f)
## Purchasing Options
- On-Demand Instances : chi phí cao nhất, dùng bao nhiêu tính tiền bấy nhiêu(theo giây), không trả trước
=> Dùng trong khoảng thới gian ngắn ko muốn gián đoạn và chưa định hình được máy sẽ như thế nào
- Reserved Instances : giá có thể giảm tối đa 72% so với On-Demand , thời hạn từ 1(24%) đến 3 năm (72%), có thể trả sau,trả trước 1 phần hoặc trả toàn bộ
=> thích hợp dùng cho các ứng dụng chạy ổn định như database ,có thể mua bán Reserved Instance trên chợ
- Convertible Reserved Instance : Có thể thay đổi EC2 instance type, instance family, OS, scope and tenancy và giảm tối đa lên đến 66%
- Savings Plans : Nhận giảm giá nếu sử dụng lâu lên đến 72% ,giảm 10$/h khi cam kết sử dụng 1 loại hình nhất định,nếu mức sự dụng vượt quá saving plans sẽ bị tính phí như On-Demand 
=> Không thể thay đổi dòng instance và region nhưng được thay đổi instance size ,os, Tenancy 
- Spot Instacnce : có thể giám chi phí tới 90% nhưng đổi lại có thể mất instance bất cứ lúc nào nếu giá tối đa thấp hơn vs giá của instance hiện tại
=> thích hợp cho Batch jobs, data analysis, image processing, any distributed workloads, workloads with a flexible start and end time
- Dedicated Hosts : Server vật lý, giải quyết các yêu cầu và tuân thủ về  software licenses, chi phí có thể chọn như Ondemand và reserved instance
=> áp dụng cho mô hình BYOL hoặc các công ty cần quy định tuân thủ chặt chẽ 
- Dedicated Instances : instance chạy trên phần cứng ,có thể share phần cứng với cùng 1 acc, ko kiểm soát vị trí nơi đặt
- Capacity Reservations : 
