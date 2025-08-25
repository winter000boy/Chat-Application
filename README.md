# Chat Application

A high-level, real-time chat application built with modern web technologies. The project leverages **SockJS** and **STOMP.js** (using the STOMP protocol) for robust WebSocket communication, and is powered by a Java Spring backend.

---

## Features

- **Real-Time Messaging**: Instant chat using WebSockets for low-latency communication.
- **SockJS & STOMP.js**: Ensures reliable messaging even when native WebSockets are not available.
- **Spring Boot Backend**: Scalable and production-ready server logic written in Java.
- **STOMP Protocol**: Standard messaging protocol for interoperability and reliability.
- **User-Friendly Interface**: Modern, responsive front-end for seamless chatting.

---

## Tech Stack

- **Frontend**
  - [SockJS](https://github.com/sockjs/sockjs-client): WebSocket emulation for reliable real-time messaging.
  - [STOMP.js](https://stomp-js.github.io/): Implements STOMP protocol over WebSockets.
  - JavaScript, HTML, CSS (Framework/library can be specified if used)
- **Backend**
  - [Java Spring Boot](https://spring.io/projects/spring-boot): RESTful API and WebSocket/STOMP endpoint management.
  - Spring WebSocket, Spring Messaging

---

## Getting Started

### Prerequisites

- Java 11 or higher
- Node.js & npm (if building the frontend separately)
- Maven or Gradle for managing backend dependencies

### Running the Application

#### Backend (Spring Boot)

1. Clone the repository:
    ```bash
    git clone https://github.com/winter000boy/Chat-Application.git
    cd Chat-Application
    ```

2. Build and run the backend:
    ```bash
    ./mvnw spring-boot:run
    ```
    Or, if using Gradle:
    ```bash
    ./gradlew bootRun
    ```

#### Frontend

- If the frontend is a separate project, follow its README or serve the static files as specified.

---

## Architecture Overview

- **Client** establishes a connection using SockJS.
- **STOMP.js** is used to communicate with the backend using the STOMP protocol.
- **Spring Boot** handles messaging, authentication, and business logic.
- **WebSocket endpoints** are managed by the backend, ensuring real-time delivery.

---

## Example WebSocket Flow

1. Client connects to `/ws` endpoint via SockJS.
2. STOMP.js subscribes to relevant chat topics (e.g., `/topic/messages`).
3. Users send/receive messages in real time.

---

## Contributing

Contributions are welcome! Please fork the repo and submit a pull request.

---

## License

This project is licensed under the MIT License.

---

## References

- [SockJS Documentation](https://sockjs.github.io/sockjs-protocol/)
- [STOMP Protocol](https://stomp.github.io/)
- [Spring WebSocket](https://docs.spring.io/spring-framework/docs/current/reference/html/web.html#websocket)
