### Docker
- Docker là nền tảng phần mềm cho phép bạn dựng, kiểm thử và triển khai ứng dụng một cách nhanh chóng.
- Docker đóng gói phần mềm vào các đơn vị tiêu chuẩn hóa được gọi là container có mọi thứ mà phần mềm cần để chạy, trong đó có thư viện, công cụ hệ thống, mã và thời gian chạy.
- Bằng cách sử dụng Docker, bạn có thể nhanh chóng triển khai và thay đổi quy mô ứng dụng vào bất kỳ môi trường nào và biết chắc rằng mã của bạn sẽ chạy được.
### Cách thức hoạt động
- Docker hoạt động bằng cách cung cấp phương thức tiêu chuẩn để chạy mã của bạn. 
- Docker là hệ điều hành dành cho container. 
- Cũng tương tự như cách máy ảo ảo hóa (loại bỏ nhu cầu quản lý trực tiếp) phần cứng máy chủ, các container sẽ ảo hóa hệ điều hành của máy chủ.
- Docker được cài đặt trên từng máy chủ và cung cấp các lệnh đơn giản mà bạn có thể sử dụng để dựng, khởi động hoặc dừng container
### Docker khác VM ở chỗ nào
- Docker là 1 loại công nghệ ảo hóa
- Chia sẻ tài nguyên chung với host

### Amazon ECS
LaunchType
- Launch Docker Containers on AWS = Launch ECS Tasks on ECS Cluster
+ EC2 Launch Type :
- Tự cung cấp và maintain cơ sở hạ tầng (EC2 Instance)
- Mỗi EC2 Instance sẽ chạy 1 ECS Agent để đăng ký vào ECS Cluster
- EC2 Instance Profile được dùng bởi ECS Agent thực hiện lệnh API Call tới ECS Services
- Gửi Container logs tới CloudWatch logs
- Pull Docker Image từ ECR 
+ Fargate Launch Type
- Launch Docker container trên AWS
- Ko cần tự cung cấp và maintain cơ sở hạ tầng
- Nó là Serverless, chỉ cần cung cấp tài nguyên mong muốn
- Để mở rộng chỉ cần tăng số task
### ECS Task Role 
- Cho phép mỗi Task thực hiện 1 vai trò riêng biệt cụ thể
- Mỗi role khác nhau sẽ phục vụ cho mỗi ECS Services khác nhau
- Task role được định nghĩa trong task definition
