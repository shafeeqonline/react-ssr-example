# React Server Side Rendering
A baseline for server side rendering for your React application. This repo has a couple of tags that follow building full support for rendering React applications on the server.

## Getting started
Clone the repo with
```git clone https://github.com/shafeeqonline/react-ssr```

Install dependencies with
```npm i```

Run dev mode with
```npm run dev```

Now open the browser and navigate to `http://localhost:2048` and you get your server rendered React app. You can inspect the page source and see that the html coming from your local server has all the nodes defined in the React app.

### A few notes
* I tried to limit the complexity of the entire app to focus on the server side rendering part. Don't take the same shortcuts in your production app!
* We're starting the server with the `index.js` file which is in the root folder. This file loads the babel-register and sets up the babel plugins needed to run JSX and ESModules on the server.
* The node server needs to handle the static files from the `dist` folder.
* The entry point of the bundle is called `client.js` because it's the only part of our application that is not used for the server render.