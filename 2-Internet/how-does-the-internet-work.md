# How does the internet work

Notes from the book *Computer Networking: A Top Down Approach, 7th edition*.

## 1 What is the Internet

We can answer this question in two ways. One in terms of its **hardware and software components**. The other in terms of an **infrastructure** for providing services to distributed applications.

1. The internet is a computer network that interconnectes billions of computing devices throughout the world. The devices being hooked up to the internet are called **hosts** and **end systems**. 
      - End systems  are connected together by a network of **communication links** (copper wire, radio spectrum, optical fiber ...) and **packet switches** (routers, link-layer switches). 
      - End systems access the Internet through **Internet Service Providers** (ISPs, like local cable or telephone companies, airports, hotels that provide WIFI) which itself is a network of packet switches and communication links. 
      - End systems, packet switches and other pieces of the Internet run **protocols**(Transmission Control Protocol(TCP) and the Internet Protocol(IP),...) that control the sending and receiving of Information within the Internet. 

2. The internet is an infrastructure that provides services to distributed **applications**(e-mail, web surfing, mobile applications: messaging, mapping, music streaming...)

   	- End systems attached to the Internet provide a **socket Interface** that specifies how a program running on one end system asks the Internet infrastructure to deliver data to a specific destination program running on another end system. 

   - The Internet socket interface is a set of ruls that sending program must follow so that the Internet can deliver the data to the destination program.

### 1.1 What is a protocol

A protocol defines the **format** and the **order** of messages exchanged between two or more communicating entities, as well as **actions** taken on the transmission and/or receipt of a message or other event.

- Consider when you make a request to a web server. That is, when you type the URL of a web page into your browser. First your computer will send a connection request message to the web server and wait for a reply. The web server will eventually receive your connection request message and return a connection reply message. Knowing it is now OK to request a web document, your computer will send the name of the web page it wants to fetch from the web server in a GET message. Finally the web server returns the web page to your computer.

## 2. The Network Edge

The **end systems** include:

- Desktop Computers: PCs, Macs, and Linux boxes
- Servers: Web and email servers
- Mobile Devices: laptops, smartphones
- Other: IoT

End systems are also refered to as **hosts** because they host application programs such as a web browser program, a web server program, an e-mail client program.

### 2.1 Access Network

- Home Access: DSL, Cable, FTTH, Dial-UP and Satellite
- Access in the Enterprise(and the Home): Ethernet and WIFI
- Wide-Area Wireless Access: 3G and LTE.

### 2.2 Physical Media

- Twisted-Pair Copper WIre
- Coaxial Cable
- Fiber Optics
- Terrestrial Radio Channels
- Satellite Radio Channels

## 3. The Network Core

The network core: the mesh of packet switches and links that interconnects the internet's end systems.

There are two fundamental approaches to moving data through a network of links and switches: 

- Circuit Switching
- Packet Switching

### 3.1 Packet Switching

#### Packet

In network application, end systems exchange message with each other. Messages can contain anything the application wants. To send a message from a source end system to destination end system, the source breaks long messages into smaller chunks of data known as **packets**.

#### Packet Switches

Between source and destination, each packet travels through communication links(full transmisssion rate) and **packet switches**.

- Routers
- Link-layer switches

#### Store-and-Forward Trasmission

Most packet switches use the store-and-forward transmission at the input to the links. The packet switch must receive the entire packet before it can begin to transmit the first bit of the packet onto the outbound link. 

Routers neet to receive, store and process the entire packet before forwarding.

The general case of sending one packet of L bits from source to destination over a path consisting of N links each of rate R (thus, there are N-1 routers between source and destination). The end-to-end delay is:

```
d_end2end = N*L/R
```

#### Queuing Delays and Packet Loss

Each packet switch has multiple linkes attached to it. For each attached link, the packet switch has an **output buffer**(also called an **output queue**), which stores packets that the router is about to send int the link.

Imagine a packet has arrived but the packet switch is busy transmission another packet. So this packet must wait in queue. So in addition to store-and-forward delays, packets suffer output buffer **queuing delays**, which depend on the level of congestion in the network.

However, since the amout of a buffer space is finite, an arriaving packet may find that the buffer is completely full with other packets in queue. In this case **packet loss** will occur-- either the arriving packet or one of the already queued packets will be dropped.

#### Forwarding Tables and Routing Protocols

Router takes a packet arriving on one of its attached communication links and forward that packet onto another one of its attached communication links. Packet forwarding is actually done in different ways in different types of computer networks. In the Internet, every end system has an address called an **IP address**.

When a source end system want to send a packet to a destination end system, the source includes the destination's IP address in the packet's header. Each router has a **forwarding table** that maps destination address(or portions of it) to tht router's outbound links. When a packet arrives, the router examines the header, find the address and search the forwarding table to find the appropriate outbond link.

### 3.2 Circuit Switching



### 3.3 A Network of Networks



## 4. Delay, Loss and Throughout in Pack



## 5. Protocol Layers and Their Service



## 6. Network Under Attack



## 7. History of Computer Networking

