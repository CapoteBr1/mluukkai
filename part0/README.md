PART 0 

  //EXERCISE 4
  
    title Untitled
    browser->server: HTTP POST https://studies.cs.helsinki.fi/exampleapp/new_note
    server-->browser: HTTP status code 302
    browser->server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/notes
    server-->browser: HTML-code
    browser->server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/main.css
    server-->browser: main.css
    browser->server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/main.js
    server-->browser: main.js

    note over browser:
    browser starts executing js-code
    that requests JSON data from server 
    end note

    browser->server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/data.json
    server-->browser: [{ content: "HTML is easy", date: "2019-05-23" }, ...]

    note over browser:
    browser executes the event handler
    that renders notes to display
    end note


  //EXERCISE 5
  
    browser->server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/spa
    server-->browser: HTML-code
    browser->server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/main.css
    server-->browser: main.css
    browser->server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/main.js
    server-->browser: main.js

    note over browser:
    browser starts executing js-code
    that requests JSON data from server 
    end note

    browser->server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/data.json
    server-->browser: [{ content: "HTML is easy", date: "2019-05-23" }, ...]

    note over browser:
    browser executes the event handler
    that renders notes to display
    end note


  // EXERCISE 6
  
    title Untitled
    browser->server: HTTP POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    server-->browser: "note created"

    note over browser:
    The server responds with status code 201 created.
    This time the server does not ask for a redirect, the browser
    stays on the same page, and it sends no further HTTP requests.
    end note
    

