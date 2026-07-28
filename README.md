# EX01 Developing a Simple Webserver

# Date: 28/07/2026
# AIM:
To develop a simple webserver to serve html pages and display the configuration details of laptop.

# DESIGN STEPS:
## Step 1:
HTML content creation.

## Step 2:
Design of webserver workflow.

## Step 3:
Implementation using Python code.

## Step 4:
Serving the HTML pages.

## Step 5:
Testing the webserver.

# PROGRAM:
```from http.server import HTTPServer,BaseHTTPRequestHandler
content='''<html>
<h1>Hello Everyone!!</h1>
</html>'''
class Myserver(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Get request recevied...")
        self.send_response(200)
        self.send_header("content-type","text/html")
        self.end_headers()
        self.wfile.write(content.encode())
print("This is my webserver")
server_address=('',8000)
httpd=HTTPServer(server_address,Myserver)
httpd.serve_forever()
```

# OUTPUT:
![alt text](<Screenshot 2026-07-28 133748.png>)
![alt text](<Screenshot 2026-07-28 133822.png>)

# RESULT:
The program for implementing simple webserver is executed successfully.
