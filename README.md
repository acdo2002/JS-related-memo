# JS-related-memo
### Record the problem I met and the solution
-------------
Probelm:
Cannot use export/import with Node.js

Solution:
1. install two packages: babel-cli and babel-preset-env and save them both as dev dependancies.
npm init
npm install babel-cli babel-preset-env --save-dev

2. compile:
./node_modules/.bin/babel-node main.js

export.js: the js file contains the export function
main.js (compile this with babel-node): the js file contains the import function

References:
https://medium.com/@JedaiSaboteur/import-export-babel-and-node-a2e332d15673 <br>
https://medium.com/10coding/node-js-%E4%BD%BF%E7%94%A8-babel-%E5%81%9A-es6-%E9%96%8B%E7%99%BC-44b5b9e5f508 <br>

-------------
Problem:
Change the reading behavior inside module/class <br>
for instance:<br>
original: greet(){} <--> console.log(xxx.greet()) <br>
changed: get greet(){} <--> console.log(xxx.greet) <br>
 
tsc cannot compile. 
error TS1056: Accessors are only available when targeting ECMAScript 5 and higher.

Solution:
tsc --target es5 script.ts

References:
https://stackoverflow.com/questions/41010780/accessors-are-only-available-when-targeting-ecmascript-5-and-higher <br>
