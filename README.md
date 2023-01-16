# Developing a Simple Webserver

# AIM:
Name:Deepesh P
Refernce Number:22008539


# DESIGN STEPS:

## Step 1:

HTML content creation is done

## Step 2:

Design of webserver workflow

## Step 3:

Implementation using Python code

## Step 4:

Serving the HTML pages.

## Step 5:

Testing the webserver

# PROGRAM:
```
from http.server import HTTPServer, BaseHTTPRequestHandler

content = """
<html>
<head>
</head>
<body>
<h1>Welcome</h1>
<p> django - python </p>
<p> laravel - php</p>
<p> React - Javascript</p> 
</body>
</html>
"""

class HelloHandler(BaseHTTPRequestHandler):
    def do_GET(self):
      self .send_response(200)
      self.send_header('Content_type', 'text/html; charset=utf-8')
      self.end_headers()
      self.wfile.write(content.encode())


server_address = ('', 80)
httpd = HTTPServer(server_address,HelloHandler)
httpd.serve_forever()
```


# OUTPUT:
![OUTPUT](./Image/Output.png)

# RESULT:

The program is executed succesfully.
