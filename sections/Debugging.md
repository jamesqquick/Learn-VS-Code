# Debugging

1. Creating Your First Debug Configuration
    1. What we’ll cover
        1. Exploring the features of the built in debugging tools
        2. Learn how VS Code tracks debug configuration
        3. Create and run a debug configuration for Client Side JavaScript
    2. Resources
        1. [VS Code Docs](https://code.visualstudio.com/docs/editor/debugging)
        2. [Debugger For Chrome](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-chrome)
    3. Pro Tips
        1. True debugging is much more efficient than using console.log() statements.  Spent the time to learn the tools and it will make you a better developer.

```json
{
    "type": "chrome",
    "request": "launch",
    "name": "Launch Chrome against localhost",
    "url": "http://localhost:8080",
    "webRoot": "${workspaceFolder}"
}
```

2. Debug Configurations for Server Side JavaScript (Node.js)
    1. What we’ll cover
        1. Create and run a debug configuration for Server Side JavaScript
    2. Resources
        1. [VS Code Docs](https://code.visualstudio.com/docs/editor/debugging)

Launch Node (replace program with your server file)

```json
{
    "type": "node",
    "request": "launch",
    "name": "Launch Program",
    "program": "${workspaceFolder}/app.js"
}
```

Attach to Process (you will need to run your application first with `node --inspect server.js`)

```json
{
    "type": "node",
    "request": "attach",
    "name": "Attach by Process ID",
    "processId": "${command:PickProcess}"
}
```

Attach to Port (you will need to run your application first with `node --inspect server.js`)

```json
{
    "type": "node",
    "request": "attach",
    "name": "Attach",
    "port": 9229
}
```

Attach to Port using Nodemon (you will need to run your application first with `nodemon --inspect server.js`)

```json
{
    "type": "node",
    "request": "attach",
    "name": "Attach",
    "port": 9229,
    "restart": true
}
```

3. Debugging Angular CLI Applications
    1. What we’ll cover
        1. Create and run a debug configuration Angular
    2. Resources
        1. [VS Code Docs](https://code.visualstudio.com/docs/editor/debugging)

Angular CLI Applications (you will need to start your Angular app yourself with `npm start` or `ng serve`)

```json
{
    "type": "chrome",
    "request": "launch",
    "name": "Launch Chrome against localhost for Angular",
    "url": "http://localhost:4200",
    "webRoot": "${workspaceFolder}"
}
```

4. Debugging Create React App Applications
    1. What we’ll cover
        1. Create and run a debug configuration Angular
    2. Resources
        1. [VS Code Docs](https://code.visualstudio.com/docs/editor/debugging)

Create React App Applications (you will need to start your app with `npm start`)

```json
{
    "type": "chrome",
    "request": "launch",
    "name": "Launch Chrome against localhost for React",
    "url": "http://localhost:3000",
    "webRoot": "${workspaceFolder}/src"
}
```

5. Debugging Vue CLI Applications
    1. What we’ll cover
        1. Create and run a debug configuration Angular
    2. Resources
        1. [VS Code Docs](https://code.visualstudio.com/docs/editor/debugging)
        2. [Debugging Vue CLI Apps in VS Code](https://vuejs.org/v2/cookbook/debugging-in-vscode.html)

Vue CLI Applications (you will need to start your app with `npm start`)

```json
 {
    "type": "chrome",
    "request": "launch",
    "name": "vuejs: chrome",
    "url": "http://localhost:8080",
    "webRoot": "${workspaceFolder}/src",
    "breakOnLoad": true,
    "sourceMapPathOverrides": {
    "webpack:///src/*": "${webRoot}/*"
    }
}
```
