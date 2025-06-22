# GraphQL API with Subscriptions

A clean and efficient GraphQL API implementation with real-time subscriptions using Node.js, Express, and Apollo Server.

## Features

- GraphQL Queries, Mutations, and Subscriptions
- Real-time updates using WebSocket
- Clean and modular code structure
- Efficient message handling with PubSub
- Memory-optimized implementation

## Installation

1. Install dependencies:
```bash
npm install
```

2. Start the server:
```bash
npm start
```

For development with auto-reload:
```bash
npm run dev
```

The server will run at:
- HTTP: http://localhost:4000/graphql
- WebSocket: ws://localhost:4000/graphql

## GraphQL Operations

### Query
```graphql
query {
  messages {
    id
    content
    timestamp
  }
}
```

### Mutation
```graphql
mutation {
  sendMessage(content: "Hello, World!") {
    id
    content
    timestamp
  }
}
```

### Subscription
```graphql
subscription {
  messageAdded {
    id
    content
    timestamp
  }
}
```

## Performance Considerations

- Uses efficient PubSub implementation
- Implements proper server cleanup
- Optimized WebSocket handling
- Memory-efficient message storage
