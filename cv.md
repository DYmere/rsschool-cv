# Resume 

---

### Personal Information
First name: **Dzmitry**  
Last Name: **Yatsyna**  
Age: **28**  
Location: **Belarus, Minsk**

### Contact info

| communication method  | info                       |   
|          :---:        |           :---:            |  
| Email                 | _dy.rschool2020@gmail.com_ |  
| Phone Number          | _+37511441234666_          |  
| Skype                 | _dy.rschool2020_           |

### Objective
In search of a front-end  position where I can work with diversified and creative projects

### Work Experience

2015 — 2019 "JSSS" Com, Belarus, Minsk
*System Administrator*
+ Development, configuration and maintenance of the company's infrastructure
+ Development and support of a monitoring system.

### Education

+ [Belarusian State University of Informatics and Radioelectronics](https://bsuir.by), Master's Degree
+ [HTML academy](https://htmlacademy.ru/), Basics of HTML and CSS
+ Oracle PL/SQL course
+ English courses (Intermediate level)

### Skills
+ JavaScript
+ HTML
+ CSS
+ Python
+ Unix/Linux

### Language known
+ Belarusian
+ Russian
+ English (Intermediate level)

### Code example
```python
class ForgeHandler(BaseHTTPRequestHandler):
    """
    The handler parse the request and the headers, then call a method specific to the request type
    """
    def do_GET(self):
        """
        'GET' request serving function
        """
        global st_point, cur_request
        if time.time() - st_point < 1 and cur_request > args.MAX_REQ:
            self.send_response(429)
            self.send_header("Content-type","text/html")
            self.end_headers()
            time.sleep(0.2)
            return
        elif time.time() - st_point > 1:
            st_point = time.time()
            cur_request = 1
        self.func_PARSE()
        if self.parsed_url[2] in ["/ping", "/cats"]:
            self.func_DO()
        else:
            self.send_response(400)
            text="<h1 align=center>Bad request</h1>"
            self.func_PRINT(text)
```
