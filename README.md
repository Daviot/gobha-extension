# gobha-extension

A [Metalsmith](www.metalsmith.io) plugin to change the file extension of the file

Can be used to create static sites, but with some more possibilities in dynamic web hosts. 

Every file that match the `extension` option will be converted into an *.html file.  
**Example**: `/test/demo.md` will become `/test/demo.html` 


## Installation

	$ npm install gobha-file-to-path

## Javascript Usage

```js
let file_to_path = require('gobha-file-to-path')

metalsmith.use(file_to_path())
```

## Options

```js
{
	extension: "html|php|md|hbs"
}
```
#### extension

The plugin checks every file extension and when the extension matches the regex it will process the file and change the file extension

## Change file extension

It's possible to use other file extensions then html.  
Just add a new meta information into the file itself to set the extension

```md
---
ext: php
---
```

The new meta ext will tell this site that the new file extension should be .php

**Example:** `file.md` with the meta `ext: php` will become `file.php`

Now it's possible to add PHP code into the site to process form data.

## License
MIT