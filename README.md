# toy-http
lightweight embeddable http server.  
Supported requests: GET, HEAD  
You can easily embed the http server as a thread to your applications
It is only designed for unix (linux, macOSX, freebsd and other OS with posix programming environment).

# install the standalone server
You can use it as lightweight server. Only clone this repository and
type in: `./install`.  
Try `toy-http` to run the server in the actual directory.  
For more advanced usage you need 3 arguments in the console:  
1. Port (numeric)  
2. Max. Connections at once (numeric)  
3. Source directory (path)  
example: `toy-http 8080 300 /var/www` 

# embed it!
You can embed it into your applications, simply add `service.h` and `service.c` to your project
and use this function: ` int serve(int http_port, int max_connections, char *serve_directory);`.  
`max_connections` is the maximum number of clients that can be connected at once.  
`serve_directory` is the folder with the ressources and files that are hosted.

# dependencies
It depends only on the std. library of C, a good C compiler and the posix programming interface.

# licensing
All distributed under GNU AGPL v3 (or later) Copyright 2015 Lukas Himsel
