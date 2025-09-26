# Simple Web Server

In todays lecture we learnt how to deploy a simple web server on linux system using bash.

```bash
#!/bin/bash

while true; do echo -e "HTTP/1.1 200 OK\n\n $(date)" | nc -l localhost 1500; done

```
Here we are making a simple server

```shell
 @hypruser  curl -v http://localhost:1500
* Host localhost:1500 was resolved.
* IPv6: ::1
* IPv4: 127.0.0.1
*   Trying [::1]:1500... # Just indicating the connection is local
* Connected to localhost (::1) port 1500 # In which port it's connecting
* using HTTP/1.x # The protocol being used to fetch
> GET / HTTP/1.1 # The protocol being fetched
> Host: localhost:1500 # Host name
> User-Agent: curl/8.14.0 # Agent info
> Accept: */* # Baically taking all the root files so full system
> 
< HTTP/1.1 200 OK # The work was done is being sent out
* no chunk, no close, no size. Assume close to signal end
< 
 Thu Sep  4 02:38:36 AM IST 2025 # The output.Q
* Request completely sent off
```
