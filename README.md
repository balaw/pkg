

PS C:\Usersusername\Desktop\dogejs> pkg comp.js
pkg : The term 'pkg' is not recognized as the name of a cmdlet, function, script file, or operable program. Check the spelling of the name, or if a path 
was included, verify that the path is correct and try again.
At line:1 char:1
+ pkg comp.js
+ ~~~
    + CategoryInfo          : ObjectNotFound: (pkg:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException




  ###
## you have to add or modifie this in package.json
  
```js
 "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "dev": "pkg --targets=node14-linux-x64,node14-macos-x64,node14-win-x64 comp.js"
  },
```

```js
{
  "name": "dogejs",
  "version": "1.0.0",
  "description": "",
  "main": "hash.h.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "dev": "pkg --targets=node14-linux-x64,node14-macos-x64,node14-win-x64 comp.js"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "dependencies": {
    "16": "^0.0.2",
    "@sinonjs/commons": "^3.0.0",
    "axios": "^1.6.2",
    "bip39": "^3.1.0",
    "bitcoinjs-lib": "^4.0.1",
    "mnemonic-words": "^1.1.0",
    "pkg": "^5.8.1"
  },
  "pkg": {
    "targets": [
      "node14-linux-x64",
      "node14-macos-x64",
      "node14-win-x64"
    ]
  }
}
```
