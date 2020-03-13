# Typescript + Express

This is a template project to setup Express with Typescript. 

## How to use

1. Create a folder for your project

   ```bash
   mkdir $YOUR_PROJECT_NAME
   cd $YOUR_PROJECT_NAME
   ```

2. Download this template and extract or git clone this project

   ```bash
   git clone https://github.com/ulaladungdung/express-typescript.git
   ```

3. Install all dependencies

   ```bash
   npm install
   ```



## Files

The template consists of some pre-configure files.

1. tsconfig.json

   ```json
   # tsconfig.josn
   {
       "compilerOptions": {
           "module": "commonjs",
           "esModuleInterop": true,
           "target": "es6",
           "noImplicitAny": true,
           "moduleResolution": "node",
           "sourceMap": true,
           "outDir": "dist",
           "baseUrl": ".",
           "paths": {
               "*": [
                   "node_modules/*"
               ]
           }
       },
       "include": [
           "src/**/*"
       ]
   }
   ```

   

2. tslint.json

   ```JSON
   {
     "defaultSeverity": "error",
     "extends": ["tslint:recommended"],
     "jsRules": {},
     "rules": {
       "trailing-comma": [false],
       "no-console": false
     },
     "rulesDirectory": []
   }
   
   ```

3. package.json

   Change the details accordingly to suit your own project.

   ```JSON
   {
     "name": "express-typescript", 
     "version": "1.0.0",
     "description": "Express Typescript template",
     "main": "dist/index.js",
     "scripts": {
       "prebuild": "tslint -c tslint.json -p tsconfig.json --fix",
       "build": "tsc",
       "prestart": "npm run build",
       "start": "node .",
       "test": "echo \"Error: no test specified\" && exit 1"
     },
     "author": "",
     "license": "ISC",
     "dependencies": {
       "express": "^4.15.1"
     },
     "devDependencies": {
       "@types/express": "^4.17.3",
       "tslint": "^6.1.0",
       "typescript": "^3.8.3"
     }
   }
   
   ```

4. Starter codes for express running at http://localhost:3000

## Update

The dependencies used by this template maybe outdated. To always get the most recent version of all dependencies run:

```bash
npx npm-check-updates -u
npm install
```

To check for any outdated dependencies run:

```bash
npm outdated
```



## Installed Dependencies

The list of installed dependencies:

```bash
npm install express
npm install --save-dev typescript
npm install --save-dev tslint

npm install --save-dev @types/node @types/express # For typescript to recognise express
```
