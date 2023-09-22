# Typewriter Animation README

This repository contains source code for a simple typewriter animation effect using HTML and CSS. 

[Link to Typewriter Animation Video](./animation.gif)

There are two main files in this project:

## index.html
This HTML file defines the structure of the web page and includes a reference to an external CSS file for styling. The contents of the HTML file are as follows:

``` html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Text Typing Animation Tutorial</title>

    <link rel="stylesheet" href="./styles.css" type="text/css" />
  </head>
  <body>
    <h1>Text Typing Animation</h1>
  </body>
</html>
```

## styles.css
This CSS file defines the styling and animation for the typewriter effect. It uses CSS variables to control background color and animation steps. Here's the content of the CSS file:
    
``` css
:root {
  --bg-color: #000000;
  --animation-steps: 21;
}

body {
  background-color: var(--bg-color);
  font-family: monospace;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}

h1 {
  color: #eee;
  font-size: 5rem;
  font-weight: 400;
  position: relative;
}

h1::before,
h1::after {
  content: '';
  position: absolute;
  inset: 0;
}

h1::before {
  background: var(--bg-color);
  animation: typewriter 2.5s steps(var(--animation-steps)) 500ms forwards;
}

h1::after {
  margin-left: 0.4rem;
  width: 0.125rem;
  background: #6a6a6a;
  animation: typewriter 2.5s steps(var(--animation-steps)) 500ms forwards,
    blink 1000ms steps(var(--animation-steps)) infinite;
}

@keyframes typewriter {
  to {
    left: 100%;
  }
}

@keyframes blink {
  to {
    background: transparent;
  }
}
```

This code creates a typewriter animation effect on the `<h1>` element of the HTML page.

Feel free to explore and modify these files to understand and customize the typewriter animation for your own use. Enjoy experimenting with this simple animation!
