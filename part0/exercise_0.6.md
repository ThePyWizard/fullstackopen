**Question:** Create a diagram depicting the situation where the user creates a new note using the single-page version of the app.

**Answer:**

```mermaid
sequenceDiagram
    participant browser
    participant server
    
    browser->>server: HTTP POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    Note right of browser: Content-type: application/json <br/> {"content": "HAYYA","date": "2023-03-18T03:07:28.840Z"}
    server-->>browser: 201 created
    deactivate server
    
    Note right of browser: Browser executes the event handler that renders notes to display
```
