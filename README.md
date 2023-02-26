# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.\
You will also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).





## Repo setup steps notes
# react-gh-pages
Testing deployment of react codespace code to gh-pages.

Codesapce vs gh-page
Codespace is a live envioremnet for coding, serving a development server for previewing changes while coading.
Free users have 30 hours of free usage of Codesapces.
Codespace is not public.
Github pages (gp-pages) is a github static page made by performing a deploymet, aka making a small bundle from your development code and hosting it on the repos github page.
Free users have an unlimited usage of github page.
Gh-pages are public.
Turn off a codeesapce when not working, use gh-pages to sahre your site with otehrs.

Create a repo called "react-gh-pages"
Go to Codesapces and create a new codesapce, select the previously ccreated repo for the codesapce.
In codesapce create a react app
    npx create-react-app my-app --template typescript
    If you prefer javascript over typescript remove --template typescript
mv my-app/* .
npm install gh-pages --save-dev
code package.json
    Add homepage 
        "name": "my-app",
        "version": "0.1.0",
        + "homepage": "https://gitname.github.io/react-gh-pages",
        "private": true,
    Add deploy and predeploy
        "scripts": {
        +   "predeploy": "npm run build",
        +   "deploy": "gh-pages -d build",
            "start": "react-scripts start",
            "build": "react-scripts build",
To deploy to gh-pages use 
    npm run deploy
or with custom message
    npm run deploy -- -m "Deploy React app to GitHub Pages"
On repo settings select the deployed branch as the repo page
Your repo > Settings > Pages:
    Source: Deploy from a branch
    Branch: gh-pages
    Folder: / (root)
Your repo should be at
    https://gitname.github.io/react-gh-pages/
Commit react development code on main, and the gh-pages branch is used only for deploying the final bundled code as a static site which will remain after you turn off codespace for free.
I've used the launch,json from
    https://github.com/github/codespaces-react
    Run your app with the debugger and a popup will open a new tab to view your app served by  the codespaces (not by gh-pages).

Turn off your codesapce when youre not developing !
