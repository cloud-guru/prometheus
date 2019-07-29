# Hiện trạng
Hiện tại, có nhiều cách giám sát cloud trên nền openstack, như collectd, zabbix, TICK và Telemetry. Các cách giám sát gặp phải một số hạn chế như: TICK có phần cảnh báo chưa tốt, không triển khai được HA, telemetry được cộng đồng đánh giám không cao do hiệu năng kém và cảnh báo khó dùng. Nghiên cứu này sẽ tìm hiểu sử dụng prometheus nhằm giám sát cho môi trường Cloud cho cả về tài nguyên vật lý và ảo hóa.

# Đối tượng giám sát 
* Cloud control plane
* Cloud backend service: mysql, ceph, rabbit, memache, apache.
* Cloud instance libvirt.

# Giới thiệu prometheus 
Prometheus là bộ công cụ giám sát hệ thống mã nguồn mở. Bắt đầu thành lập từ 2012 bởi Sound Cloud, hiện đã được chuyển giao cho Cloud Native Computing Foundation (CNCF) - trở thành một dự án mã nguồn mở độc lập, với tư cách là dự án được ưu tiên phát triển lớn thứ 2, chỉ sau Kubernetes . Hiện tại được rất nhiều công ty, tổ chức áp dụng và có một cộng đồng hỗ trợ mạnh.

# Bố cục 

* Kiến trúc : các khái niệm và các thành phần của prometheus.
* Khởi động: giới thiệu cài đặt thử nghiệm. 
* Thu thập dữ liệu: lấy dữ liệu giám sát cho prometheus, đặc biệt dùng cho nhiệm vụ giám sát cloud
* Lưu trữ dữ liệu: thiết lập mô hình lưu trữ các dữ liệu giám sát trên.
* Truy vấn và cảnh báo: giới thiệu cách thức truy vấn dữ liệu, cấu hình của thành phần cảnh báo
* Kịch bản sử dụng: các ca sử dụng với hệ thống , ví dụ như xem đồ thị giám sát, đặt cảnh báo .
* Kiến trúc triển khai: mô hình bố trí các thành phần, đảm bảo HA
* Hướng dẫn cài đặt: cài đặt hệ thống HA bằng ansible, docker
* Kết luận: ưu, nhược điểm và các so sánh với hệ thống khác.

 

