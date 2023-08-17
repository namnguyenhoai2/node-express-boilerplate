# 1. yarn install


# 2. Husky, GitHub Desktop commit error: cannot find module yarn.js

So the problem is, there is no C:\Users\user\AppData\Local\GitHubDesktop\app-3.1.2\resources\app\git\node_modules\yarn\bin\yarn.js

My first assumption is that there is no npm initialized in the git folder. Let's check:

1- Open Powershell
2- Type cd C:\Users\user\AppData\Local\GitHubDesktop\app-3.1.2\resources\app\git to set the directory
3- Type explorer . to view the folder in File Explorer

screenshot from the git folder

So we see no node_modules, package.json or package-lock.json. This means that npm is not initialized in this current directory.

To add the missing ...\git\node_modules\yarn\bin\yarn.js:

1- Run npm init to initialize npm in the directory.
2- Run npm i yarn to add yarn dependency to the current directory.

This way, we have added the missing ...\git\node_modules\yarn\bin\yarn.js file.
Now everything works fine!