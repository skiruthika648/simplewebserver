# EX01 Developing a Simple Webserver
## Date: 20/09/2023

## AIM:
To develop a simple webserver to serve html pages.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Serving the HTML pages.

### Step 5:
Testing the webserver.

## PROGRAM:
```
from http.server import HTTPServer, BaseHTTPRequestHandler
content = """
<!DOCTYPE html>
<html>
<head>
<title>My webserver</title>
</head>
<body>
<h1>Top five Revenue generating Software Companies</h1>
<ol>
<li>Microsoft</li>
<li>Oracle</li>
<li>Salesforce</li>
<li>IBM</li>
<li>Intuit</li>
</ol>
</body>
</html>

class myhandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request received")
        self.send_response(200)
        self.send_header('content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address = ('',8004)
httpd = HTTPServer(server_address,myhandler)
print("my webserver is running...")
httpd.serve_forever()

```



## OUTPUT:
![kweb2](https://github.com/skiruthika648/simplewebserver/assets/128348968/19b3be90-d671-450c-81a3-770d5cdb6714)
![kweb1](https://github.com/skiruthika648/simplewebserver/assets/128348968/b548c2e1-ae28-4ce3-aa65-7b929645ef4a)


## RESULT:
The program for implementing simple webserver is executed successfully.
