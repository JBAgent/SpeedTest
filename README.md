# Real-Time Network Speed Test

A client-server application that measures upload and download speeds in real-time with an interactive dashboard.

## Features

- Real-time download speed testing
- Real-time upload speed testing
- Interactive dashboard with progress tracking
- Speed history chart
- WebSocket communication for minimal latency
- Responsive design

## Requirements

- Node.js (v14 or higher)
- npm (v6 or higher)

## Installation

1. Clone the repository or download the files
2. Navigate to the project directory
3. Install dependencies:

```bash
npm install
```

## Usage

### Starting the server

```bash
npm start
```

For development with auto-restart:

```bash
npm run dev
```

### Accessing the client

Open your browser and navigate to:

```
http://localhost:3000
```

## How It Works

### Server Side

The server uses Express.js for HTTP handling and WebSockets for real-time communication. It:

1. Generates random data chunks for download tests
2. Receives data chunks for upload tests
3. Calculates speeds based on the amount of data transferred and elapsed time
4. Sends real-time speed updates to the client

### Client Side

The client uses a responsive HTML/CSS/JavaScript interface that:

1. Establishes WebSocket connection to the server
2. Provides buttons to start/stop speed tests
3. Displays real-time speed measurements
4. Shows data transfer progress
5. Charts historical speed data
6. Automatically attempts to reconnect if disconnected

## Customization

You can customize the test parameters by modifying the following variables in the code:

- `chunkSize` in server.js (default: 256KB) - Size of data chunks sent during tests
- The test duration and update intervals in both client and server code

## Troubleshooting

- If you cannot connect to the server, check your firewall settings
- For accurate results, avoid running other network-intensive applications during tests
- The application runs best on a local network (LAN) connection

## License

MIT
