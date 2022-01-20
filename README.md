# Install and Manage Tools

## Error: The engine "node" is incompatible with this module

- Update node.js

## Node.js

- Update Node.js on Windows

  1. Update Node.js with the installer, https://nodejs.org/en/download/

  - `node -v`

  - Updating Node.js by downloading the installer from the official page is easy. While this is a straight forward process, at times the system may fail to overwrite the older Node.js release resulting in two instances of Node.js. If that problem occurs, follow the second method to install Node.js on Windows with NPM.

  2. Update Node.js with NPM

  - ```bash
    node -v
    npm cache clean -f
    npm install -g n
    sudo n stable         // sudo n latest    // sudo n [version.number]
    node -v
    ```

## Error: command not found on Windows

- After a package installed global by `yarn global add package`, when it was run, it returned the error.

### Solution:

- Get the location of the yarn global binary, `yarn global bin`

- Add the binary path to PATH environment variable

  - Click on Windows button then search with `environment` and click on `Edit the system environment variables`.

  - On `System Properties` dialog, click on `Environment Variables...` button.

  - Select `Path` on `User variables for user` and click on `Edit...` button.

  - Click on `New` button to add the path of the yarn global binary, and click `OK`

  - Restart vscode

## Error: cannot find module 'typescript/bin/tsc'

- When I had installed typescript globally and ran tsc-watch, the error happened.

### Solution:

- Go to the global package folder, `cd c:/Users/[UserName]/AppData/Local/Yarn/Data/global/node_modules/typescript`

- Register the package, `yarn link`

  - The results have the package name, `success Registered "typescript".`

- Go to the project which you want to link

- Link the package, `yarn link typescript`
