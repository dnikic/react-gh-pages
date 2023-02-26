# react-gh-pages

```
Testing deployment of react codespace code to gh-pages.

Codesapce vs gh-page
Codespace is a live envioremnet for coding, serving a development server for previewing changes while coading.
Free users have 30 hours of free usage of Codesapces.
Codespace is not public.
Github pages (gp-pages) is a github static page made by performing a deploymet, aka making a small bundle from your development code and hosting it on the repos github page.
Free users have an unlimited usage of github page.
Gh-pages are public.
Turn off a codeesapce when not working, use gh-pages to sahre your site with otehrs.

Base for understanding gh-pages
    https://github.com/gitname/react-gh-pages
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
    https://github.com/codespaces
    Thre dots near the name of your codesapace, and press STOP

On android use Kiwi browser to inspect or debug if youre having problems with the final built app.


My link shortcuts:
https://github.com/dnikic/react-gh-pages/settings/pages
https://dnikic.github.io/react-gh-pages/
https://github.com/gitname/react-gh-pages



```