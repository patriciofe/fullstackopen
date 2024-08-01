```mermaid
sequenceDiagram
  participant client
  participant server

  client->>server:GET https://studies.cs.helsinki.fi/exampleapp/spa
  activate server
  server-->>client:200 OK: SPA HTML Document
  deactivate server

  client->>server:GET https://studies.cs.helsinki.fi/exampleapp/main.css
  activate server
  server-->>client:200 OK: SPA CSS Stylesheet
  deactivate server

  client->server:GET https://studies.cs.helsinki.fi/exampleapp/spa.js
  activate server
  server-->>client:200 OK: SPA JS Script
  deactivate server

  client->server:GET https://studies.cs.helsinki.fi/exampleapp/data.json
  activate server
  server-->>client:200 OK: {{date:"2024-07-31...", content: "abcde", ... }}

```