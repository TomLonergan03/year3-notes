There are [[W3N2 - Transport service guarantees|many possible guarantees]] a transportation system could make, but the internet provides only 2 transport protocols.
# Transmission control protocol (TCP)
TCP guarantees that a bytestream sent using it will arrive, and arrive in order with no duplicate packets (provides [[W3N2 - Transport service guarantees#Reliable data transfer|reliable data transfer]]). It is a **connection oriented service**, meaning that the client and server exchange transport layer level control information before the application layer messages start to flow. This is the **TCP handshake**, after which a **TCP connection** is said to exist between the sockets at either end. TCP also includes a **congestion control mechanism**, which throttles the sending process if the network is congested between the sender and receiver, to limit that process' impact on the network. The congestion control also attempts to limit each TCP connection to its fair share of network bandwidth.
# User datagram protocol (UDP)
UDP provides no guarantees about anything - data sent over it may arrive corrupted, out of order, or simply not arrive at all. UDP makes no attempt to control congestion, and will send data as fast as the underlying network is able to take it. UDP's advantage against TCP is that it is more performant, as it doesn't need to do the handshake or wait for acknowledgement of data being delivered.
# Services not provided by Internet transport protocols
No internet protocol provides (or can provide!) guarantees of [[W3N2 - Transport service guarantees#Timing|timing]] or [[W3N2 - Transport service guarantees#Throughput|throughput]]. This doesn't mean that the internet is unable to support timing or throughput sensitive applications, just that they must be designed to work without strict guarantees.