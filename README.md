# Developing a Simple Webserver

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

HTML content creation is done

### Step 2:

Design of webserver workflow

### Step 3:

Implementation using Python code

### Step 4:

Serving the HTML pages.

### Step 5:

Testing the webserver

## PROGRAM:
```html
from http.server import HTTPServer,BaseHTTPRequestHandler

content='''
<!doctype html>
<html>
<head>
<title> My Web Server</title>
</head>
<body>
<h1>Top Five Web Application Development frame works</h1>
<h2>1.Django</h2>
<h2>2.MEAN Stack</h2>
<h2>3.React
</h2>
</body>
</html>
'''

class MyServer(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Get request received...")
        self.send_response(200) 
        self.send_header("content-type", "text/html")       
        self.end_headers()
        self.wfile.write(content.encode())

print("This is my webserver") 
server_address =('',80)
httpd = HTTPServer(server_address,MyServer)
httpd.serve_forever()

```

## OUTPUT:

### CLIENT OUTPUT

![275313158-7fdd471c-7ae8-480d-aa4a-276224b8bbf9](https://github.com/rajeshsmaha/webserver/assets/147608800/d4c33262-0d4e-410f-82f9-301ccfb8debc)


### SERVER OUTPUT
![275313231-17cd4411-92fc-4676-93de-4dd4e2749b4e](https://github.com/rajeshsmaha/webserver/assets/147608800/89761c8a-9fe1-443b-b5c6-cfcfe5e4fb69)




## RESULT:
The program is executed succesfully
