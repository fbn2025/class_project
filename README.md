# Class Project on Git

A class project on Git and Github Collaboration.

## Website Architecture

Our website is structured around three key players:

- **DevOps Project** – manages infrastructure, CI/CD, hosting, and monitoring.
- **Backend Team** – develops APIs, handles business logic, and works with the database.
- **Frontend Team** – builds the user interface and delivers static assets.

### Architectural Diagram

```mermaid
flowchart TB
A[End User] --> B[Frontend (Static)]
B --> C[Backend API Layer]
subgraph DevOps
    D[Hosting/CDN]
    E[CI/CD & Monitoring]
    F[Security & Infrastructure]
end
B --> D
C --> D
C --> G[Database/Storage]
D --> E
D --> F
E --> D
F --> D
```

This diagram illustrates how users interact with the frontend, which in turn communicates with the backend. DevOps provides the underlying services for both layers.
