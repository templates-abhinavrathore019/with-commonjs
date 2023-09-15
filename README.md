# Template for

commonjs project

# Compatible Versions:

### Node

- v19.7.0

# Initialise project

```bash
npm init
```

# nodemon

- Watches files and restarts the server in case of changes.

## Install

```jsx
npm i nodemon
```

## nodemon.json

- Sample configuration

```json
{
  "restartable": "rs",
  "ignore": [".git", "node_modules/**/node_modules"],
  "verbose": true,
  "execMap": {
    "js": "node --harmony"
  },
  "events": {
    "restart": "osascript -e 'display notification \"App restarted due to:\n'$FILENAME'\" with title \"nodemon\"'"
  },
  "watch": ["test/fixtures/", "test/samples/"],
  "env": {
    "NODE_ENV": "development"
  },
  "ext": "js,json"
}
```

# Final Configuration

## nodemon.json

```jsx
{
    "restartable": "rs",
    "ignore": [
      ".git",
      "node_modules/**/node_modules"
    ],
    "verbose": true,
    "watch": [
      "src/"
    ],
    "ext": "js,json"
  }
```

## package.json

```jsx
{
  "name": "with-commonjs",
  "version": "1.0.0",
  "description": "template project for express + nodejs + commonjs",
  "main": "src/app.js",
  "scripts": {
    "dev": "cross-env NODE_ENV=development nodemon",
    "prod": "cross-env NODE_ENV=production nodemon",
    "test": "jest"
  },
  "repository": {
    "type": "git",
    "url": ""
  },
  "keywords": [
    "express",
    "nodejs",
    "dotenv",
    "crossenv",
    "commonjs"
  ],
  "author": "deltacap019",
  "license": "ISC",
  "dependencies": {
    "axios": "1.5.0",
    "cross-env": "7.0.3",
    "dotenv": "16.3.1",
    "express": "4.18.2",
    "express-async-handler": "1.2.0",
    "joi": "17.10.1",
    "mongoose": "7.5.0",
    "node-cache": "5.1.2"
  },
  "devDependencies": {
    "nodemon": "3.0.1"
  }
}
```

# Template

```jsx
npx degit "https://github.com/templates-deltacap019/with-commonjs.git" "my_proj"
```
