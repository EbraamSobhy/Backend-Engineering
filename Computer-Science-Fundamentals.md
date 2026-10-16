# Computer Memory Fundamentals

## Memory and processes
- RAM (Random Access Memory): Acts as the fast, volatile working space for the operating system and active apps. Data disappears when power turns off.
- ROM (Read-Only Memory) is non-volatile memory that stores essential instructions permanently. It holds system firmware and boot instructions.
- Memory Hierarchy: Ranks storage by speed and capacity, starting from ultra-fast CPU registers and cache, down to main RAM, and finally to slow, permanent storage like SSDs.
- Virtual Memory: Extends physical RAM using disk space, letting the system run large programs by swapping data in blocks called pages.
- Process Definition: A program loaded into memory and actively run by the CPU.
- Process Memory Layout: Splits into distinct segments: text (code), data (variables), stack (function calls), and heap (dynamic allocation).
- Multiplexing: Shares the CPU and memory safely across many running programs so they do not interfere with each other.
- A memory unit is a standard unit used to measure the amount of data that can be stored, processed, or transferred in a computer system. It represents the storage capacity of memory and storage devices.

---

## Threads and Concurrency
- Process: An independent running program with its own isolated memory space, code, and system resources.

- Thread: A lightweight execution unit inside a process that shares the same memory space, heap, and file handles with other threads in that process. Each thread keeps its own stack, program counter, and registers.

- Concurrency: means dealing with multiple tasks at once by interleaving their execution (even on a single-core CPU via context switching).

---

## Networking Fndamentals
- Computer networking fundamentals are the core rules, hardware, and concepts that allow devices to talk to each other and share data.

### Core Network Components
- Nodes: Physical devices like computers, phones, or printers that send and receive data.
- Media: The wired cables (Ethernet, fiber optic) or wireless signals (Wi-Fi) that carry data.
- Switches: Devices that connect computers inside the same local network.
- Routers: Devices that connect multiple separate networks together and send data to the internet.
- Routers and switches control the flow of information.
- Wired media includes Ethernet and optical fiber cables.

### Key Rules and Protocols
- Protocols: Predefined rules that let different devices understand each other.
- IP Address: A unique number given to every device on a network so data reaches the right place.
- TCP / UDP: Transport rules that manage how data packets move reliably or quickly.
- HTTP / DNS: Higher-level rules used to load web pages and translate website names into numbers.

### How Computer Network Working
- Computer network operates by enabling devices to communicate and exchange data using a shared communication system. Each device in the network follows predefined rules to ensure that data is transmitted accurately, efficiently, and securely.
- A network consists of nodes such as computers, servers, routers, and switches that send or receive data.
- These nodes are connected through links, which may be wired (cables, optical fiber) or wireless (Wi-Fi, radio signals).
- When data is sent, it is broken into small packets and transmitted across the network.

---

## HTTP/HTTPS
- HTTP and HTTPS are application-layer communication protocols used by clients (like web browsers) and servers to exchange data on the web, with HTTPS adding a secure encryption layer (TLS/SSL) to protect data in transit.

### What is HTTP?
- Hypertext Transfer Protocol is the foundation of data communication on the World Wide Web.
- Client-Server Model: The client sends a request (for a webpage, image, or script), and the server processes it and returns a response.
- Stateless: Each request-response cycle is independent; the server does not retain session information by default.
- Plain Text: Data transfers in clear text, making it easy for outside observers to read or tamper with traffic.
- Network Details: Operates on default port 80 over TCP.
- Common Methods: GET (retrieves data), POST (submits data), PUT/PATCH (updates data), and DELETE (removes data).

### What is HTTPS?
- Hypertext Transfer Protocol Secure is an extension of HTTP that incorporates cryptographic security.
- Encryption: Uses TLS (Transport Layer Security) or SSL to scramble data so third parties cannot read it.
- Authentication: Relies on digital certificates issued by a trusted Certificate Authority (CA) to verify the identity of the server.
- Network Details: Operates on secure port 443.
- Integrity: Ensures messages cannot be modified or corrupted undetectably while traveling across the network.

## TCP/IP and DNS
### What is DNS?
- The Internet's Phonebook: DNS (Domain Name System) translates human-readable names into machine-readable numeric IP addresses.
- Lookup Process: When you type a web address, your computer queries root servers, TLD (Top-Level Domain) servers, and authoritative nameservers until it finds the matching IP address.

### What is TCP/IP?
- The Communication Suite: TCP/IP (Transmission Control Protocol / Internet Protocol) is the core set of rules governing how data travels across networks.
- IP (Internet Protocol): Handles addressing and routing, acting like a physical street address on an envelope to ensure packets find the correct destination.
- TCP (Transmission Control Protocol): Ensures reliable delivery by establishing a connection via a "three-way handshake," checking for missing data, and reassembling packets in the correct order.

### What does TCP do?

- TCP makes sure that data sent from one computer to another:
- Arrives at the correct destination
- Arrives in the correct order
- Is not missing or corrupted
- Can be retransmitted if something goes wrong

