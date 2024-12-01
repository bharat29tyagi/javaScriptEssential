# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

# Deploy using Github Pages

To deploy your react application in GitHub you need to install "gh-pages". This allows you to use it as a tool for deploying your project to GitHub Pages. 

1. Perform given command in the terminal:

    npm install gh-pages --save-dev

2. Add given lines before "build": "vite build" in package.json file.

    "predeploy": "npm run build",
    "deploy": "gh-pages -d dist",

3. Then in the vite.config.js file add this line before plugins: [react()]

    base: "/YOUR_REPOSITORY_NAME",
    
    Note: Instead of <YOUR_REPOSITORY_NAME> write your own repository name such as assume if your github repository name is learning_react the it should look like base: "/javaScriptEssential".

4. Now perform deploy command in the terminal to executes the "deploy" script defined in the package.json file, deploying the project to GitHub Pages using the gh-pages tool.

    npm run deploy

