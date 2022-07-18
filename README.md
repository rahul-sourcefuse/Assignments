# Assignments
## Question 1. How HTTPS works behind the scene?

Answer: HTTPS stands for HyperText Transfer Protocol Secure. It means HTTP over a secure layer so that no one will be able to sniff data or modify it in middle. In HTTPS when the client tries to connect with the server. The server will return the SSL certificate. It contains a public key and a digital signature. It will be used to identify the certificate is valid or not. The public key will be used for the asymmetric encryption process. 

#### Asymmetric
Asymmetric encryption is known as public-key cryptography. In this public key is being used to encrypt the data while the private key is being used to decrypt the data

#### How HTTPS use it?
    1. During the handshake, the server sends an SSL certificate that has an asymmetric public key to the client. It has a private key that is stored at the webserver(self) end.
    2. The client will create a session key based on algorithms. This session key will be encrypted by using the public key. Then it will be sent to the server.
    3. The server will use the asymmetric private key to decrypt the encrypted session key and will get the session key.
    4. Now the browser will use the session key for encrypting and decrypting the data for the session. This is known as symmetric encryption. Now the data is secured as the session key will be known by the client and server. Once the session will be expired the process will be repeated again from step 1 as the session key will be no longer valid.



## Question 2 : What are different http methods available and what they exactly do ?
1. #### GET : The GET method is used to retrieve information from the given server using a given URI. URI stands for Uniform Resource Identifier. Requests using GET should only retrieve data and should have no other effect on the data. This is the main method used for document retrieval.
2. #### HEAD : The HEAD method is functionally similar to GET, except that the server replies with a response line and headers, but no entity-body. 
3. #### POST: A POST request is used to send data to the server, for example, customer information, file upload, etc. using HTML forms.The POST method is used when you want to send some data to the server, for example, file update, form data, etc. The following example makes use of POST method to send a form data to the server, which will be processed by a process.cgi and finally a response will be returned.
4. #### PUT: Replaces all current representations of the target resource with the uploaded content. 
5. #### DELETE :Removes all current representations of the target resource given by a URI. 
6. #### CONNECT : The CONNECT method is used by the client to establish a network connection to a web server over HTTP.
7. #### OPTIONS : The OPTIONS method is used by the client to find out the HTTP methods and other options supported by a web server. The client can specify a URL for the OPTIONS method, or an asterisk (*) to refer to the entire server.
8. #### TRACE: The TRACE method is used to echo the contents of an HTTP Request back to the requester which can be used for debugging purpose at the time of development.





## Question 3: Understand and explain the use of various http response codes.
##### The Status-Code element in a server response, is a 3-digit integer where the first digit of the Status-Code defines the class of response and the last two digits do not have any categorization role. There are 5 values for the first digit:

###  1xx: Informational
    It means the request has been received and the process is continuing.
###  2xx: Success
    It means the action was successfully received, understood, and accepted.
###  3xx: Redirection
    It means further action must be taken in order to complete the request.
###  4xx: Client Error
    It means the request contains incorrect syntax or cannot be fulfilled.
###  5xx: Server Error
    It means the server failed to fulfill an apparently valid request.

## Question 4: What are the different web communication protocols and their use cases?