- Think of TCP like sending a package through a reliable delivery service. It tracks the packages and makes sure the receiver gets everything in the right order.

- Suppose you want to download a file from a website Your computer needs to receive A → B → C → D → E TCP breaks the data into smaller pieces called segments and sends them across the network.
If the receiver gets A → B → D → E TCP notices that C is missing and asks for it again. Once C arrives, TCP puts everything back in the correct order A → B → C → D → E

### The Four Layers of TCP/IP
- Application Layer: Interacts directly with software applications (using protocols like HTTP, SMTP, and DNS).
- Transport Layer: Manages host-to-host communication and session tracking using TCP or UDP.
- Internet Layer: Handles packet addressing and routing via IP.
- Link Layer: Manages network hardware, physical connections, and MAC addresses for local transmission.

## Operating System (OS)

### Core Components
- Kernel: The central core of the OS that sits directly between the hardware and software layers, handling critical tasks like CPU scheduling and memory control.
- Shell: The outer user-facing layer that interprets user commands via a Command-Line Interface (CLI) or Graphical User Interface (GUI).

### Key Responsibilities
- Process Management: Creates, schedules, pauses, and terminates tasks and threads to allow smooth multitasking.
- Memory Management: Allocates and frees up physical RAM and virtual memory space for active programs.
- File Systems: Organizes data into a structured hierarchy of files and directories on storage drives.
- Device Control: Communicates with external hardware components like keyboards, mice, and printers using device drivers.
- Security: Enforces permissions, authentication, and user access controls to protect data.

## File Systems
- User Application: The programs or software that request file operations like read, write, or delete.
- Logical File System: Manages metadata, file names, directories, and access permissions.
- Virtual File System (VFS): Acts as a bridge, allowing different file systems to work under a single interface.
- Physical File System: Handles the actual storage of data blocks on the disk.
- Partition 1, Partition 2, Partition 3: Divisions of the storage device where files are stored physically.

### Popular File Systems
- FAT (File Allocation Table): An older file system used by older versions of Windows and other operating systems.
- NTFS (New Technology File System): A modern file system used by Windows. It supports features such as file and folder permissions, compression and encryption.
- ext (Extended File System): A file system commonly used on Linux and Unix-based operating systems.
- HFS (Hierarchical File System): A file system used by macOS.
- APFS (Apple File System): A new file system introduced by Apple for their Macs and iOS devices.

- NTFS: A secure, advanced file system used by modern Windows.
- Ext4: A fast, reliable file system used by Linux systems.
- FAT32: An older, simpler file system that works on many types of USB drives and devices.

## Serialization and Deserialization
- Serialization is the process of converting an in-memory object's state into a byte stream or standard text format (like JSON or XML) so it can be easily stored or transmitted, while deserialization is the exact reverse process of reconstructing that byte stream back into a usable live object.

### Key Concepts
- Serialization: Translates complex data structures and object states into a linear, portable format (bytes, JSON, XML)
- Serialization = converting an object/data structure in memory into a format that can be stored or sent.

```js
User {
  name: "John",
  age: 25
}
```
- Serialization might turn it into JSON:

```JSON
{"name":"John","age":25}
```

You could then:
- save that JSON to a file/database
- send it over a network
- put it in a cache

Later, deserialization converts:
```JSON
{"name":"John","age":25}
```
back into a User object.

- Deserialization: Reads the portable byte stream or text and rebuilds the exact native object in memory.
- Deserialization = converting that stored/transmitted format back into an object/data structure that the program can use.

- Object in memory → Serialization → storable/transmittable data → Deserialization → Object in memory

### Common Use Cases
- Data Transmission: Sending data objects across a network or via web APIs (REST, microservices).
- Persistence: Saving application state, files, or user preferences to a hard drive or database.
- Caching: Storing active objects in memory caches like Redis for fast retrieval.

### Popular Formats
- JSON / XML: Human-readable, text-based formats ideal for cross-platform and web communication.
- Binary: Compact, highly optimized formats used for low-latency performance and internal system storage.

## Authentication vs authorization

### Authentication (AuthN)
- Definition: The process of proving your identity to a system.
- Question answered: "Who are you?"
- How it works: You provide credentials like a username, password, one-time code (OTP), or fingerprint. The system checks if these match its records.
- Timing: This always happens first, usually when you log in.
- Protocols/Tools: OpenID Connect (OIDC), passwords, and biometrics.
- HTTP Error: 401 Unauthorized (which actually means unauthenticated).

### Authorization (AuthZ)
- Definition: The process of granting or denying access to specific resources or actions.
- Question answered: "What are you allowed to do?"
- How it works: The system checks your verified identity against preset rules or roles (like regular user vs. admin) to see if you can view a file or run a command.
- Timing: This happens after authentication, every time you try to access a protected resource.
- Protocols/Tools: OAuth 2.0, Role-Based Access Control (RBAC).
- HTTP Error: 403 Forbidden.

### Real-World Example
- Authentication: Showing your passport at an airport security checkpoint to prove your identity.
- Authorization: Showing your boarding pass at the gate to get onto a specific airplane.
