# EX01 Developing a Simple Webserver
## Date:27-03-2024

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
<html>
      <head> 
            <title>Top Software Companies Revenue</title>
      </head>
      <body>
      <table border="4" cellspacing="5" width="40" heigth="50"
        <caption>REVENUE</caption>
        <tr>
             <th>Rank</th>
             <th>company </th>
             <th>Revenue</th>
             <th>R&D spend</th>
        </tr>
        <tr>
             <td>1</td>
             <td>2U</td>
             <td>$286.8m</td>
             <td>$98m</td>
        </tr>
        <tr>
             <td>2</td>
             <td>Ellie Mae</td>
             <td>$417m</td>
             <td>$133.9m</td>
        </tr>
        <tr>
             <td>3</td>
             <td>Athenahealth</td>
             <td>$1,220.3m</td>
             <td>$310.1m</td>
        </tr>
        <tr>
             <td>4</td>
             <td>paylocity Holding</td>
             <td>$377.5m</td>
             <td>$73.9m</td>
        </tr>
        <tr>
             <td>5</td>
             <td>NantHealth</td>
             <td>$86.7m</td>
             <td>$41.2m</td>  
        </tr>
        </table>
        </body>
        </html>      

"""
class myhandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request received")
        self.send_response(200)
        self.send_header('content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address = ('',8000)
httpd = HTTPServer(server_address,myhandler)
print("my webserver is running...")
httpd.serve_forever()
```

## OUTPUT:
![alt text](<Screenshot 2024-03-17 145229.png>)
![alt text](<Screenshot 2024-03-17 145655.png>)

## RESULT:
The program for implementing simple webserver is executed successfully.
