# Stack - A Serverless NoSQL Database

**Stack** is a high-performance, serverless NoSQL database designed with an emphasis on scalability and flexibility. By focusing on efficient internal data storage and retrieval, Stack aims to provide rapid access to data while scaling seamlessly across a wide range of use cases.

## Why Go?

Stack is built with the Go programming language for several key reasons:

- **Concurrency**: Go’s goroutines and channels make it ideal for handling multiple concurrent operations, a critical feature for databases that need to manage large volumes of requests simultaneously.
- **Performance**: Go is known for its fast execution times, making it a great choice for performance-sensitive applications like databases.
- **Simplicity and Readability**: Go is a relatively simple language, making it easy to maintain and extend Stack as the project evolves.
- **Strong Ecosystem**: Go has a rich ecosystem, providing great libraries and tools that help with building robust, high-performance applications.

## In-Memory Data Storage Priority

One of the core design decisions behind Stack is the use of **in-memory data storage**. This choice prioritizes speed and efficiency in data retrieval. Here’s why:

- **Faster Access**: Accessing data in memory is significantly faster than querying disk-based storage, which makes Stack ideal for high-throughput applications where speed is critical.
- **Reduced Latency**: By storing data in memory, Stack reduces the need for costly disk I/O operations, which translates to lower latency and faster response times.
- **Scalability**: In-memory databases can scale easily as the entire database is stored in RAM, and systems with larger amounts of memory can handle growing data volumes without the need for complex disk-based scaling solutions.

While in-memory storage does have certain trade-offs (e.g., limited by system memory), this design choice aligns with Stack’s focus on speed and flexibility, especially for applications with high performance requirements.

## Getting Started

To run the Stack server locally, follow these steps:

### 1. Clone the repository:

```bash
git clone https://github.com/your-username/stack.git
cd stack
```

### 2. Launch the server:

Inside the `source` folder:

```bash
go run .
```

This will start the Stack server locally, allowing you to interact with the database.

A port will be open through the TCP protocol so you can connect with the database with:

```bash
 telnet localhost 9000  
```

### 3. Unit Testing
To run the unit tests, navigate to the source folder and run:

```bash
go test ./src/unit...
```

This will execute the unit tests and display the results in your terminal.
