# Network Questions

* [Difference between GET & POST?](#difference-between-get-&-post)
* [HTTP status codes?](#http-status-codes)
* [Web service?](#web-service)
* [OSI model?](#osi-model)
* [TCP/IP?](#tcp/ip)
* [HTTP Request methods?](#http-request-methods)
* [HTTPS negotiation steps?](#http-negotiation-steps)
* [What is CORS? ](#what-is-cors )
* [REST?](#rest)
* [Web API?](#web-api)

### Difference between GET & POST?

REST asks developers to use HTTP methods explicitly and in a way that's consistent with the protocol definition. This basic REST design principle establishes a one-to-one mapping between create, read, update, and delete (CRUD) operations and HTTP methods. According to this mapping:
- To create a resource on the server, use POST.
- To retrieve a resource, use GET.
- To change the state of a resource or to update it, use PUT.
- To remove or delete a resource, use DELETE.

###### Reference
* https://stackoverflow.com/questions/3477333/what-is-the-difference-between-post-and-get

[[↑] Back to top](#network-questions)


### HTTP status codes?
-	Temporary response(1XX)
-	Success(2XX)
-	Redirecting(3XX)
-	Response error(4XX)
-	Server error(5XX)

###### Reference
* https://en.wikipedia.org/wiki/List_of_HTTP_status_codes

[[↑] Back to top](#network-questions)


### Web service?
a service between two device via www use  particular technology(HTTP), transferring machine-readable file (JSON/XML), web-based interface to a database server

###### Reference
* https://en.wikipedia.org/wiki/Web_service

[[↑] Back to top](#network-questions)


### OSI model?
-	Application
-	Presentation
-	Session
-	Transport
-	Network
-	Data link
-	Physical

###### Reference
* https://en.wikipedia.org/wiki/OSI_model

[[↑] Back to top](#network-questions)


### TCP/IP?
Transport layer end-to-end data communication specifying how data should be packetized, addressed, transmitted, routed, and received.

###### Reference
* https://en.wikipedia.org/wiki/Internet_protocol_suite

[[↑] Back to top](#network-questions)


### HTTP Request methods?
application protocol define exchange or transfer of the hypertext, how data communicate.
request–response protocol in the client–server computing model
1) **GET**:- Used when the client is requesting a resource on the Web server.
2) **HEAD**:- Used when the client is requesting some information about a resource but not requesting the resource itself.
3) **POST**:- Used when the client is sending information or data to the server—for example, filling out an online form (i.e. Sends a large amount of complex data to the Web Server).
4) **PUT:- Used when the client is sending a replacement document or uploading a new document to the Web server under the request URL.
5) **DELETE**:- Used when the client is trying to delete a document from the Web server, identified by the request URL.
6) **TRACE**:- Used when the client is asking the available proxies or intermediate servers changing the request to announce themselves.
7) **OPTIONS**:- Used when the client wants to determine other available methods to retrieve or process a document on the Web server.
8) **CONNECT**:- Used when the client wants to establish a transparent connection to a remote host, usually to facilitate SSL-encrypted communication (HTTPS) through an HTTP proxy.

###### Reference
* https://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol
* https://www.w3schools.com/tags/ref_httpmethods.asp

[[↑] Back to top](#network-questions)


### HTTPS negotiation steps?
1.	Client request a SSL connection.
2.	Server response with the certificate(public key;SSL done).
3.	Client validates the certificate/public key.
4.	Client generates a symmetric key(session key) and transmits it to the server.
5.	SSL session is established(finished).

###### Reference
* https://stackoverflow.com/questions/6241991/how-exactly-https-ssl-works

[[↑] Back to top](#network-questions)


### What is CORS? 
Cross-Origin Resource Sharing. Uses additional HTTP headers to let a user agent gain permission to access selected resources from a server on a different origin (domain) than the site currently in use. A user agent makes a cross-origin HTTP request when it requests a resource from a different domain, protocol, or port than the one from which the current document originated.

###### Reference
* https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS

[[↑] Back to top](#network-questions)


### REST?
Representational State Transfer (REST) is an architectural style that defines a set of constraints and properties based on HTTP. (Resource-base/Representations)
####The six constraints are:
-	**Uniform Interface(CRUD)**- simplifies and decouples the architecture/ evolve independently
-	**Stateless**--no client context being stored on the server between requests
-	**Cacheable**--eliminates some client–server interactions, further improving scalability and performance.
-	**Client-Server**-- enforce security policies
-	**Layered System**
-	**Code on Demand** (optional)-- temporarily extend or customize the functionality

###### Reference
* https://en.wikipedia.org/wiki/Representational_state_transfer
* http://www.restapitutorial.com/lessons/whatisrest.html

[[↑] Back to top](#network-questions)


### Web API?
 application programming interface for either a web server or a web browser.

###### Reference
* https://en.wikipedia.org/wiki/Web_API

[[↑] Back to top](#network-questions)
