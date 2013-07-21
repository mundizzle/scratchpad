## Scratchpad

Real Time HTML editor with preview. Uses [ACE Editor](https://github.com/mundizzle/scratchpad)

Hopefully useful for quickly trying out some HTML/CSS and even JS ideas and seeing how they look in a browser.

Inspired by [Scratchpad](http://scratchpad.io)

## Things to know

#### LocalStorage
Scratchpad saves and retrieves documents using the brower's localStorage. The document's ID is the ```location.hash```

For example ```http://mundizzle.github.io/scratchpad/#cool_codez``` will create an entry in localStorage named ```#cool_codez```. You can verify this by typing ```localStorage.getItem('#cool_codez')``` in your browser's JS console.

#### Create new document
You can create a new document by changing the ```location.hash``` to any ID you want.

If no hash is supplied, for example ```http://mundizzle.github.io/scratchpad```, then a hash will be generated via ```new Date().getTime()``` and that will be the ID of the document.

If there is not an entry in localStorage for a given document ID, Scratchpad will make an entry containing some basic HTML boilerplate.

#### Shareable Links

Are supported by appending a querystring parameter of ```code``` to the URL. Scratchpad automatically create a document ID and use the ```code``` value as the document.

Example: ```http://localhost:8080/?code=<b>Boo!</b>```
