# fundamentals-vnx
## Bảng

| Cột 1 | Cột 2 | Cột 3 |
| --- | --- | --- |
| Giá trị 1 | Giá trị 2 | Giá trị 3 |
| Giá trị 4 | Giá trị 5 | Giá trị 6 |
| Giá trị 1 | Giá trị 2 | Giá trị 3 |
| Giá trị 4 | Giá trị 5 | Giá trị 6 |
| Giá trị 1 | Giá trị 2 | Giá trị 3 |
| Giá trị 4 | Giá trị 5 | Giá trị 6 |

## Gắn thẻ người dùng

Hãy chào @username!

## Biểu tượng cảm xúc

Tôi rất :grinning: khi sử dụng Markdown trên GitHub!

*innghieng*

**in dam**

***in nghienva in dam***

~~gach giua~~

code inline `sieu dep` ne

> # trich dan sieu cap
>
> Trich dan thu cap

>## Trich dan sieu cap 2

> Trich dan `thu cap` 2 


>### Trich dan sieu cap 3
>
> `Trich dan` thu cap 3


```
1. cap1
 
2. cap2

3. cap3

  3.1 cap 3.1

```


```py

print("format code")
```



@@@@@@@@@@@@@@@@

@@@@@@@@@@@@@@@@


SSL

SSL là gì ?

Có bao nhiêu cách chứng thực SSL ?

CSR file dùng làm gì trong quá trình tạo SSL

Sử dụng OpenSSL để gen file CSR sau đó request SSL cho domain tech.training.vietnix.tech

Pem file là gì ?

Private key ssl là gì ?

PFX file là gì ? Cách chuyển từ file crt file sang PFX file.

1. SSL (Secure Sockets Layer) là một giao thức bảo mật được sử dụng để tạo kết nối an toàn giữa trình duyệt web và máy chủ web. Nó mã hóa dữ liệu truyền giữa client và server, đảm bảo rằng thông tin không bị đánh cắp hoặc can thiệp bởi bên thứ ba.

2. Có 2 cách chứng thực SSL chính:
   - Chứng thực bởi Tổ chức Chứng nhận (Certificate Authority - CA): Các tổ chức như Let's Encrypt, DigiCert, GoDaddy, v.v. cung cấp và quản lý các chứng chỉ SSL.
   - Chứng thực sử dụng chứng chỉ tự ký (self-signed certificate): Người dùng tự tạo và ký chứng chỉ SSL cho miền của mình.

3. CSR (Certificate Signing Request) file là một yêu cầu gửi đến Tổ chức Chứng nhận để nhận được một chứng chỉ SSL hợp lệ. Nó chứa thông tin về máy chủ, tên miền và thông tin xác thực khác mà CA sẽ sử dụng để cấp chứng chỉ.

4. Để tạo CSR file sử dụng OpenSSL cho domain tech.training.vietnix.tech, bạn có thể sử dụng lệnh sau:

   ```
   openssl req -new -newkey rsa:2048 -nodes -keyout tech.training.vietnix.tech.key -out tech.training.vietnix.tech.csr
   ```

   Sau đó, bạn có thể gửi file CSR (tech.training.vietnix.tech.csr) đến CA để yêu cầu cấp chứng chỉ SSL.

5. PEM file là một định dạng mã hóa chứng chỉ SSL. Nó có thể chứa chứng chỉ công khai, khóa riêng tư hoặc cả hai. PEM file thường được nhận dạng bởi phần mở rộng ".crt" hoặc ".pem".

6. Private key SSL là một phần không thể thiếu của chứng chỉ SSL. Nó được sử dụng để mã hóa và giải mã dữ liệu được truyền giữa trình duyệt và máy chủ. Private key phải được giữ an toàn và không được chia sẻ với bất kỳ ai khác.

7. PFX (Personal Information Exchange) file là một định dạng tập tin chứa chứng chỉ SSL và khóa riêng tư trong một tập tin duy nhất. Nó thường được sử dụng trong các ứng dụng Windows. Để chuyển từ file CRT sang PFX, bạn có thể sử dụng lệnh sau:

   ```
   openssl pkcs12 -export -in tech.training.vietnix.tech.crt -inkey tech.training.vietnix.tech.key -out tech.training.vietnix.tech.pfx
   ```

   Lệnh này sẽ tạo ra file PFX có tên `tech.training.vietnix.tech.pfx` từ file CRT và Private Key.

   
Domain

Domain là gì ?
Các trạng thái của domain
Subdomain là gì?
Virtual Hosts là gì?

1. Domain (tên miền) là một địa chỉ trên internet dùng để định danh một website hoặc dịch vụ trực tuyến. Nó giúp người dùng dễ dàng truy cập và nhớ địa chỉ của website thay vì sử dụng địa chỉ IP.

