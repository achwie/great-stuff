# Great stuff
Helpful tools, commands and other great stuff

## Linux

Generate UUIDs:
```
$ uuidgen
d5fb8b8a-9ad1-4a9a-ae29-97f044d248b5
```

Format JSON:
```
$ echo '{"foo": "lorem", "bar": "ipsum"}' | python -m json.tool
{
    "bar": "ipsum",
    "foo": "lorem"
}
```

Show active connections:
```
$ netstat -pant
(Not all processes could be identified, non-owned process info
 will not be shown, you would have to be root to see it all.)
Active Internet connections (servers and established)
Proto Recv-Q Send-Q Local Address           Foreign Address         State       PID/Program name    
tcp        0      0 127.0.0.1:43721         0.0.0.0:*               LISTEN      -                   
tcp        0      0 127.0.0.53:53           0.0.0.0:*               LISTEN      -                   
tcp        0      0 127.0.0.1:631           0.0.0.0:*               LISTEN      -             
...
```

Check how long a command takes to run:
```
# Checks how long "find . | wc -l" takes
$ time find . | wc -l
86782

real	0m1,483s
user	0m0,110s
sys	0m0,344s
```

Find text (like grep, [just better and faster](https://beyondgrep.com/why-ack/)):
```
$ ack --java "class CartService"
microservices-shop-demo/cart/src/main/java/achwie/hystrixdemo/cart/CartService.java
13:public class CartService {

microservices-shop-demo/frontend/src/main/java/achwie/hystrixdemo/cart/CartService.java
17:public class CartService {

kafka-demo/cart/src/main/java/achwie/shop/cart/CartService.java
13:public class CartService {
...
```

Find text really, really fast (like ack, [just way faster](https://github.com/ggreer/the_silver_searcher)):
```
$ ag --java "class CartService"

microservices-shop-demo/cart/src/main/java/achwie/hystrixdemo/cart/CartService.java
13:public class CartService {

microservices-shop-demo/frontend/src/main/java/achwie/hystrixdemo/cart/CartService.java
17:public class CartService {

kafka-demo/cart/src/main/java/achwie/shop/cart/CartService.java
13:public class CartService {
...
```

Stop current task and move to background:
```
# For example, start vi. Then stop task (and put into background) by pressing [Ctrl]+[Z].
$ vi

[1]+  Stopped                 vi

# Run some command with vi in the background
$ ls -l | wc -l
16

# Bring vi to foreground again with fg
$ fg

```
