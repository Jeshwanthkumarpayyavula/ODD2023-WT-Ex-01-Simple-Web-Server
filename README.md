# Ex-01-Simple-Web-Server
## Name:Jeshwanth Kumar
## Ref.No:23002519
## Date:15/11/2023

## AIM:
To develop a simple webserver to serve html pages.The Top five web application frameworks

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
<html>
<head>
<title>Top Five Web Application Development Frameworks</title>
</head>
<body>
<h1>1.Django</h1>
<h1>2.MEAN Stack</h1>
<h1>3.React<h1>
<h1>4.Ruby on rails<h1>
<h1>5.Angular<h1>
</body>
</html>
"""

class HelloHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        self.send_response(200)
        self.send_header('Content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())

server_address = ('', 80)
httpd = HTTPServer(server_address, HelloHandler)
httpd.serve_forever()

```


## OUTPUT:
![image](https://github.com/Jeshwanthkumarpayyavula/ODD2023-WT-Ex-01-Simple-Web-Server/assets/145742402/346c04f0-405c-403f-a92d-cc7f9eb4c6ca)



## RESULT:
The program for implementing simple webserver is executed successfully.
