Exercise 06: 
Create a diagram depicting the situation where the user creates a new note using the single-page version of the app https://studies.cs.helsinki.fi/exampleapp/spa.

```mermaid
sequenceDiagram
    participant browser
    participant server

    browser->>server: POST https://fullstack-exampleapp.herokuapp.com/new_note_spa
    activate server
    server-->>browser [{ "content": "Exercise 06 is easy", "date": "2025-2-4" }, ... ]
    deactivate server

    Note right of browser: The event handler creates a new note, adds it to the notes list, rerenders the notes list on the page, and sends the new note to the server.
```