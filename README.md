# Learn Nodejs

This is a repository for learning Node.js. It contains a collection of resources to learn Node.js from scratch. It includes topics like Node.js, NPM, Modules, Events, File System, HTTP, Express, RESTful API, MongoDB, Mongoose, Authentication, Authorization, Validation, Unit Testing, Integration Testing, Test Driven Development, Deployment, Security, Performance, Scalability, Design Patterns, Error Handling, Logging, Debugging, Monitoring, CI/CD, Docker, Microservices, GraphQL, Websockets, TypeScript, ES6, and Best Practices.

## Table of Contents

- [Introduction](#introduction)
- [Prerequisites](#prerequisites)
- [Environment Setup](#environment-setup)
  - [Windows](#windows)
  - [macOS](#macos)
  - [Linux](#linux)
- [ECMAScript](#ecmascript)
  - [ES5 (ES2009)](#es5-es2009)
  - [ES6 (ES2015)](#es6-es2015)
- [Chrome's V8 Engine](#chromes-v8-engine)
- [JavaScript Runtime](#javascript-runtime)
- [Node.js](#nodejs)
- [Features of Node.js](#features-of-nodejs)
- [Node.js Architecture](#nodejs-architecture)
- [Node.js Applications](#nodejs-applications)
- [Node.js Use Cases](#nodejs-use-cases)
- [Node.js Advantages](#nodejs-advantages)
- [Node.js Disadvantages](#nodejs-disadvantages)
- [NPM](#npm)
  - [Installation of NPM](#installation-of-npm)
  - [Usage](#usage)
  - [package.json](#packagejson)
  - [Semantic Versioning](#semantic-versioning)
  - [NPM Scripts](#npm-scripts)
  - [NPM Modules](#npm-modules)
  - [NPM Registry](#npm-registry)
  - [NPM CLI](#npm-cli)
- [Modules](#modules)
  - [Creating Modules](#creating-modules)
  - [Exporting Modules](#exporting-modules)
  - [Importing Modules](#importing-modules)
  - [Built-in Modules](#built-in-modules)
  - [Custom Modules](#custom-modules)
  - [Local Modules](#local-modules)
  - [Module Scope](#module-scope)
  - [Module Wrapper](#module-wrapper)
  - [Module Caching](#module-caching)
  - [ES Modules](#es-modules)
  - [Importing JSON and Watch Mode](#importing-json-and-watch-mode)
  - [Path Module](#path-module)
  - [OS Module](#os-module)
  - [URL Module](#url-module)
  - [Query String Module](#query-string-module)
  - [Crypto Module](#crypto-module)
  - [Zlib Module](#zlib-module)
  - [Stream Module](#stream-module)
  - [Child Process Module](#child-process-module)
  - [Cluster Module](#cluster-module)
- [Callback Pattern](#callback-pattern)
- [Events](#events)
  - [EventEmitter](#eventemitter)
  - [Event Loop](#event-loop)
  - [Event Emitter Patterns](#event-emitter-patterns)
- [Character Sets and Encoding](#character-sets-and-encoding)
- [Streams](#streams)
- [Buffers](#buffers)
- [Asynchronous JavaScript](#asynchronous-javascript)
- [File System](#file-system)
  - [Reading Files](#reading-files)
  - [Writing Files](#writing-files)
  - [Deleting Files](#deleting-files)
  - [Renaming Files](#renaming-files)
- [Pipes](#pipes)
- [HTTP](#http)
  - [Creating a Server](#creating-a-server)
  - [Handling Requests](#handling-requests)
  - [Routing](#routing)
  - [Query Strings](#query-strings)
  - [Redirects](#redirects)
- [Thread](#thread)
- [libuv](#libuv)
- [Worker Threads](#worker-threads)
- [Queue](#queue)
  - [Microtask Queue](#microtask-queue)
  - [Timer Queue](#timer-queue)
  - [I/O Queue](#io-queue)
  - [Check Queue](#check-queue)
  - [Close Queue](#close-queue)
  - [I/O Polling](#io-polling)
  - [Network I/O](#network-io)
  - [Timers](#timers)
- [Promises](#promises)
- [Creating a Node Server](#creating-a-node-server)
  - [JSON Responses](#json-responses)
  - [HTML Responses](#html-responses)
  - [HTML Templates](#html-templates)
- [Web Framework](#web-framework)
  - [Libraries and Frameworks](#libraries-and-frameworks)
- [Express](#express)
  - [Installation of Express](#installation-of-express)
  - [Hello World with Express](#hello-world-with-express)
  - [Middleware Functions with Express](#middleware-functions-with-express)
  - [Routing with Express](#routing-with-express)
  - [Template Engines with Express](#template-engines-with-express)
  - [Static Files with Express](#static-files-with-express)
  - [Error Handling with Express](#error-handling-with-express)
- [RESTful API](#restful-api)
  - [HTTP Methods](#http-methods)
  - [Endpoints](#endpoints)
  - [Status Codes](#status-codes)
  - [JSON](#json)
  - [CRUD Operations](#crud-operations)
  - [Authentication](#authentication)
  - [Authorization](#authorization)
  - [Validation](#validation)
  - [Pagination](#pagination)
  - [Filtering](#filtering)
  - [Versioning](#versioning)
  - [HATEOAS](#hateoas)
- [MongoDB](#mongodb)
- [Mongoose](#mongoose)
- [Authentication](#authentication)
- [Authorization](#authorization)
- [Validation](#validation)
- [Unit Testing](#unit-testing)
- [Integration Testing](#integration-testing)
- [Test Driven Development](#test-driven-development)
- [Deployment](#deployment)
- [Security](#security)
- [Performance](#performance)
- [Scalability](#scalability)
- [Design Patterns](#design-patterns)
- [Error Handling](#error-handling)
- [Logging](#logging)
- [Debugging](#debugging)
- [Monitoring](#monitoring)
- [CI/CD](#cicd)
- [Docker](#docker)
- [Microservices](#microservices)
- [GraphQL](#graphql)
- [Websockets](#websockets)
- [TypeScript](#typescript)
- [ES6](#es6)
- [Best Practices](#best-practices)

## Introduction

- Node.js is an open-source, cross-platform, JavaScript runtime environment that executes JavaScript code outside a web browser.
- Node.js lets developers use JavaScript to write command line tools and for server-side scripting.
- Node.js represents a "JavaScript everywhere" paradigm, unifying web application development around a single programming language, rather than different languages for server- and client-side scripts.

## Prerequisites

- Before you start learning Node.js, you should have a basic understanding of JavaScript.

## Environment Setup

- You can run Node.js on Windows, macOS, and Linux.

### Windows

- You can download Node.js from the official website [nodejs.org](https://nodejs.org/).
- You can also install Node.js using a package manager like `chocolatey` & `fnm`.

    ```bash
    # download and install Node.js
    choco install nodejs-lts --version="20.14.0"

    # verifies the right Node.js version is in the environment
    node -v # should print `20`
    
    # verifies the right NPM version is in the environment
    npm -v # should print `10.7.0`
    ```

    ```bash
    # installs fnm (Fast Node Manager)
    winget install Schniz.fnm

    # download and install Node.js
    fnm use --install-if-missing 20

    # verifies the right Node.js version is in the environment
    node -v # should print `v20.14.0`

    # verifies the right NPM version is in the environment
    npm -v # should print `10.7.0`
    ```

### macOS

- You can download Node.js from the official website [nodejs.org](https://nodejs.org/).
- You can also install Node.js using a package manager like `brew`.

    ```bash
    brew install node
    ```

### Linux

- You can download Node.js from the official website [nodejs.org](https://nodejs.org/).
- You can also install Node.js using a package manager like `apt`.

    ```bash
    sudo apt install nodejs
    ```

- You can also install Node.js using a package manager like `nvm`.

    ```bash
    # installs nvm (Node Version Manager)
    curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash

    # download and install Node.js (you may need to restart the terminal)
    nvm install 20

    # verifies the right Node.js version is in the environment
    node -v # should print `v20.14.0`

    # verifies the right NPM version is in the environment
    npm -v # should print `10.7.0`
    ```

## ECMAScript

- ECMAScript is the standard upon which JavaScript is based, and it's often abbreviated to ES.

### ES5 (ES2009)

- ECMAScript 5 (ES5) is the fifth edition of the ECMAScript standard.
- ES5 was published in December 2009 and was widely adopted by all modern web browsers.

### ES6 (ES2015)

- ECMAScript 6 (ES6) is the sixth edition of the ECMAScript standard.
- ES6 was published in June 2015 and is also known as ECMAScript 2015.

## Chrome's V8 Engine

- V8 is Google's open-source high-performance JavaScript and WebAssembly engine, written in C++.
- It is used in Chrome and in Node.js, among others.

## JavaScript Runtime

- A JavaScript runtime is a program that executes JavaScript code.
- Node.js is a JavaScript runtime built on Chrome's V8 JavaScript engine.

## Node.js

- Node.js is a JavaScript runtime built on Chrome's V8 JavaScript engine.
- Node.js uses an event-driven, non-blocking I/O model that makes it lightweight and efficient.
- Node.js' package ecosystem, npm, is the largest ecosystem of open source libraries in the world.

## Features of Node.js

- Asynchronous and Event-Driven
- Very Fast
- Single-Threaded but Highly Scalable
- No Buffering

## Node.js Architecture

- Node.js is built on the Google Chrome V8 JavaScript engine.
- It uses a non-blocking, event-driven I/O model.
- It is lightweight and efficient.

## Node.js Applications

- Web Applications
- Real-Time Chat Applications
- RESTful API Applications
- Microservices
- CRON Jobs

## Node.js Use Cases

- I/O Bound Applications
- Data Streaming Applications
- Data Intensive Real-Time Applications (DIRT)
- JSON APIs based Applications
- Single Page Applications

## Node.js Advantages

- Easy to Learn
- Fast Execution
- Large Ecosystem
- Active Community
- Great Performance

## Node.js Disadvantages

- Callback Hell
- Unhandled Exceptions
- Single Threaded
- Not Suitable for CPU Intensive Tasks

## Hello World

```javascript
console.log('Hello, World!');
```

### REPL

- REPL stands for Read-Eval-Print-Loop. It is a simple, interactive computer programming environment.

    ```bash
    $ node
    > console.log('Hello, World!');
    Hello, World!
    undefined
    >
    ```

### Command Line Arguments

- You can access command line arguments using `process.argv`.

    ```javascript
    process.argv.forEach((val, index) => {
    console.log(`${index}: ${val}`);
    });
    ```

### Environment Variables

- You can access environment variables using `process.env`.

    ```javascript
    console.log(process.env.HOME);
    ```

### Global Objects

- Node.js global objects are global in nature and available in all modules.

    ```javascript
    console.log(__dirname);
    console.log(__filename);
    ```

## NPM

- npm is the package manager for JavaScript and the world’s largest software registry.
- npm consists of a command line client that interacts with a remote registry.

### Installation of NPM

- npm comes with Node.js. You only need to install Node.js to get npm.

### Usage

- You can install packages using `npm install <package-name>`.
- You can install packages globally using `npm install -g <package-name>`.
- You can install packages as development dependencies using `npm install --save-dev <package-name>`.
- You can uninstall packages using `npm uninstall <package-name>`.
- You can update packages using `npm update <package-name>`.
- You can search packages using `npm search <package-name>`.
- You can list packages using `npm list`.

### package.json

- The `package.json` file is the heart of a Node.js project.
- It contains metadata about the project, such as the name, version, description, and dependencies.

    ```json
    {
    "name": "my-app",
    "version": "1.0.0",
    "description": "My first Node.js app",
    "main": "index.js",
    "scripts": {
        "start": "node index.js"
    },
    "dependencies": {
        "express": "^4.17.1"
    },
    "devDependencies": {
        "jest": "^26.6.3"
    }
    }
    ```

### Semantic Versioning

- Semantic Versioning is a versioning scheme based on three numbers: major, minor, and patch.
- A version number is in the format of `MAJOR.MINOR.PATCH`.

    ```json
    {
    "dependencies": {
        "express": "^4.17.1"
    }
    }
    ```

- `^4.17.1` means any version from `4.17.1` to `<5.0.0`.

### NPM Scripts

- You can run scripts using `npm run <script-name>`.

    ```json
    {
    "scripts": {
        "start": "node index.js",
        "test": "jest"
    }
    }
    ```

- You can run `npm start` to start the application.

### NPM Modules

- You can create your own modules using `module.exports`.

    ```javascript
    // math.js
    module.exports.add = (a, b) => a + b;

    // index.js
    const math = require('./math');
    console.log(math.add(1, 2));
    ```

### NPM Registry

- The npm registry is a large public database of JavaScript software and the meta-information surrounding it.

    ```bash
    npm search express
    npm info express
    ```

### NPM CLI

- You can use the npm CLI to manage packages.

    ```bash
    npm install express
    npm install express@4.17.1
    npm install express --save
    npm install express --save-dev
    npm uninstall express
    npm update express
    npm search express
    npm list
    ```

## Modules

- A module encapsulates related code into a single unit of code.
- A module can be included in other modules using `require` function.
- Node.js has a set of built-in modules which you can use without any further installation.

    ```javascript
    const fs = require('fs');
    const http = require('http');
    const url = require('url');
    ```

### Creating Modules

- You can create your own modules using `module.exports`.

    ```javascript
    // math.js
    module.exports.add = (a, b) => a + b;

    // index.js
    const math = require('./math');
    console.log(math.add(1, 2));
    ```

### Exporting Modules

- You can export modules using `module.exports`.

    ```javascript
    // math.js
    module.exports.add = (a, b) => a + b;

    // index.js
    const math = require('./math');
    console.log(math.add(1, 2));
    ```

### Importing Modules

- You can import modules using `require`.

    ```javascript
    // math.js
    module.exports.add = (a, b) => a + b;

    // index.js
    const math = require('./math');
    console.log(math.add(1, 2));
    ```

### Built-in Modules

- Node.js has a set of built-in modules which you can use without any further installation.

    ```javascript
    const fs = require('fs');
    const http = require('http');
    const url = require('url');
    ```

### Custom Modules

- You can create your own modules using `module.exports`.

    ```javascript
    // math.js
    module.exports.add = (a, b) => a + b;

    // index.js
    const math = require('./math');
    console.log(math.add(1, 2));
    ```

### Local Modules

- Local modules are modules that are stored locally in your project.

    ```javascript
    // math.js
    module.exports.add = (a, b) => a + b;

    // index.js
    const math = require('./math');
    console.log(math.add(1, 2));
    ```

### Module Scope

- Each module has its own scope.

    ```javascript
    // math.js
    const PI = 3.14;

    module.exports.area = (r) => PI * r * r;

    // index.js
    const math = require('./math');
    console.log(math.area(5));
    ```

### Module Wrapper

- Node.js wraps each module with a function wrapper.

    ```javascript
    (function (exports, require, module, __filename, __dirname) {
    // Your code here
    });
    ```

### Module Caching

- Node.js caches the modules on the first `require` call.
- Subsequent `require` calls will return the cached module.

    ```javascript
    // math.js
    console.log('math.js is loaded!');

    module.exports.add = (a, b) => a + b;

    // index.js
    console.log('Before require');
    const math = require('./math');
    console.log('After require');
    const math = require('./math');
    ```

### ES Modules

- ES Modules are the official standard format to package JavaScript code for reuse.
- ES Modules are stored in files.

    ```javascript
    // math.js
    export const add = (a, b) => a + b;

    // index.js
    import { add } from './math';
    console.log(add(1, 2));
    ```

### Importing JSON and Watch Mode

- You can import JSON files using ES Modules.

    ```javascript
    // data.json
    {
    "name": "John Doe",
    "email": "john.doe@gmail.com"
    }

    // index.js
    import data from './data.json';
    console.log(data.name);
    ```

- You can use watch mode to automatically reload the application.

    ```bash
    node --experimental-modules --es-module-specifier-resolution=node index.js
    ```

    ```bash
    node --experimental-modules --es-module-specifier-resolution=node --watch index.js
    ```

    ```bash
    node --experimental-modules --es-module-specifier-resolution=node --watch-dir . index.js
    ```

    ```bash
    node --experimental-modules --es-module-specifier-resolution=node --watch-dir . --watch-extensions js, mjs index.js
    ```

### Path Module

- The `path` module provides utilities for working with file and directory paths.

    ```javascript
    const path = require('path');
    console.log(path.dirname('/path/to/file.txt'));
    console.log(path.extname('/path/to/file.txt'));
    console.log(path.basename('/path/to/file.txt'));
    ```

### OS Module

- The `os` module provides operating system-related utility methods.

    ```javascript
    const os = require('os');
    console.log(os.arch());
    console.log(os.cpus());
    console.log(os.freemem());
    ```

### URL Module

- The `url` module provides utilities for URL resolution and parsing.

    ```javascript
    const url = require('url');
    console.log(url.parse('https://example.com'));
    console.log(url.resolve('https://example.com', '/about'));
    ```

### Query String Module

- The `querystring` module provides utilities for parsing and formatting URL query strings.

    ```javascript
    const querystring = require('querystring');
    console.log(querystring.parse('name=John Doe'));
    console.log(querystring.stringify({ name: 'John Doe' }));
    ```

### Crypto Module

- The `crypto` module provides cryptographic functionality.

    ```javascript
    const crypto = require('crypto');
    const hash = crypto.createHash('sha256');
    hash.update('Hello, World!');
    console.log(hash.digest('hex'));
    ```

### Zlib Module

- The `zlib` module provides compression and decompression functionality.

    ```javascript
    const zlib = require('zlib');
    const input = 'Hello, World!';
    zlib.deflate(input, (err, buffer) => {
    if (!err) {
        console.log(buffer.toString('base64'));
    }
    });
    ```

### Stream Module

- The `stream` module provides an API for streaming data.

    ```javascript
    const fs = require('fs');
    const readStream = fs.createReadStream('file.txt');
    const writeStream = fs.createWriteStream('copy.txt');
    readStream.pipe(writeStream);
    ```

### Child Process Module

- The `child_process` module provides the ability to spawn child processes.

    ```javascript
    const { exec } = require('child_process');
    exec('ls -la', (err, stdout, stderr) => {
    if (!err) {
        console.log(stdout);
    }
    });
    ```

### Cluster Module

- The `cluster` module allows you to create child processes that share server ports.

    ```javascript
    const cluster = require('cluster');
    const http = require('http');
    const numCPUs = require('os').cpus().length;

    if (cluster.isMaster) {
    console.log(`Master ${process.pid} is running`);

    for (let i = 0; i < numCPUs; i++) {
        cluster.fork();
    }

    cluster.on('exit', (worker, code, signal) => {
        console.log(`Worker ${worker.process.pid} died`);
    }
    } else {
    http.createServer((req, res) => {
        res.writeHead(200);
        res.end('Hello, World!');
    }).listen(8000);

    console.log(`Worker ${process.pid} started`);
    }
    ```

## Callback Pattern

- A callback function is a function passed into another function as an argument.
- Callback functions can be synchronous or asynchronous.

    ```javascript
    const fs = require('fs');
    fs.readFile('file.txt', 'utf8', (err, data) => {
    if (err) throw err;
    console.log(data);
    });
    ```

## Events

- Events in Node.js are actions or occurrences that happen in the system.
- Node.js has a built-in module, `events`, where you can create-, fire-, and listen for- your own events.

### EventEmitter

- Node.js core API is built around an idiomatic asynchronous event-driven architecture in which certain kinds of objects (called "emitters") emit named events that cause Function objects ("listeners") to be called.

    ```javascript
    const EventEmitter = require('events');
    const myEmitter = new EventEmitter();

    myEmitter.on('event', () => {
    console.log('an event occurred!');
    });

    myEmitter.emit('event');
    ```

### Event Loop

- Node.js is a single-threaded application, but it can support concurrency via the concept of an event loop.

### Event Emitter Patterns

- Event Emitter patterns are used to handle events in Node.js.

    ```javascript
    const EventEmitter = require('events');
    class MyEmitter extends EventEmitter {}
    const myEmitter = new MyEmitter();

    myEmitter.on('event', () => {
    console.log('an event occurred!');
    });

    myEmitter.emit('event');
    ```

## Character Sets and Encoding

- A character set is a set of characters that can be used in a language.
- An encoding is a mapping from a character set to a sequence of bytes.

## Streams

- Streams are objects that let you read data from a source or write data to a destination in continuous fashion.

    ```javascript
    const fs = require('fs');
    const read = fs.createReadStream('file.txt');
    const write = fs.createWriteStream('copy.txt');
    read.pipe(write);
    ```

## Buffers

- A buffer is a temporary memory location for data when it is being moved from one place to another.
- Buffers are used to store raw binary data.

    ```javascript
    const buffer = Buffer.from('Hello, World!');
    console.log(buffer.toString());
    ```

## Asynchronous JavaScript

- Asynchronous JavaScript is a programming pattern that provides non-blocking I/O operations.
- Asynchronous JavaScript uses callbacks to handle asynchronous operations.

    ```javascript
    const fs = require('fs');
    fs.readFile('file.txt', 'utf8', (err, data) => {
    if (err) throw err;
    console.log(data);
    });
    ```

## File System

- Node.js includes `fs` module to work with the file system.
- The `fs` module provides file I/O operations using simple wrappers around standard POSIX functions.

### Reading Files

- You can read files using `fs.readFile`.

    ```javascript
    const fs = require('fs');
    fs.readFile('file.txt', 'utf8', (err, data) => {
    if (err) throw err;
    console.log(data);
    });
    ```

### Writing Files

- You can write files using `fs.writeFile`.

    ```javascript
    const fs = require('fs');
    fs.writeFile('file.txt', 'Hello, World!', (err) => {
    if (err) throw err;
    console.log('The file has been saved!');
    });
    ```

### Deleting Files

- You can delete files using `fs.unlink`.

    ```javascript
    const fs = require('fs');
    fs.unlink('file.txt', (err) => {
    if (err) throw err;
    console.log('The file has been deleted!');
    });
    ```

### Renaming Files

- You can rename files using `fs.rename`.

    ```javascript
    const fs = require('fs');
    fs.rename('file.txt', 'newfile.txt', (err) => {
    if (err) throw err;
    console.log('The file has been renamed!');
    });
    ```

## Pipes

- Pipes are used to connect the output of one stream to another stream.

    ```javascript
    const fs = require('fs');
    const read = fs.createReadStream('file.txt');
    const write = fs.createWriteStream('copy.txt');
    read.pipe(write);
    ```

## HTTP

- Node.js has a built-in module, `http`, which allows Node.js to transfer data over the Hyper Text Transfer Protocol (HTTP).
- Node.js has a built-in module, `https`, which allows Node.js to transfer data over secure Hyper Text Transfer Protocol (HTTPS).

### Creating a Server

- You can create an HTTP server using `http.createServer`.

    ```javascript
    const http = require('http');
    const server = http.createServer((req, res) => {
    res.end('Hello, World!');
    });
    server.listen(3000);
    ```

### Handling Requests

- You can handle requests using `req` and `res` objects.

    ```javascript
    const http = require('http');
    const server = http.createServer((req, res) => {
    res.writeHead(200, { 'Content-Type': 'text/plain' });
    res.end('Hello, World!');
    });
    server.listen(3000);
    ```

### Routing

- You can route requests using `url` module.

    ```javascript
    const http = require('http');
    const url = require('url');
    const server = http.createServer((req, res) => {
    const path = url.parse(req.url).pathname;
    if (path === '/') {
        res.writeHead(200, { 'Content-Type': 'text/plain' });
        res.end('Home Page');
    } else if (path === '/about') {
        res.writeHead(200, { 'Content-Type': 'text/plain' });
        res.end('About Page');
    } else {
        res.writeHead(404, { 'Content-Type': 'text/plain' });
        res.end('Not Found');
    }
    });
    server.listen(3000);
    ```

### Query Strings

- You can parse query strings using `url` module.

    ```javascript
    const http = require('http');
    const url = require('url');
    const server = http.createServer((req, res) => {
    const query = url.parse(req.url, true).query;
    res.writeHead(200, { 'Content-Type': 'text/plain' });
    res.end(`Hello, ${query.name}!`);
    });
    server.listen(3000);
    ```

### Redirects

- You can redirect requests using `res.writeHead`.

    ```javascript
    const http = require('http');
    const server = http.createServer((req, res) => {
    res.writeHead(301, { 'Location': 'http://example.com' });
    res.end();
    });
    server.listen(3000);
    ```

## Thread

- Node.js is a single-threaded application, but it can support concurrency via the concept of an event loop.

## libuv

- libuv is a multi-platform support library with a focus on asynchronous I/O.
- Node.js uses the `libuv` library to handle asynchronous operations.

    ```javascript
    const fs = require('fs');
    fs.readFile('file.txt', 'utf8', (err, data) => {
    if (err) throw err;
    console.log(data);
    });
    ```

## Worker Threads

- Worker threads are used to perform CPU-intensive JavaScript operations.

    ```javascript
    const { Worker, isMainThread, parentPort } = require('worker_threads');

    if (isMainThread) {
    const worker = new Worker(__filename);
    worker.on('message', (message) => {
        console.log(message);
    });
    worker.postMessage('Hello, World!');
    } else {
    parentPort.on('message', (message) => {
        parentPort.postMessage(message);
    });
    }
    ```

## Queue

- A queue is a data structure that stores elements in a First-In-First-Out (FIFO) order.

    ```javascript
    class Queue {
    constructor() {
        this.items = [];
    }

    enqueue(element) {
        this.items.push(element);
    }

    dequeue() {
        return this.items.shift();
    }

    front() {
        return this.items[0];
    }

    isEmpty() {
        return this.items.length === 0;
    }

    print() {
        console.log(this.items.toString());
    }
    }

    const queue = new Queue();
    queue.enqueue(1);
    queue.enqueue(2);
    queue.enqueue(3);
    queue.print();
    queue.dequeue();
    queue.print();
    ```

### Microtask Queue

- Microtask Queue is a queue that stores microtasks in a First-In-First-Out (FIFO) order.

    ```javascript
    console.log('Start');

    setTimeout(() => {
    console.log('Timeout');
    }, 0);

    Promise.resolve().then(() => {
    console.log('Promise');
    });

    console.log('End');
    ```

### Timer Queue

- Timer Queue is a queue that stores timers in a First-In-First-Out (FIFO) order.

    ```javascript
    console.log('Start');

    setTimeout(() => {
    console.log('Timeout');
    }, 0);

    console.log('End');
    ```

### I/O Queue

- I/O Queue is a queue that stores I/O operations in a First-In-First-Out (FIFO) order.

    ```javascript
    const fs = require('fs');
    fs.readFile('file.txt', 'utf8', (err, data) => {
    if (err) throw err;
    console.log(data);
    });
    ```

### Check Queue

- Check Queue is a queue that stores check operations in a First-In-First-Out (FIFO) order.

    ```javascript
    setImmediate(() => {
    console.log('Immediate');
    });

    console.log('End');
    ```

### Close Queue

- Close Queue is a queue that stores close operations in a First-In-First-Out (FIFO) order.

    ```javascript
    const server = require('http').createServer();
    server.listen(3000);
    server.close(() => {
    console.log('Server closed');
    });
    ```

### I/O Polling

- I/O Polling is a mechanism that polls the I/O Queue for I/O operations.

    ```javascript
    const fs = require('fs');
    fs.readFile('file.txt', 'utf8', (err, data) => {
    if (err) throw err;
    console.log(data);
    });
    ```

### Network I/O

- Network I/O is a mechanism that handles network I/O operations.

    ```javascript
    const server = require('http').createServer();
    server.listen(3000);
    ```

### Timers

- Timers are used to schedule tasks to be executed in the future.

    ```javascript
    setTimeout(() => {
    console.log('Timeout');
    }, 1000);
    ```

## Promises

- A promise is an object representing the eventual completion or failure of an asynchronous operation.

    ```javascript
    const promise = new Promise((resolve, reject) => {
    setTimeout(() => {
        resolve('Hello, World!');
    }, 1000);
    });

    promise.then((value) => {
    console.log(value);
    });
    ```

### Chaining Promises

- You can chain promises using `then`.

    ```javascript
    const promise = new Promise((resolve, reject) => {
    setTimeout(() => {
        resolve('Hello,');
    }, 1000);
    });

    promise.then((value) => {
    return value + ' World!';
    }).then((value) => {
    console.log(value);
    });
    ```

## Creating a Node Server

- You can create a simple Node server.

    ```javascript
    const http = require('http');
    const server = http.createServer((req, res) => {
    res.end('Hello, World!');
    });
    server.listen(3000);
    ```

### JSON Responses

- You can send JSON responses.

    ```javascript
    const http = require('http');
    const server = http.createServer((req, res) => {
    res.writeHead(200, { 'Content-Type': 'application/json' });
    res.end(JSON.stringify({ message: 'Hello, World!' }));
    });
    server.listen(3000);
    ```

### HTML Responses

- You can send HTML responses.

    ```javascript
    const http = require('http');
    const server = http.createServer((req, res) => {
    res.writeHead(200, { 'Content-Type': 'text/html' });
    res.end('<h1>Hello, World!</h1>');
    });
    server.listen(3000);
    ```

### HTML Templates

- You can use HTML templates.

    ```javascript
    const http = require('http');
    const server = http.createServer((req, res) => {
    res.writeHead(200, { 'Content-Type': 'text/html' });
    res.end(`
        <h1>Hello, World!</h1>
        <p>${new Date()}</p>
    `);
    });
    server.listen(3000);
    ```

### HTTP Routing

- You can create routes using `url` module.

    ```javascript
    const http = require('http');
    const url = require('url');
    const server = http.createServer((req, res) => {
    const path = url.parse(req.url).pathname;
    if (path === '/') {
        res.writeHead(200, { 'Content-Type': 'text/plain' });
        res.end('Home Page');
    } else if (path === '/about') {
        res.writeHead(200, { 'Content-Type': 'text/plain' });
        res.end('About Page');
    } else {
        res.writeHead(404, { 'Content-Type': 'text/plain' });
        res.end('Not Found');
    }
    });
    server.listen(3000);
    ```

## Web Framework

- A web framework is a software framework designed to aid in the development of web applications including web services, web resources, and web APIs.

### Libraries and Frameworks

- There are many web frameworks available for Node.js.

  - Express
  - Koa
  - Hapi
  - Nest
  - Fastify

## Express

- Express is a minimal and flexible Node.js web application framework that provides a robust set of features for web and mobile applications.
- Express provides a thin layer of fundamental web application features, without obscuring Node.js features.

### Installation of Express

- You can install Express using `npm install express`.

### Hello World with Express

- You can create a simple Express application.

    ```javascript
    const express = require('express');
    const app = express();
    app.get('/', (req, res) => {
    res.send('Hello, World!');
    });
    app.listen(3000);
    ```

### Middleware Functions with Express

- Middleware functions are functions that have access to the request object (`req`), the response object (`res`), and the next middleware function in the application’s request-response cycle.

    ```javascript
    const express = require('express');
    const app = express();
    app.use((req, res, next) => {
    console.log('Time:', Date.now());
    next();
    });
    app.get('/', (req, res) => {
    res.send('Hello, World!');
    });
    app.listen(3000);
    ```

### Routing with Express

- You can create routes using `app.get`, `app.post`, `app.put`, and `app.delete`.

    ```javascript
    const express = require('express');
    const app = express();
    app.get('/', (req, res) => {
    res.send('Home Page');
    });
    app.get('/about', (req, res) => {
    res.send('About Page');
    });
    app.listen(3000);
    ```

### Template Engines with Express

- Express supports a variety of template engines.

    ```javascript
    const express = require('express');
    const app = express();
    app.set('view engine', 'pug');
    app.get('/', (req, res) => {
    res.render('index', { title: 'Express' });
    });
    app.listen(3000);
    ```

### Static Files with Express

- You can serve static files using `express.static`.

    ```javascript
    const express = require('express');
    const app = express();
    app.use(express.static('public'));
    app.listen(3000);
    ```

### Error Handling with Express

- You can handle errors using `app.use`.

    ```javascript
    const express = require('express');
    const app = express();
    app.use((err, req, res, next) => {
    console.error(err.stack);
    res.status(500).send('Something broke!');
    });
    app.listen(3000);
    ```

## RESTful API

- REST (Representational State Transfer) is an architectural style for designing networked applications.
- A RESTful API is an application program interface (API) that uses HTTP requests to GET, PUT, POST and DELETE data.

### HTTP Methods

- RESTful APIs use standard HTTP methods.

  - `GET` to retrieve a resource.
  - `POST` to create a resource.
  - `PUT` to update a resource.
  - `DELETE` to delete a resource.

### Endpoints

- RESTful APIs use endpoints to access resources.

  - `GET /api/users` to get all users.
  - `POST /api/users` to create a user.
  - `GET /api/users/:id` to get a user.
  - `PUT /api/users/:id` to update a user.
  - `DELETE /api/users/:id` to delete a user.

### Status Codes

- RESTful APIs use standard HTTP status codes.

  - `200 OK` for successful requests.
  - `201 Created` for successful creation.
  - `400 Bad Request` for invalid requests.
  - `404 Not Found` for missing resources.
  - `500 Internal Server Error` for server errors.

### JSON

- RESTful APIs use JSON (JavaScript Object Notation) to exchange data.

    ```json
    {
        "id": 1,
        "name": "John Doe",
        "email": "johndoe@gmail.com"
    }
    ```

### CRUD Operations

- RESTful APIs use CRUD (Create, Read, Update, Delete) operations.

  - `GET /api/users` to get all users.
  - `POST /api/users` to create a user.
  - `GET /api/users/:id` to get a user.
  - `PUT /api/users/:id` to update a user.
  - `DELETE /api/users/:id` to delete a user.

### Authentication

- RESTful APIs use authentication to secure resources.

  - `Basic Auth` using username and password.
  - `Token Auth` using JWT (JSON Web Tokens).
  - `OAuth` using OAuth 2.0 protocol.

### Authorization

- RESTful APIs use authorization to control access to resources.

  - `Role Based` access control.
  - `Attribute Based` access control.
  - `Policy Based` access control.

### Validation

- RESTful APIs use validation to ensure data integrity.

  - `Input Validation` to validate user input.
  - `Schema Validation` to validate data structure.
  - `Business Rules` to validate business logic.

### Pagination

- RESTful APIs use pagination to limit data.

  - `Limit` to limit the number of records.
  - `Offset` to skip a number of records.
  - `Page` to get a specific page of records.

### Filtering

- RESTful APIs use filtering to search data.

  - `Filter` to search by specific criteria.
  - `Sort` to sort data by specific criteria.
  - `Search` to search by keyword.

### Versioning

- RESTful APIs use versioning to manage changes.

  - `URI Versioning` using the URI path.
  - `Header Versioning` using the request header.
  - `Media Type Versioning` using the request header.

### HATEOAS

- HATEOAS (Hypermedia as the Engine of Application State) is a constraint of the REST application architecture.

  - `Links` to navigate between resources.
  - `Actions` to perform operations on resources.
  - `Forms` to submit data to resources.

## MongoDB

- MongoDB is a cross-platform document-oriented database program.
- Classified as a NoSQL database program, MongoDB uses JSON-like documents with optional schemas.

## Mongoose

- Mongoose is an Object Data Modeling (ODM) library for MongoDB and Node.js.
- It manages relationships between data, provides schema validation, and is used to translate between objects in code and the representation of those objects in MongoDB.

## Unit Testing

- Unit testing is a software testing method by which individual units of source code are tested to determine whether they are fit for use.
- Jest is a delightful JavaScript Testing Framework with a focus on simplicity.

```javascript
// math.js
const add = (a, b) => a + b;

module.exports = add;

// math.test.js

const add = require('./math');

test('adds 1 + 2 to equal 3', () => {
  expect(add(1, 2)).toBe(3);
});
```

## Integration Testing

- Integration testing is the phase in software testing in which individual software modules are combined and tested as a group.
- Supertest is a high-level abstraction for testing HTTP.

    ```javascript
    // app.js
    const express = require('express');
    const app = express();

    app.get('/', (req, res) => {
    res.send('Hello, World!');
    });

    module.exports = app;

    // app.test.js
    const request = require('supertest');
    const app = require('./app');

    test('GET /', async () => {
    const response = await request(app).get('/');
    expect(response.text).toBe('Hello, World!');
    });
    ```

## Test Driven Development

- Test-driven development (TDD) is a software development process that relies on the repetition of a very short development cycle.
- TDD is a programming technique that involves writing tests before writing the actual code.

    ```javascript
    // math.js
    const add = (a, b) => a + b;

    module.exports = add;

    // math.test.js
    const add = require('./math');

    test('adds 1 + 2 to equal 3', () => {
    expect(add(1, 2)).toBe(3);
    });
    ```

## Deployment

- Deployment is the process of making a software system available for use.

## Security

- Security is the degree of resistance to, or protection from, harm.
- Helmet helps secure Express apps by setting various HTTP headers.

    ```javascript
    const express = require('express');
    const helmet = require('helmet');
    const app = express();

    app.use(helmet());
    ```

## Performance

- Performance is a measure of how quickly a system performs a certain process or transaction.
- PM2 is a production process manager for Node.js applications with a built-in load balancer.

    ```bash
    pm2 start app.js
    ```

## Scalability

- Scalability is the capability of a system to handle a growing amount of work, or its potential to accommodate growth.
- Horizontal scaling means that you scale by adding more machines into your pool of resources.

    ```bash
    pm2 start app.js -i max
    ```

    ```bash
    pm2 scale app +3
    ```

    ```bash
    pm2 scale app 2
    ```

## Design Patterns

- Design patterns are typical solutions to common problems in software design.
- Design patterns can speed up the development process by providing tested, proven development paradigms.

    ```javascript
    // Singleton Pattern
    class Singleton {
    constructor() {
        if (!Singleton.instance) {
        Singleton.instance = this;
        }
        return Singleton.instance;
    }
    }

    const instance1 = new Singleton();
    const instance2 = new Singleton();

    console.log(instance1 === instance2);
    ```

## Error Handling

- Error handling is the process of responding to and recovering from error conditions in a program.
- Express has a default error handler, but you can also define custom error handlers.

    ```javascript
    const express = require('express');
    const app = express();

    app.use((err, req, res, next) => {
    console.error(err.stack);
    res.status(500).send('Something broke!');
    });
    ```

## Logging

- Logging is the process of recording events that happen in an application.
- Winston is a versatile logging library for Node.js.

    ```javascript
    const winston = require('winston');
    const logger = winston.createLogger({
    level: 'info',
    format: winston.format.json(),
    defaultMeta: { service: 'user-service' },
    transports: [
        new winston.transports.File({ filename: 'error.log', level: 'error' }),
        new winston.transports.File({ filename: 'combined.log' }),
    ],
    });

    logger.info('Hello, World!');
    ```

## Debugging

- Debugging is the process of finding and resolving defects or problems within a computer program.
- Node.js has a built-in debugging interface.

    ```bash
    node inspect app.js
    ```

    ```bash
    node --inspect app.js
    ```

    ```bash
    node --inspect-brk app.js
    ```

    ```bash
    node --inspect=
    ```

    ```bash
    node --inspect-brk=
    ```

    ```bash
    node --inspect --debug-brk app.js
    ```

    ```bash
    node --inspect --debug-brk=
    ```

    ```bash
    node --inspect --debug-brk --inspect-brk app.js
    ```

    ```bash
    node --inspect --debug-brk --inspect-brk=
    ```

    ```bash
    node --inspect --debug-brk --inspect-brk= app.js
    ```

## Monitoring

- Monitoring is the process of observing and checking the progress or quality of a program over time.
- PM2 provides a monitoring feature.

    ```bash
    pm2 monit
    ```

## CI/CD

- Continuous Integration (CI) is the practice of merging all developer working copies to a shared mainline several times a day.
- Continuous Deployment (CD) is a strategy for software releases wherein any code commit that passes the automated testing phase is automatically released into the production environment.

```yaml
name: CI

on:
  push:
    branches:
      - main

jobs:
    build:
        runs-on: ubuntu-latest
    
        steps:
        - uses: actions/checkout@v2
    
        - name: Use Node.js
        uses: actions/setup-node@v2
        with:
            node-version: '14'
    
        - name: Install Dependencies
        run: npm install
    
        - name: Run Tests
        run: npm test
```

```yaml
name: CD

on:
    push:
        branches:
        - main

jobs:
    deploy:
        runs-on: ubuntu-latest

        steps:
        - uses: actions/checkout@v2

        - name: Use Node.js
        uses: actions/setup-node@v2
        with:
            node-version: '14'

        - name: Install Dependencies
        run: npm install

        - name: Build
        run: npm run build

        - name: Deploy
        run: |
            npm install -g pm2
            pm2 start app.js
```

## Docker

- Docker is a set of platform as a service products that use OS-level virtualization to deliver software in packages called containers.
- A Docker container image is a lightweight, standalone, executable package of software that includes everything needed to run a piece of software.

```dockerfile
# Dockerfile
FROM node:14

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

EXPOSE 3000

CMD ["node", "app.js"]
```

```bash
docker build -t my-app .
docker run -p 3000:3000 my-app
```

## Microservices

- Microservices is a variant of the service-oriented architecture (SOA) architectural style that structures an application as a collection of loosely coupled services.
- Each service is self-contained and should implement a single business capability.

## GraphQL

- GraphQL is a query language for APIs and a runtime for executing those queries by using a type system you define for your data.
- GraphQL is a specification for how to communicate with APIs.

    ```javascript
    const { ApolloServer, gql } = require('apollo-server');

    const typeDefs = gql`
    type Query {
        hello: String
    }
    `;

    const resolvers = {
    Query: {
        hello: () => 'Hello, World!',
    },
    };

    const server = new ApolloServer({ typeDefs, resolvers });

    server.listen().then(({ url }) => {
    console.log(`Server ready at ${url}`);
    });
    ```

## Websockets

- WebSockets is a communication protocol that provides full-duplex communication channels over a single TCP connection.
- Socket.IO enables real-time, bidirectional and event-based communication.

    ```javascript
    const http = require('http');
    const server = http.createServer();
    const io = require('socket.io')(server);

    io.on('connection', (socket) => {
    console.log('a user connected');
    socket.on('disconnect', () => {
        console.log('user disconnected');
    });
    });

    server.listen(3000);
    ```

## TypeScript

- TypeScript is an open-source programming language developed and maintained by Microsoft.
- TypeScript is a strict syntactical superset of JavaScript and adds optional static typing to the language.

    ```typescript
    // math.ts
    const add = (a: number, b: number): number => a + b;

    export default add;

    // index.ts
    import add from './math';

    console.log(add(1, 2));
    ```

## ES6

- ECMAScript 6, also known as ECMAScript 2015, is the latest version of the ECMAScript standard.
- ES6 includes significant enhancements to the language, such as arrow functions, classes, template literals, and let + const.

    ```javascript
    // ES6 Arrow Functions
    const add = (a, b) => a + b;

    // ES6 Classes
    class Math {
    add(a, b) {
        return a + b;
    }
    }

    // ES6 Template Literals
    const name = 'John Doe';
    console.log(`Hello, ${name}!`);

    // ES6 Destructuring
    const [a, b] = [1, 2];
    console.log(a, b);

    // ES6 Spread Operator
    const a = [1, 2];
    const b = [3, 4];
    const c = [...a, ...b];
    console.log(c);
    ```

## Best Practices

- Best practices are a set of guidelines, ethics or ideas that represent the most efficient or prudent course of action.
- Node.js best practices include error-first callbacks, event emitters, streams, and middleware.

    ```javascript
    // Error-First Callbacks
    fs.readFile('file.txt', (err, data) => {
    if (err) throw err;
    console.log(data);
    });

    // Event Emitters
    const EventEmitter = require('events');
    const myEmitter = new EventEmitter();

    myEmitter.on('event', () => {
    console.log('an event occurred!');
    });

    myEmitter.emit('event');

    // Streams
    const fs = require('fs');
    const readStream = fs.createReadStream('file.txt');

    readStream.on('data', (data) => {
    console.log(data);
    });

    // Middleware
    const express = require('express');
    const app = express();

    app.use((req, res, next) => {
    console.log('Time:', Date.now());
    next();
    });
    ```

## Connect with me

- [Twitter](https://twitter.com/manthan_ank)
- [LinkedIn](https://www.linkedin.com/in/manthanank)
- [Facebook](https://www.facebook.com/manthanank/)
- [Instagram](https://www.instagram.com/manthan_ank/)
- [YouTube](https://www.youtube.com/@manthanank)
- [GitHub](https://github.com/manthanank)

## Support

If you like this learning repository and find it useful, consider buying me a coffee or sponsoring me through the GitHub Sponsor. Your support will help me to continue and bring more exciting projects. Thank you!

[![Buy Me A Coffee](/assets/bmc-button.svg)](https://www.buymeacoffee.com/manthanank)

[![Sponsor Me](https://img.shields.io/badge/Sponsor-GitHub-green)]([https://](https://github.com/sponsors/manthanank))

---

Show your support by 🌟 the repository.

---
