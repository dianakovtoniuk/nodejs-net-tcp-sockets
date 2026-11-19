# Node.js TCP Server and Client

A minimal example of TCP networking in Node.js using the built-in `net` module. A server listens on a local port and logs the raw bytes it receives, and a client connects to it and sends a small buffer.

## How it works

1. `simple-server.js` creates a TCP server on `127.0.0.1:3099` and prints every chunk of data received from a connected client.
2. `simple-sender.js` opens a connection to that server and writes a 2-byte buffer (`12` and `34`).

## Usage

Start the server in one terminal:

```bash
node networking/simple-server.js
```

Then run the sender in another:

```bash
node networking/simple-sender.js
```

The server logs the received buffer:

```
<Buffer 0c 22>
```

## Requirements

- Node.js 16 or newer
