# Creating an npm package

## Getting Started
### Initial steps
- Create a new git repo for your npm package and clone it locally.

- Create an 'index.js' file and a 'README.md' file.

- In the package folder type `npm init -y` to generate a 'package.json' file

### In the 'package.json' file
- Change the name of the package to have '@stuvascript/' in front of the package name to scope it to your npm account. Also make sure the package name is what you want because it defaults to what you saved it as locally.

- Change version to '0.1.0' to indicate its not ready yet.

- Give it a brief description

- Add your npm name as the author.

- Change license to 'MIT'

### Next
- Type `npm whoami` and your npm name should pop up. If not, type `npm login` or go login on the npm site.

- Your package needs to have 'export' or 'export default' on the functions for them to be imported by another project and utilized. See your other packages for examples. (Normally you would use 'module.exports' for this but you're utilizing ES6 modules and not Common.js right now.)

## Testing
- To test your package, in your package folder type `npm link`.

- Then in another folder you want to link it to for testing, type `npm link {package name (including the '@stuvascript/' scope)}`. Because your package folder and project folder are now linked, if you make changes in either folder it will automatically update it in both the project folder and the package folder.

## Finish
- To publish your SCOPED package PUBLICLY, type `npm publish --access public` to publish it to the npm registry. Each time you make an update and publish again, make sure you update the semantic versioning or it won't let you publish.

- When your package is complete, change the version to '1.0.0'

## To use in a project
- Pretty sure you need Webpack to do any sort of browser stuff since node.js is a backend tool.

- Type `npm init -y` in the new project. To install the package type `npm i {name of project}`. On your package's page there will be an 'Install' spot on the right that you can copy pasta instead if you want.

- In your new project, Use the 'import' function to import the functions from the package. (Normally you would use the 'require' function assigned to a variable for this but you're utilizing ES6 modules and not Common.js right now.)

## Links
### Videos
- [Swashbuckling with Code - "How to Create and Publish an NPM Package"](https://www.youtube.com/watch?v=WRjJW8tseQg)
- [JavaScript Mastery - "Learn how to deploy an NPM Package"](https://www.youtube.com/watch?v=8FziherTC8M)
- [Web Dev Simplified - "How To Create And Publish Your First NPM Package"](https://www.youtube.com/watch?v=J4b_T-qH3BY)
- [codedamn - "How to create and publish NPM Packages?"](https://www.youtube.com/watch?v=rTsz09zRuTU)
### The official docs
- [npm Docs](https://docs.npmjs.com/about-packages-and-modules)
