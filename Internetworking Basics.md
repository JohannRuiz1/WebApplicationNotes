
### Circuit Switching
- When a connection is established, there is a fixed path of communication, and that call takes all the bandwidth
- Other phones get the *busy* signal when in use
- Routing only occurs before the call

### Packet Switching
- Internet Protocol provides a decentralized packet-switched foundation
- Each packet is individually and continuously routed, baed on it's destination address
- Multiple users can send packets through statistically multiplexing
- Packets may 1) arrive out of order 2) dropped/lost/corrupted 3) duplicated
- TCP (Transmission Control Protocol): Reliability over Speed, Connection-Oriented
- UDP (Universal Datagram Protocol): Speed over Reliability, Connectionless
![[Pasted image 20240521074215.png]]

### OSI Reference Model
- Provide an abstract view of the network, and group functionality into layers
- Each layer
	- provides services to the upper layers
	- uses the services of the lower layers
	- has one or more alternate protocols

| Top to Bottom | OSI Layer | Description | Example |
| ---- | ---- | ---- | ---- |
| 7 | Application Layer | Ensure communication between distributed software components | HTTP, FTP, SMTP |
| 6 | Presentation Layer | Convert OS standards to/from network representations | SSL |
| 5 | Session Layer | Manages connections between local and remote application | Sockets |
| 4 | Transport Layer | Deliver data from operating system to operating system | TCP, UDP |
| 3 | Network Layer | Deliver packets with routing services across multiple data links | IP (Unifying Protocol) |
| 2 | Data Link Layer | Groups bits into addressed frames for transmission over physical links | Ethernet  |
| 1 | Physical Layer | Deliver bits over physical link | IEEE 802.11 |
