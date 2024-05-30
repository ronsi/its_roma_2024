$ docker build -t myhttpd:1.0 .
$ docker run -dit --name my-running-app -p 8080:80 myhttpd:1.0
$curl http://localhost:8080


$ netstat -natp | grep LISTEN
(Not all processes could be identified, non-owned process info
 will not be shown, you would have to be root to see it all.)
tcp        0      0 0.0.0.0:8080            0.0.0.0:*               LISTEN      -                   
tcp        0      0 127.0.0.1:631           0.0.0.0:*               LISTEN      -                   
tcp        0      0 127.0.0.53:53           0.0.0.0:*               LISTEN      -                   
tcp        0      0 127.0.0.54:53           0.0.0.0:*               LISTEN      - 

tcp6       0      0 :::8080                 :::*                    LISTEN      -               
tcp6       0      0 ::1:631                 :::*                    LISTEN      -                   

