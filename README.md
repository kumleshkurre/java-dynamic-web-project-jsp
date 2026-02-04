# 🌐 Java Dynamic Web Project (JSP & HTML)
- Eclipse + Apache Tomcat

## 📌 Project Overview
---
This project demonstrates how to create and run a Java Dynamic Web Application using Eclipse IDE, HTML, JSP, and Apache Tomcat Server.
The application takes user input from an HTML form and processes it using a JSP page.

## 🛠️ Tools & Technologies Used

- Eclipse IDE (Enterprise Java & Web Developer)
- Apache Tomcat 10
- Java (JSP)
- HTML5
- Browser (Chrome / Edge)
  
## 📂 Project Structure
```
Dynamicweb
├── Deployment Descriptor
├── JAX-WS Web Services
├── Java Resources
├── build
└── src
    └── main
        ├── java
        └── webapp
            ├── META-INF
            ├── WEB-INF
            ├── First.jsp
            └── index.html
```
## 📥 Step 1: Download Required Software
- 1️⃣ Download Eclipse IDE
- Download Eclipse IDE for Enterprise Java and Web Developers
- Official site:
👉 https://www.eclipse.org/downloads/

- 2️⃣ Download Apache Tomcat
- Download latest Apache Tomcat 10
- Official site:
👉 https://tomcat.apache.org/download-10.cgi

## 📂 Step 2: Create Dynamic Web Project
- Open Eclipse
- Go to
- File → New → Dynamic Web Project
- Enter Project Name
- Select Apache Tomcat Server
- Click Finish


## 🧾 HTML File (index.html)
- 📍 Location: src/main/webapp/index.html
```
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Java Web Page</title>
</head>
<body>
<center>
<h1>THIS IS MY JAVA WEB PAGE</h1>

<form action="First.jsp" method="get">
  Number 1: <input type="text" name="num1"><br><br>
  Number 2: <input type="text" name="num2"><br><br>
  <input type="submit" value="Add Numbers">
</form>

</center>
</body>
</html>
```

- 📌 Form ke through data server (JSP page) par submit hota hai.

## 🧾 JSP File (First.jsp)

- 📍 Location: src/main/webapp/First.jsp
```
<%@ page language="java" contentType="text/html; charset=UTF-8"
    pageEncoding="UTF-8"%>
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>JSP Result</title>
</head>
<body>
<center>
<h1>This is JSP Page</h1>

<%
int num1 = Integer.parseInt(request.getParameter("num1"));
int num2 = Integer.parseInt(request.getParameter("num2"));
int result = num1 + num2;

out.print("<h2>Addition is = " + result + "</h2>");
%>

</center>
</body>
</html>
```
- 📌 JSP page client se aane wali request ko read karta hai aur result generate karta hai.
## ➕ Second Program: Square Calculation (HTML + JSP)
### 🧾 HTML File – Square Program (square.html)
- 📍 Location: src/main/webapp/square.html

```
  <!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Square Program</title>
</head>
<body>
<center>
<h1>THIS IS MY JAVA WEB PAGE</h1>

<form action="Square.jsp" method="get">
  Number: <input type="text" name="num">
  <input type="submit" value="Get Square">
</form>

</center>
</body>
</html>
```
- 📌 User ka input JSP page par request ke form me send hota hai.

 ## 🧾 JSP File – Square Logic (Square.jsp)
- 📍 Location: src/main/webapp/Square.jsp
```
  <%@ page language="java" contentType="text/html; charset=UTF-8"
    pageEncoding="UTF-8"%>
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Square Result</title>
</head>
<body>
<center>
<h1>This is JSP Page</h1>

<%
int n = Integer.parseInt(request.getParameter("num"));
int sqr = n * n;

out.print("<h1>Square = " + sqr + "</h1>");
%>

</center>
</body>
</html>
```
## ▶️ How to Run the Project
- Right-click on the project
- Select Run As → Run on Server
- Choose Apache Tomcat
- Click Finish
- Project browser me open ho jayega 🎉

## ✅ Output
- User numbers enter karta hai
- JSP page addition calculate karta hai
- Result browser par show hota hai

## 🎯 Learning Outcome
- Eclipse me Dynamic Web Project banana
- HTML se JSP ko data pass karna
- JSP me request parameters handle karna
- Apache Tomcat server configuration

## 📌 Author

Kumlesh Kurre
💼 Java | JSP | Web Development
📁 GitHub Projects for Learning & Practice
