# Creación de una nueva nota en una SPA

```mermaid
sequenceDiagram
    participant browser
    participant server

     Note right of browser: El usuario escribe una nueva nota y hace clic en "Save"
    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    server-->>browser: 201 new_note_spa (Nota creada con éxito)
    deactivate server
    

    Note right of browser: El navegador actualiza dinámicamente la lista de notas
