## Scratchpad

Real time HTML editor with preview. Uses [ACE Editor](https://github.com/mundizzle/scratchpad)

Hopefully useful for quickly trying out some HTML/CSS and even JS code and seeing how it looks.

Inspired by [Scratchpad](http://scratchpad.io)

For more substantial coding excercises, I highly recommend more capable and featureful apps like..

- [Codepen](http://codepen.io)
- [JSFiddle](http://jsfiddle.net)
- [JSBin](http://jsbin.com)
- [Dabblet](http://dabblet.com)


## Things to know

### LocalStorage
Scratchpad saves and retrieves documents using the brower's localStorage. The document's ID is the ```location.hash```

For example ```http://mundizzle.github.io/scratchpad/#cool_codez``` will create an entry in localStorage named ```#cool_codez```. You can verify this by typing ```localStorage.getItem('#cool_codez')``` in your browser's JS console.

### Create new document
You can create a new document by changing the ```location.hash``` to any ID you want.

If no hash is supplied, for example ```http://mundizzle.github.io/scratchpad```, then a hash will be generated via ```new Date().getTime()``` and that will be the ID of the document.

If there is not an entry in localStorage for a given document ID, Scratchpad will make an entry containing some basic HTML boilerplate.

### Shareable Links

Are supported by appending a querystring parameter of ```code``` to the URL. Scratchpad automatically create a document ID and use the ```code``` value as the document.

Example: ```http://localhost:8080/?code=<b>Boo!</b>```

### JavaScript Evaluation

Scratchpad does not evaluate JS real time like it does for HTML & CSS. Instead, if the document contains any ```<script>``` tags, a lightning bolt icon will appear. Clicking this will execute the JS code.

Scratchpad does not currently support script tags with src (```<script src="">```) from servers that are not CORS enabled.

### Browser Compatibility

Only tested on Mac Chrome/Firefox/Safari latest
