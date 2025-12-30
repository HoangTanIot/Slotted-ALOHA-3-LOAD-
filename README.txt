Aloha
=====

This model makes it possible to measure the efficiency of the Aloha and
slotted Aloha protocols. The model is similar to the original University
of Hawaii radio network: "hosts" talk to a central "server" via a shared
radio channel. In this model we're only interested in the achievable channel
utilization, so we ignore the "downstream" link (TDM broadcast from
the server) and retransmissions.

Hosts transmit according to Poisson process. The protocol choice (slotted or
"pure" Aloha) is encode in the slotTime parameter of the host model --
if a nonzero slotTime is given, transmissions are aligned to the next slot
boundary.

The model of the central server checks for collisions and computes statistics.
The internal state of the server and all statistics are visible in the GUI
The most important statistics is channel utilization. It is also recorded in
omnetpp.vec, and can be plotted using the Analysis Tool in the IDE.

The supplied omnetpp.ini file contains 6 predefined configurations:
- pure Aloha at high load
- pure Aloha at moderate load (utilization =~ max)
- pure Aloha at low load
- slotted Aloha at high load
- slotted Aloha at moderate load (utilization =~ max)
- slotted Aloha at low load

In addition, it also contains a predefined parameter study called
PureAlohaExperiment, which explores the channel utilization in the
function of the number of hosts and the packet generation frequency.

According to some descriptions of the Aloha protocol, hosts have to listen
on the channel before they start to transmit anything. This "listen before
talk" behavior is not part of the current model. (One reason is that with
the radio nodes scattered around, the propagation delays of radio signals
are different for every host pair, and it becomes very complex to accurately
model whether any host can hear any transmission at any given moment.)
Aloha

Mô hình này cho phép đo hiệu suất của các giao thức Aloha và Slotted Aloha.
Mô hình tương tự mạng vô tuyến ban đầu của Đại học Hawaii: các host giao tiếp với một server trung tâm thông qua một kênh vô tuyến dùng chung.

Trong mô hình này, chúng ta chỉ quan tâm đến mức độ sử dụng kênh truyền đạt được, vì vậy bỏ qua liên kết “downstream” (phát quảng bá TDM từ server) và các lần truyền lại (retransmission).

Các host truyền dữ liệu theo quá trình Poisson.
Việc lựa chọn giao thức (Slotted hay “Pure” Aloha) được mã hóa thông qua tham số slotTime của mô hình host — nếu slotTime ≠ 0, các lần truyền sẽ được căn chỉnh theo ranh giới của các khe thời gian (slot).

Mô hình server trung tâm sẽ kiểm tra va chạm và tính toán các thống kê.
Trạng thái nội bộ của server và tất cả các thống kê đều hiển thị trong GUI.
Thống kê quan trọng nhất là mức độ sử dụng kênh truyền (channel utilization).
Giá trị này cũng được ghi vào file omnetpp.vec và có thể vẽ đồ thị bằng Analysis Tool trong IDE.

File omnetpp.ini đi kèm chứa 6 cấu hình định nghĩa sẵn:

Pure Aloha với tải cao

Pure Aloha với tải trung bình (hiệu suất xấp xỉ cực đại)

Pure Aloha với tải thấp

Slotted Aloha với tải cao

Slotted Aloha với tải trung bình (hiệu suất xấp xỉ cực đại)

Slotted Aloha với tải thấp

Ngoài ra, file còn chứa một nghiên cứu tham số (parameter study) định nghĩa sẵn tên là PureAlohaExperiment, nhằm khảo sát mức độ sử dụng kênh truyền theo số lượng host và tần suất sinh gói tin.

Theo một số mô tả về giao thức Aloha, các host phải nghe kênh truyền trước khi bắt đầu truyền dữ liệu.
Hành vi “nghe trước khi nói” này không được đưa vào mô hình hiện tại.
(Một lý do là do các node vô tuyến nằm rải rác, nên độ trễ lan truyền tín hiệu giữa mỗi cặp host là khác nhau, khiến việc mô phỏng chính xác khả năng một host có thể nghe được một truyền nào đó tại một thời điểm bất kỳ trở nên rất phức tạp.)

