# EX01 Developing a Simple Webserver

# Date:
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
content="""
<html>
<title>Top Sofware Indusries</title>
<body>
<table border="2" cellspacing="10"sellpadding="6"
<caption>Top 5 Revenue Generating Software Companies </caption>
<tr>
<th>s.no</th>
<th>companies</th>
<th>revenue</th>
</tr>
<tr>
<th>1</th>
<th>microsoft</th>
<th>65 billion</th>
</tr>
<tr>
<th>2</th>
<th>IBM</th>
<th>29.1 billion</th>
</tr>
<tr>
<th>3</th>
<th>oracle</th>
<th>29.6 billion</th>
</tr>
<tr>
<th>4</th>
<th>sap</th>
<th>6.4 billion</th>
</tr>
<tr>
<th>5</th>
<th>symentec</th>
<th>5.6 bilion</th>
</tr>
</body>
</html>
"""
class myhandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("reqest received")
        self.send_response(200)
        self.send_header('sontent-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address=('',8000)
httpd = HTTPServer(server_address,myhandler)
print("m webserver is running...")
httpd.serve_forever()
```
# OUTPUT:
![Screenshot 2025-03-25 135837](https://github.com/user-attachments/assets/06f507dd-f8b4-4872-a225-253fee53a3db)
![Screenshot 2025-03-25 135731](https://github.com/user-attachments/assets/a06d987d-b123-42ca-9576-561459c4759e)

# RESULT:
The program for implementing simple webserver is executed successfully.
