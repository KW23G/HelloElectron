# HelloElectron

This is an Electron test app.

You should also take a look at https://www.electronjs.org/docs/tutorial/first-app

## What you have to do:

1. Download npm and node.js from https://nodejs.org/en/

2. Run ```npm init``` in your project folder

3. Open package.json and change it to:

```
{
  "name": "your-app",
  "version": "0.1.0",
  "main": "main.js",
  "scripts": {
    "start": "electron ."
  }
}
```

4. Run ```npm install --save-dev electron``` to install electron for the project

5. create an ```index.html``` and ```main.js``` file. In ```index.html``` you can just write normal frontend,
but you need to paste the following code into ```main.js```:

```
const { app, BrowserWindow } = require('electron')

function createWindow () {
  // Create the browser window.
  let win = new BrowserWindow({
    width: 800,
    height: 600,
    webPreferences: {
      nodeIntegration: true
    }
  })

  // and load the index.html of the app.
  win.loadFile('index.html')
}

app.whenReady().then(createWindow)
```
Of course you can change the code (examples on https://www.electronjs.org/docs/tutorial/first-app#electron-development-in-a-nutshell)

6. To run your app, just do ```npm start``` in the project directory (Don't worry if electron creates some new files / ...)

## Tip:

NodeJS will automatically create a folder called ```node_modules```. Because this folder is too big to be pushed to GitHub,
you can create a ```.gitignore``` file in the Repository and add ```path/to/node_modules/``` to the created file.
Now, Git just ignores that folder, so you don't have to worry about this large, no huge, folder.
