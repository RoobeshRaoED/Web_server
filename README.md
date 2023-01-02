# Developing a Simple Webserver

# AIM:

Name:Roobesh Rao.E.D , Ref.No:22008573

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
<h1>Welcome to my first web page</h1>
<h2>Name:Roobesh Rao.E.D</h2>
<h3>Ref.no:22008573</h3>
<p>
<img src ="https://static.djangoproject.com/img/logos/django-logo-negative.1d528e2cb5fb.png" style="width:200px;height:100px">
</p>
</body>
</html>
"""
class HelloHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        self.send_response(200)
        self.send_header('Content-type',"text/html; charset=utf-8")
        self.end_headers()
        self.wfile.write(content.encode())

server_address = ('',80)
httpd = HTTPServer(server_address, HelloHandler)
httpd.serve_forever()
```

# OUTPUT:

[Roobesh Rao.E.D 22008573 simple webserver.pdf](https://github.com/RoobeshRaoED/Web_server/files/10330103/Roobesh.Rao.E.D.22008573.simple.webserver.pdf)

![R](op.png)


# RESULT:

The program is executed succesfully
