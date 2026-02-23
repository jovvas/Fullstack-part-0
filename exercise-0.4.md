```mermaid
<<<<<<< HEAD
sequence diagram
=======
sequenceDiagram
>>>>>>> f6778d27bb595db38e0a202cee8fec5b8e057621
    participant browser
    participant server

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note 
    activate server
    server->>browser: redirection of the request 
    deactivate server

    Note left of server: Server asks the browser to perform a new HTTP GET request

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/notes 
    activate server
    server->>browser: HTML document
<<<<<<< HEAD
    deactivate server0

    Notes right of browser: The browser reloads the Notes page

    browser->>server GET https://studies.cs.helsinki.fi/exampleapp/main.css 
    activate server
    server->>browser: CSS file
    deactivate browser

    browser->>server GET https://studies.cs.helsinki.fi/exampleapp/main.js 
=======
    deactivate server

    Note right of browser: The browser reloads the Notes page

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.css 
    activate server
    server->>browser: CSS file
    deactivate server

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.js 
>>>>>>> f6778d27bb595db38e0a202cee8fec5b8e057621
    activate server
    server->>browser: JavaScript file
    deactivate server

    Note right of browser: Browser executes JavaScript that fetches JSON from the server

<<<<<<< HEAD
    browser->>server GET https://studies.cs.helsinki.fi/exampleapp/data.json 
    activate server
    server->>browser: JSON file 

    Note right of browser: Browser runs callback function to render notes
```
=======
    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/data.json 
    activate server
    server->>browser: JSON file
    deactivate server

    Note right of browser: Browser runs callback function to render notes
```
>>>>>>> f6778d27bb595db38e0a202cee8fec5b8e057621
