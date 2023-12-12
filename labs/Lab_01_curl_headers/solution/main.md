# Лабораторная работа №1
___
Запросы осуществить к источнику exam.abit.rgups.ru

> curl -Iv exam.abit.rgups.ru

Ответ получен в следующем формате:


~~~
 * processing: exam.abit.rgups.ru
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
  0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--     0*   Trying 89.16.96.110:80...
* Connected to exam.abit.rgups.ru (89.16.96.110) port 80
> HEAD / HTTP/1.1
> Host: exam.abit.rgups.ru
> User-Agent: curl/8.2.1
> Accept: */*
>
* HTTP 1.0, assume close after body
< HTTP/1.0 301 Moved Permanently
< Server: nginx
< Date: Mon, 11 Sep 2023 13:58:31 GMT
< Content-Type: text/html
< Content-Length: 162
< Location: https://exam.abit.rgups.ru/
< X-Cache: MISS from wifi-proxy
< X-Cache-Lookup: MISS from wifi-proxy:8080
< Via: 1.1 wifi-proxy:8080 (squid/2.7.STABLE9)
< Connection: close
<
  0   162    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--     0HTTP/1.0 301 Moved Permanently
Server: nginx
Date: Mon, 11 Sep 2023 13:58:31 GMT
Content-Type: text/html
Content-Length: 162
Location: https://exam.abit.rgups.ru/
X-Cache: MISS from wifi-proxy
X-Cache-Lookup: MISS from wifi-proxy:8080
Via: 1.1 wifi-proxy:8080 (squid/2.7.STABLE9)
Connection: close


* Closing connection

~~~
Описание к коду:

> curl -Iv exam.abit.rgups.ru 

`-I` - флаг, указывающий на следование перенаправлениям при запросе.

`-v` - флаг, указывающий на вывод подробной информации о запросе.

` processing: exam.abit.rgups.ru` - Получение заголовков HTTP (ключ -Iv) с exam.abit.rgups.ru

  >*0   162    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--     0HTTP/1.0 301 Moved Permanently

`HEAD / HTTP/1.1` - HTTP 1.1 вводит еще одно понятие по умолчанию, которое называется keep-alive. keep-alive означает, что соединение TCP, по которому ходит HTTP, не закрывается.

`Host: exam.abit.rgups.ru` - Host-любое устройство, предоставляющее сервисы формата «клиент-сервер» в режиме сервера по каким-либо интерфейсам и уникально определённое на этих интерфейсах.

`User-Agent: curl/8.2.1` - Строка User-Agent (UA) - это информация, включенная в заголовок HTTP, действующая от имени пользователя.

`Accept: */*` - Accept указывает, какие типы контента, выраженные как MIME типы, клиент может понять. 

>* HTTP 1.0, assume close after body

`HTTP/1.0 301 Moved Permanently` - Это строка состояния ответа, указывающая на то, что запрошенный ресурс был окончательно перемещен в новое местоположение.

`Server: nginx` - Этот заголовок указывает на сервер программного обеспечения, сгенерировавший ответ. В этом случае веб-сервер использует программное обеспечение nginx.

`Date: Mon, 11 Sep 2023 13:58:31 GMT` - Этот заголовок указывает дату и время, когда был сгенерирован ответ. В этом примере ответ был сгенерирован 11 сентября 2023 года в 13:58:31 по GMT.

`Content-Type: text/html` - Этот заголовок указывает MIME-тип содержимого в ответе. В этом случае содержимое находится в формате HTML.

`Content-Length: 162` - Этот заголовок определяет длину содержимого в байтах. В этом примере длина содержимого составляет 162 байта.

`Location: https://exam.abit.rgups.ru/` - ссылка на сайт, куда мы переходим

`X-Cache: MISS from wifi-proxy` - MISS from wifi-proxy: Этот заголовок предоставляет информацию о состоянии кэша. В этом примере это указывает на то, что ответ не был найден в кэше.

`X-Cache-Lookup: MISS from wifi-proxy:8080` - ОШИБКА с wifi-прокси:8080: Этот заголовок предоставляет дополнительную информацию о поиске в кэше. В этом примере это указывает на то, что поиск в кэше не был успешным.

`Via: 1.1 wifi-proxy:8080 (squid/2.7.STABLE9)` - via указывает источник ссылки, Wi-Fi прокси — это промежуточный сервер между вашим устройством и интернетом, который может выполнять запросы вместо вас, 8080 - порт, (squid/2.7.STABLE9) - конфиг сайта.

`Connection: close` - Connection определяет, остаётся ли сетевое соединение активным после завершения текущей транзакции (запроса)
