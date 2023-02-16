#### http状态码
```
https://cloud.tencent.com/developer/article/1373924

https://cloud.tencent.com/developer/news/678417

https://developer.aliyun.com/article/311893
```
- 301
  - （永久移动） 请求的网页已永久移动到新位置。 服务器返回此响应（对 GET 或 HEAD 请求的响应）时，会自动将请求者转到新位置。
- 302
  - （临时移动） 服务器目前从不同位置的网页响应请求，但请求者应继续使用原有位置来进行以后的请求。
- 499
  - client发送请求后，如果在规定的时间内（假设超时时间为500ms）没有拿到nginx给的响应，则认为这次请求超时，会主动结束，这个时候nginx的access_log就会打印499状态码(499如果比较多的话，可能会引起服务雪崩)。
- 500
  - Internal Server Error 内部服务错误，比如脚本错误，编程语言语法错误、访问量大的时候，由于系统资源限制，而不能打开过多的文件句柄。
- 502
  - Bad Gateway错误，网关错误。比如服务器当前连接太多，响应太慢，页面素材太多、带宽慢。
- 503
  - Service Temporarily Unavailable，服务不可用，web服务器不能处理HTTP请求，可能是临时超载或者是服务器进行停机维护。
- 504
  - Gateway timeout 网关超时，程序执行时间过长导致响应超时，例如程序需要执行20秒，而nginx最大响应等待时间为10秒，这样就会出现超时。
  - 
