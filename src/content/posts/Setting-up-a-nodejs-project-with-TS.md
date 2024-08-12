---
title: "Setting up a Node.js Express project with Typescript"
description:
pubDate: "Aug 02 2024"
---

Setting up a Node.js project with TypeScript can significantly improve your developer experience by providing static type checking in your code. In this blog, I'll guide you through the steps to set up a Node.js Express project with TypeScript.

**Create your project directory**

Create a directory for your project and then navigate to it. In this example the name of our directory is **_node-ts_**.

```
mkdir node-ts
cd node-ts
```

**Initialize the project**

Install a new node project with **_npm init_**. This will create a **_package.json_** file in the root of your project.

```
npm init
```

**Install TypeScript**

Install TypeScript as a development dependancy.

```
npm install --save-dev typescript
```

**Initialize the TypeScript configuration file**

```
npx tsc --init
```

**Set up your project structure**

Create directories for your source (src) and compiled files (dist).

```
mkdir src
mkdir dist
```

**Install development tools**

Install **_nodemon_** and **_ts-node_** as development dependencies to run and monitor your project.

```
npm install nodemon ts-node --save-dev
```

**Configure scripts**

Configure a script in the **_package.json_** to run your server in development mode.

```
"scripts": {
    "dev": "nodemon --exec ts-node src/server.ts"
  }
```

**Configure nodemon**

Create a **_nodemon.json_** file to configure **_nodemon_** to watch the TypeScript files.

```
{
  "watch": ["src"],
  "ext": "ts,json",
  "exec": "ts-node ./src/server.ts"
}
```

**Configure TypeScript**

In the **_tsconfig.json_**, specify the compiler options and include your source files.

```
{
  "compilerOptions": {
    "target": "es2016",
    "module": "commonjs",
    "rootDir": "./src",
    "outDir": "./dist",
    "esModuleInterop": true,
    "forceConsistentCasingInFileNames": true,
    "strict": true,
    "skipLibCheck": true
  },
  "include": ["src/**/*.ts"]
}
```

**Install Express**

```
npm install express
npm install @types/express --save-dev
```

**Create a simple express server**

Create a **_server.ts_** file in your **_src/_** directory with the following basic set up for an express server.

```
import express from 'express';

const app = express();
const port = process.env.PORT || 3000;

app.get('/', (req, res) => {
  res.send('Hello, TypeScript with Node.js and Express!');
});

app.listen(port, () => {
  console.log(`Server is running at http://localhost:${port}`);
});

```

**Start the development server**

To start the server run the script you configured in your **_package.json_** file.

```
npm run dev
```

Your Node.js Express with TypeScript project should be up and running now.
