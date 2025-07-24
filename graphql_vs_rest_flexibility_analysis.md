# ⚔️ GraphQL vs REST API: Flexibility Analysis

## 🧵 The Over-Fetching Problem

In a REST API, over-fetching occurs when a client must retrieve more data than it actually needs. For example, calling `/users` might return an entire user object including email, address, and profile image when the client only needs the username. Under-fetching happens when multiple endpoints are needed to assemble the required data, leading to additional HTTP requests.

GraphQL solves both of these problems by allowing the client to request exactly what it needs and nothing more. Using its flexible query syntax, a client can specify just the fields it wants reducing payload sizes and improving performance. This fine-tuned control eliminates the need for multiple requests or unnecessary data.

---

## 🔌 Endpoint and Schema Philosophy

A REST API is organized around multiple endpoints, each representing a specific resource (e.g., `/users`, `/posts`, `/products`). This can lead to redundancy and tight coupling between frontend and backend changes.

In contrast, GraphQL uses a **single endpoint** and operates based on a strongly-typed schema. This schema defines all available data types and their relationships in one place, making the API self-documenting. For frontend developers, this is a major advantage as they can explore the schema, auto-generate queries, and reduce reliance on backend updates. Tools like GraphQL, Playground and GraphiQL further enhance this discoverability and ease of use.

---

## 🧠 Caching and Complexity

Caching in REST is straightforward because each endpoint maps to a specific resource and HTTP verbs (like GET) can be cached by browsers or CDNs using standard headers.

GraphQL complicates this because all requests go through a single endpoint (`/graphql`) and each query can vary. As a result, traditional caching mechanisms are harder to implement. Developers may need to rely on custom caching logic or tools like Apollo Client's normalized caching.

However, the flexibility of GraphQL makes it ideal for use cases like **mobile apps**, **complex UIs**, or **real-time data dashboards**, where data needs vary widely between views. In such scenarios, the precision and speed of GraphQL outweigh the caching limitations.

---

## 📚 Sources

- [GraphQL vs REST: A Comprehensive Comparison](https://hygraph.com/blog/graphql-vs-rest-apis)
- [Is GraphQL Better Than REST? A Comparison](https://tailcall.run/graphql/graphql-vs-rest-api-comparison/)
- [GraphQL vs REST: API Showdown](https://medium.com/@programordie/graphql-vs-rest-api-showdown-fcf11d9c4fe6)

## 🧑🏿‍💻 Author

Created by [Yusuf Bolden](github.com/YusufBolden).
