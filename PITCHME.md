## Lunch And Learn - How to Hack
### Agenda 
---
* Types of Hacking
* More detail on Cross-site scripting (XSS)
* XSS Interactive game/workshop
---
### WARNING
Anything you learn today should never be used without explicit permission. Do NOT use any of the techniques on applications you are not authorized to test.
---
### Why is hacking so common
* Applications are not built with security in mind
* Developers/Managers are focused on delivering business value
* Developers are not trained in application security
---
### OWASP
 * OWASP is an open community dedicated to enabling organizations to conceive, develop, acquire, operate, and maintain applications that can be trusted.
 * All of the OWASP tools, documents, forums, and chapters are free and open to anyone interested in improving application security. 
 * We advocate approaching application security as a people, process, and technology problem because the most effective approaches to application security include improvements in all of these areas. 
---
### OWASP Top Ten
 1 Injection
 2 Broken Authentication and Session Management
 3 Cross-Site Scripting (XSS)
 4 Broken Access Control (As it was in 2004)
 5 Security Misconfiguration
 6 Sensitive Data Exposure
 7 Insufficient Attack Protection (NEW)
 8 Cross-Site Request Forgery (CSRF)
 9 Using Components with Known Vulnerabilities
 10 Underprotected APIs (NEW)
---
### Cross-Site Scripting (XSS)
* Injecting Browser-side code into an application
* Malicious code is used on unsuspecting users of the application without even knowing it
* The malicious content sent to the web browser often takes the form of a segment of JavaScript, but may also include HTML, Flash, or any other type of code that the browser may execute. The variety of attacks based on XSS is almost limitless, but they commonly include transmitting private data, like cookies or other session information, to the attacker, redirecting the victim to web content controlled by the attacker, or performing other malicious operations on the user's machine under the guise of the vulnerable site.
* Types
..* [Stored](https://www.owasp.org/index.php/Testing_for_Stored_Cross_site_scripting_(OTG-INPVAL-002))
..* [Reflective](https://www.owasp.org/index.php/Testing_for_Reflected_Cross_site_scripting_(OTG-INPVAL-001))
..* [DOM Based](https://www.owasp.org/index.php/DOM_Based_XSS)
---
### Stored XSS
Stored XSS occurs when a web application gathers input from a user which might be malicious, and then stores that input in a data store for later use. 
The input that is stored is not correctly filtered. As a consequence, the malicious data will appear to be part of the web site and run within the user’s browser under the privileges of the web application.
* Hijacking another user's browser
* Capturing sensitive information viewed by application users
* Pseudo defacement of the application
* Port scanning of internal hosts ("internal" in relation to the users of the web application)
* Directed delivery of browser-based exploits
* Other malicious activities
---
### Reflective XSS
Reflective XSS occurs when an attacker injects browser executable code within a single HTTP response. The injected attack is not stored within the application itself; it is non-persistent and only impacts users who open a maliciously crafted link or third-party web page. The attack string is included as part of the crafted URI or HTTP parameters, improperly processed by the application, and returned to the victim.
---
### Examples
Blog posts, comments on blogs, forum posts are all examples of where malicious code can be stored (Stored). URLs are useful when doing Reflective XSS, if there is a vulnerability in the URL it can be changed, shortened and emailed to a victim.
+++ 

+++
