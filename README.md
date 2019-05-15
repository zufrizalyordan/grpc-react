gRPC with React

### Diagram
gRPC Web (browser) -> envoy proxy -> gRPC backend

### Installation
`docker build -t grpc-web ./src`

`yarn`

### Running the app
`yarn start` -> starts the frontend app

`node src/server.js` -> starts the backend server

`docker run -d -p 9090:9090 grpc-web` -> starts envoy proxy 

### Notes
gRPC web-client won’t send HTTP2 requests. Instead, create a proxy between web-client and gRPC backend service for converting HTTP1 request to HTTP2. gRPC web client has built-in support for Envoy as a proxy.
