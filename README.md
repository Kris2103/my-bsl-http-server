# BSL HTTP Server

A lightweight HTTP/1.1 web server built from scratch using the **Bonezegei (BSL)** programming language and the native socket library bindings.

---

## Features & Routing Specification

The server listens on `http://localhost:8080/` and handles client HTTP requests using custom route evaluation:

| Route | Method | Status | Description |
| :--- | :--- | :--- | :--- |
| `/` | `GET` | `200 OK` | Default landing page welcoming the user |
| `/about` | `GET` | `200 OK` | Information page about the project and implementation |
| `*` (Any other path) | `GET` | `404 Not Found` | Custom 404 error page for unmapped routes |

---

## Project Structure

```text
my-bsl-http-server/
├── .gitattributes
├── LICENSE
├── README.md
├── lib/
│   ├── socket.bzg
│   └── socket/
│       └── socket.dll
├── src/
│   └── http.bzg
└── documentation/
    ├── home.png
    ├── about.png
    ├── 404.png
    └── terminal.png
```

---

## Installation & Setup

### Prerequisites

* [Bonezegei (BSL)](https://github.com/bonezegei) installed and added to system `PATH`

### Running the Server

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/Kris2103/my-bsl-http-server.git](https://github.com/Kris2103/my-bsl-http-server.git)
   cd my-bsl-http-server
   ```

2. **Start the HTTP server:**
   ```bash
   bonezegei src/http.bzg
   ```

3. **Open the routes in any web browser:**
   * **Home:** `http://localhost:8080/`
   * **About:** `http://localhost:8080/about`
   * **404 Fallback:** `http://localhost:8080/hello`

---

## Documentation & Verification

### 1. Terminal Execution
PowerShell session running the BSL server, binding to port 8080, and logging incoming client requests:

![Terminal Execution](documentation/terminal.png)

### 2. Default Landing Page (`/`)
Response showing `HTTP/1.1 200 OK` on the root route:

![Home Page](documentation/home.png)

### 3. About Page (`/about`)
Response showing `HTTP/1.1 200 OK` on the about route:

![About Page](documentation/about.png)

### 4. 404 Not Found Page
Fallback handling showing `HTTP/1.1 404 Not Found` when requesting an unmapped route (e.g., `http://localhost:8080/hello`):

![404 Error Page](documentation/404.png)

---

## License

This project is licensed under the terms specified in the [LICENSE](LICENSE) file.
