#Angular 2 - Simple Setup
This repo provides a set of instructions on how to get started with Angular 2. You may choose to just clone the repo and use it as is, or you can start from scratch by following the instructions provided below.

The repo only has the bare minimum of files. It includes no fancy package management, test setup, modules or application structure.

**Assumptions**: 

* you've got node installed (i.e. npm command is available)

###Commands run to generate this setup:

1. `npm init`
    * Creates your `package.json` file which describes the node package you're building
1. `npm install tsd --save-dev` (package.json updated)
    * Installs `tsd`, which is the TypeScript definition manager that is used to download the TypeScript definition files needed for Angular 2 development in TypeScript
3. `tsd install angular2 es6-promise rx rx-lite`
    * Installs the TypeScript definition files for the listed modules
4. `touch index.html app.ts` (**see comments in the files for details**)
    * These files represent our landing page and application, respectively. The application is loaded from the landing page.
5. `npm install typescript --save-dev`
    * Installs TypeScript as a development dependency (package.json updated)
6. `npm install tsc --save-dev`
    * Installs the TypeScript compiler as a development dependency (package.json updated)
7. `npm install http-server`
    * Installs the software we'll use to serve our `index.html` and related files
8. `npm install bower --save-dev
	* Installs `bower` in order to be able to do the next step
9. `bower install traceur-runtime` (if running as root, include the --allow-root option)
    * Installs `traceur-runtime`, which is needed because the official "5 min quickstart" includes some not working links. 

###To compile the TypeScript file (continuously)
`tsc --watch -m commonjs -t es5 --emitDecoratorMetadata --experimentalDecorators app.ts`

###To run
`http-serve` and open the URL it prints


###Credits
This repo largely contains what is found in these instructions:
[https://angular.io/docs/js/latest/quickstart.html](https://angular.io/docs/js/latest/quickstart.html)