2. Các trạng thái phổ biến của một domain:
   - Registered (đã đăng ký): Domain đã được đăng ký và thuộc về chủ sở hữu.
   - Available (còn trống): Domain chưa được đăng ký và có thể được đăng ký.
   - Expired (đã hết hạn): Domain đã hết hạn và cần được gia hạn để tránh bị mất.
   - Pending Delete (chờ xóa): Domain đang trong quá trình bị xóa sau khi hết hạn.

3. Subdomain là một phần của domain chính, được sử dụng để tổ chức và phân chia nội dung. Ví dụ: `www.example.com` là subdomain của `example.com`.

4. Virtual Hosts là một tính năng của web server cho phép chạy nhiều website trên cùng một địa chỉ IP. Điều này giúp tối ưu hóa việc sử dụng tài nguyên máy chủ và quản lý nhiều website cùng lúc.

   
Mail Server

Tìm hiểu MX Record

Tìm hiểu DKIM, SPF, PTR

1. MX Record (Mail eXchange Record):
   - MX record chỉ định mail server nào sẽ nhận và xử lý email gửi đến domain.
   - Khi email được gửi đến một domain, mail server sẽ kiểm tra MX record để xác định nơi sẽ nhận và xử lý email.
   - MX record có thể chỉ định một hoặc nhiều mail server, mỗi server được gán một ưu tiên (priority).

2. DKIM (DomainKeys Identified Mail):
   - DKIM là một phương pháp xác thực email, cho phép chủ domain ký số các email được gửi đi.
   - Khi email được gửi, DKIM sẽ thêm chữ ký số vào header của email.
   - Khi email được nhận, mail server sẽ xác thực chữ ký số này để đảm bảo email thực sự được gửi từ domain đó.
   - DKIM giúp ngăn chặn các cuộc tấn công spoofing (giả mạo) email.

3. SPF (Sender Policy Framework):
   - SPF là một bản ghi DNS cho phép domain chủ sở hữu xác định những máy chủ nào được phép gửi email từ tên miền đó.
   - Khi email được gửi đến một domain, mail server sẽ kiểm tra SPF record để xác định xem email có được gửi từ một máy chủ hợp lệ hay không.
   - SPF giúp ngăn chặn các cuộc tấn công spoofing email.

4. PTR Record (Pointer Record):
   - PTR record được sử dụng để ánh xạ địa chỉ IP thành tên miền.
   - Khi một email được gửi đến, mail server sẽ kiểm tra PTR record để xác định tên miền tương ứng với địa chỉ IP của máy chủ gửi email.
   - PTR record giúp xác thực danh tính của người gửi email và chống lại các cuộc tấn công spoofing.

Tóm lại, MX, DKIM, SPF và PTR record là các công cụ quan trọng để bảo vệ email khỏi các cuộc tấn công và xác thực danh tính của người gửi.


DNS

DNS là gì ?

Các loại recored DNS

Nguyên tắc làm việc của DNS

Cách phân giải địa chỉ DNS

1. DNS (Domain Name System):
   - DNS là một hệ thống phân cấp dùng để ánh xạ tên miền (domain name) sang địa chỉ IP.
   - Nó giúp người dùng truy cập website bằng tên miền dễ nhớ thay vì phải sử dụng địa chỉ IP khó nhớ.

2. Các loại record DNS:
   - A record: Ánh xạ tên miền sang địa chỉ IPv4.
   - AAAA record: Ánh xạ tên miền sang địa chỉ IPv6.
   - CNAME record: Tạo bí danh (alias) cho một tên miền.
   - MX record: Chỉ định mail server nào sẽ nhận email gửi đến domain.
   - NS record: Chỉ định server tên miền nào quản lý một domain.
   - PTR record: Ánh xạ địa chỉ IP sang tên miền.

3. Nguyên tắc hoạt động của DNS:
   - Khi người dùng truy cập một website bằng tên miền, trình duyệt sẽ gửi yêu cầu đến DNS server.
   - DNS server sẽ tra cứu các record DNS để tìm ra địa chỉ IP tương ứng với tên miền.
   - Trình duyệt sẽ sử dụng địa chỉ IP này để thiết lập kết nối với web server.

4. Cách phân giải địa chỉ DNS:
   - Trình duyệt sẽ kiểm tra bộ nhớ cache DNS cục bộ trước.
   - Nếu không tìm thấy, trình duyệt sẽ gửi yêu cầu đến DNS server cấp cao hơn (như DNS server của ISP).
   - Các DNS server sẽ lần lượt tra cứu các record DNS để tìm ra địa chỉ IP cuối cùng.
   - Kết quả được trả về cho trình duyệt để thiết lập kết nối.

Tóm lại, DNS là hệ thống cung cấp dịch vụ ánh xạ tên miền sang địa chỉ IP, giúp người dùng truy cập website dễ dàng hơn.