##### 1. Transmission Control Protocol (TCP): TCP is a popular communication protocol which is used for communicating over a network. It divides any message into series of packets that are sent from source to destination and there it gets reassembled at the destination.
##### 2. Internet Protocol (IP): IP is designed explicitly as addressing protocol. It is mostly used with TCP. The IP addresses in packets help in routing them through different nodes in a network until it reaches the destination system. TCP/IP is the most popular protocol connecting the networks.
##### 3. User Datagram Protocol (UDP): UDP is a substitute communication protocol to Transmission Control Protocol implemented primarily for creating loss-tolerating and low-latency linking between different applications.
##### 4. Post office Protocol (POP): POP3 is designed for receiving incoming E-mails.
##### 5. Simple mail transport Protocol (SMTP): SMTP is designed to send and distribute outgoing E-Mail.
##### 6. File Transfer Protocol (FTP): FTP allows users to transfer files from one machine to another. Types of files may include program files, multimedia files, text files, and documents, etc.
##### 7. Hyper Text Transfer Protocol (HTTP): HTTP is designed for transferring a hypertext among two or more systems. HTML tags are used for creating links. These links may be in any form like text or images. HTTP is designed on Client-server principles which allow a client system for establishing a connection with the server machine for making a request. The server acknowledges the request initiated by the client and responds accordingly.
##### 8. Hyper Text Transfer Protocol Secure (HTTPS): HTTPS stands for Hyper Text Transfer Protocol Secure . It is a standard protocol to secure the communication among two computers one using the browser and other fetching data from web server. HTTP is used for transferring data between the client browser (request) and the web server (response) in the hypertext format, same in case of HTTPS except that the transferring of data is done in an encrypted format. So it can be said that https thwart hackers from interpretation or modification of data throughout the transfer of packets.
##### 9. Telnet: Telnet is a set of rules designed for connecting one system with another. The connecting process here is termed as remote login. The system which requests for connection is the local computer, and the system which accepts the connection is the remote computer.
##### 10.Gopher: Gopher is a collection of rules implemented for searching, retrieving as well as displaying documents from isolated sites. Gopher also works on the client/server principle.

## Question 5: Pros and cons of Single page and multi page applications.
### Single-page Apps
The major difference between multi-page and single-page applications is that single-page apps download the page a single time once it is executed.
As soon as a user interacts with the app, only the required component will be modified, not the complete application, which makes a single-page app much faster in terms of interactivity. Single-page applications offer a much better user experience (UX), meaning that users can navigate easily between the different pages of an app without waiting for the pages to load.

**Advantages of Single-page Apps**

An important feature of single-page applications is performance. They get a performance boost by loading HTML, CSS, and JavaScript resources as soon as the website is loaded.
The reason is that when users come to an application, they need the shortest possible wait time so that they can do their work and leave. The performance reflects the demand for the application.
If the application does not provide the necessary performance, users may leave that app and choose another platform. That's one of the primary reasons developers choose single-page apps nowadays.

There are other advantages as well:

    * Battery reusability
    
    * Optimization
    
    * Client-side rendering
    
    * User experience
    
    * Easy debugging
    
    * Performance
    
    * Less complex implementation
    
    * Better caching
    
    * Better SEO optimization
    
**Disadvantages of Single-page Apps**

There are also some disadvantages to using single-page apps:

    • Single-page apps use JavaScript, so it can be difficult to trace errors.
    
    • Users need to turn on JavaScript in their web browser or the application won’t work.
    
    • Memory leaks may result in a performance drop.
    
    • Single-page apps are not suitable for enterprise-based applications, only for small and mid-size applications.
    
    • They have terrible maintainability due to using third-party plug-ins.


### Multi-page Apps

Multi-page applications contain tons of pages, and when users request resources or interact, the app has to go to the server, download the resource, and show it to the user.
The process is quite slow and painful when it comes to performance, but mostlarge companies use multi-page applications because they have to deal with tons of services and products.
One disadvantage is in flexibility and optimization. Users may need to put in more effort, and required changes may be costly over time.

**Other disadvantages of multi-page applications include:**

    • Slow performance
    
    • Higher resource utilization
    
    • Less flexibility
    
    • More time for development and maintenance
    
    • Less reusability
    
**Comparing Single-page and Multi-page Apps**
    • Multi-page applications are often optimized for SEO so you can target your audience easily, while single-page applications are not quite optimized for that.
    
    • Single-page applications are easy to develop and maintain, while multi-page applications can be complex to develop and maintain.
    
    • Multi-page applications follow a high-security standard, while single-page applications are less secure.
    
    • One advantage of single-page apps is that they won’t make a round trip when a user interacts with the system, while multi-page apps make a round trip for each request from the end user.
    
    • Single-page applications are compatible with offline service when an internet connection is interrupted, while multi-page applications need the connection to complete user requests.
