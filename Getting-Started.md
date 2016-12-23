### Setup

* Install Eclipse
* Install Tomcat using the link  
  * http://crunchify.com/step-by-step-guide-to-setup-and-install-apache-tomcat-server-in-eclipse-development-environment-ide/
  * Tomcat provides a webserver envirnoment for your Java code to run in
* New -> Dynamic Web Project  
  * Pick your project name, and select the version of Apache Tomcat you want in Target runtime
 
### Servlet
* Java servlet is a Java class that serves up HTML to a browser
* Expand the project, Right click resources -> New -> Servlet  
* Specify class name and the Java package  
* Inside the doGet method of the HelloWorld class write this code

```java
PrintWriter out = response.getWriter();
out.println("<html>");
out.println("<b>Hello World</b>");
out.println("</html>");
```

* Click Run, select the Tomcat server
  * This will create an instance of Tomcat server  
  * When you go to a url in the browser that corresponds to the servlet in the browser  
  * It will send back the html inside the doGet method  
* You can open the url in the Chrome browser as well

### Java Server Page - JSP

* A JSP is an HTML page but you can embed Java in it
* Looks similar to an html page but has additional stuff at the top
* Tomcat compiles the JSP into a servlet

Right click webcontent folder -> New -> HTML Page

```java
<%
//Write Java code in here
//Use semi colon
out.println(text); //Can use this to print out
%>

<%=
"Used to output stuff to the html page"
//Has access to the variables defined in the block above
%>
```
