# Node-How-To

## Check if you have node installed

- node -v

## Setting up a Node Project

- mkdir my-project-name
- cd my-project-name
- npm init |
  unless specified Node with look for a file called "index.js" as an entry point for running your project
- node index.js |
  run "node filename.js" to run your js file in your terminal

## Creating, Exporting and Importing Modules

create myModule.js

- module.exports |
  In Node, module.exports is an object that will hold the code to be exported. We can use dot-notation to add the code we want to export to this object
- module.exports.varName = () => console.log("That's so fetch!") |
  Now, our module.exports object has a key-value pair where the key is "varName" and the value is a function.
- const myModule = require('./myModule.js)
- myModule.varName() |
  This is where the require function, specific to Node, comes into play. This function takes one argument: the path to the file that contains the module you are exporting to index.js.
- node index.js |

## fs module

We will use the "fs" core module (it stands for "file system") to read a text file.

- story.txt |
  Core modules just need to be imported using the "require" function.
- const fs = require('fs')
- fs.readFile('story.txt', 'utf8', function(err, data){
  if(err) {
  console.log("There was a problem reading the file.");
  } else {
  console.log(data);
  }
  });
- node index.js |
  Try adding to your story using fs.write()

## Nodemon

- npm i -g nodemon / npm instal -g nodemon |
  Since we're installing it globally (that's where the -g flag comes in), it doesn't matter what directory we're in.
  We installed nodemon globally, but most node packages will only be useful for specific projects. In this case, when you run npm i [package name] you want to make sure you're inside the directory of the project you want to use the package in, and leave off the -g flag.

## Third Party Modules

- npm i package-name |
  Make sure there is a folder called node_modules in your folder

## .gitignore

We can specify directions to git about which files it should ignore by creating a file called .gitignore. Yes, the . at the front is necessary!
A .gitignore file will contain a list of files and folders that git should NOT be tracking. Go ahead and make a .gitignore file now and put node_modules into it as the first line.
