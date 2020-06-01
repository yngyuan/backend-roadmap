# How does the internet work

## 1 What is the Internet

We can answer this question in two ways. One in terms of its hardware and software components. The other in terms of an infrastructure for providing services to distributed applications.

1. The internet is a computer network that interconnectes billions of computing devices throughout the world. The devices being hooked up to the internet are called **hosts** and **end systems**. 
   			- End systems  are connected together by a network of **communication links**(copper wire, radio spectrum, optical fiber ...) and **packet switches**(routers, link-layer switches). 
   			- End systems access the Internet through **Internet Service Providers**(ISPs, local cable or telephone companies, airports, hotels that provide WIFI) which itself is a network of packet switches and communication links. 
   			- End systems, packet switches and other pieces of the Internet run **protocols**(Transmission Control Protocol(TCP) and the Internet Protocol(IP),...) that control the sending and receiving of Information within the Internet. 

2. The internet is an infrastructure that provides services to distributed **applications**(e-mail, web surfing, mobile applications: messaging, mapping, music streaming...)

   	- End systems attached to the Internet provide a **socket Interface** that specifies how a program running on one end system asks the Internet infrastructure to deliver data to a specific destination program running on another end system. 

   - The Internet socket interface is a set of ruls that sending program must follow so that the Internet can deliver the data to the destination program.

