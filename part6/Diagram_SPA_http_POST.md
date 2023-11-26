  browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa
  activate server
  server-->>browser: HTML SPA document
  deactivate server

  browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
  activate server
  server-->>browser: the css file
  deactivate server

  browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa.js
  activate server
  server-->>browser: the JS SPA file
  deactivate server

  browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
  activate server
  server-->>browser: the JSON file
  deactivate server

  browser->>server: POST {"content": "soy un post en una SPA","date": "2023-11-26T16:23:46.109Z"} https://studies.cs.helsinki.fi/exampleapp/new_note_spa
  activate server
  server-->>browser: {"message":"note created"}
  deactivate server
