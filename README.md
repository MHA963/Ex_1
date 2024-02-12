# Lecture 01 exercises

## Exercise 01-1

### Install Node.js and Postman

Before we can start building great APIs, we need to make sure everything is up and running.

1. Go to https://nodejs.org/en/ and grap the latest Long Term Support (LTS) version of Node.js for your operating system.

Fire up your favorite terminal (Bash, Z shell, PowerShell, Command Prompt, etc.) and make sure the versions checks out with the following commands:

- `node -v` (should print at least `v20.11.0`)
- `npm -v` (should print something like `9.9.2`)

If everything checks out, we are ready to rumble!

Since the focus of this course will be to build APIs it is a good idea to have some sort of tool to test the endpoints we are building. We recommend Postman, get it @ https://www.postman.com/.

## Exercise 01-2

### Hello, Node.js

1. Create a new directory for your application
2. Create a main file for your application (usually, the main file is called `index.js`, but it can be anything)
3. Run `npm init`<sup>(<a href="https://docs.npmjs.com/cli/v9/commands/npm-init">docs</a>)</sup> in the directory to create a `package.json` file
4. Open `index.js` and copy/paste the code from `examples/hello-node/hello-node.js`
5. Run the application with `node index.js`
6. Add another endpoint at `/ping`, which responds with `pong`
7. Test it out using Postman
8. Write comments in your own words in the file explaining each statement and/or function(s)

## Exercise 01-3

### Set up TypeScript and local debugging  

Follow this guide to use Typescript together with Node: https://betterstack.com/community/guides/scaling-nodejs/nodejs-typescript/

## Exercise 01-4

### Convert project 01-2 to use TypeScript and Nodemon

Were you getting tired of constantly restarting your application manually when you did Exercise 01-2?

Install Nodemon as shown in this guide in the section "Watching file changes": https://blog.logrocket.com/how-to-set-up-node-typescript-express/#running-typescript-node-ts-node

## Exercise 01-5

### Building your first Express API

Now that we have tinkered with the basic building blocks in Node.js, it is time to build something a bit more complex. We will be introducing Express.js<sup>(<a href="http://expressjs.com/">docs</a>)</sup> to help increase our productivity.

1. Follow steps 1-3 from Exercise 01-2 to create a fresh package (You can add `nodemon` as well, if you feel like it)
2. Add Express.js to the package (run `npm i express` in the package root directory)
3. Since Express does not include type definitions, we'll have to add them manually with `npm i --save @types/express` 
4. Inspect the in `examples/hello-node/http-methods-and-routes.js` and implement the API with Express.js
    - An endpoint at `/` with `GET` and `POST` that returns data with `Content-Type: text/plain`
    - An endpoint at `/json` with `GET` and `POST` that returns data with `Content-Type: application/json`
    - There should be a separate `Router` for each endpoint (see `examples/multi-router`)
5. Write down the main differences between the vanilla Node.js and Express.js implementation.

_Hints: Problems parsing HTTP bodies? Check out https://github.com/expressjs/body-parser for more information_
