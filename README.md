# How to set up a react project using npm, compile it through browsify, and add to .html through script tag

1. Install Node.js

2. Create a new dir and cd into it. Through the terminal run `npm init`

3. Run `npm install --save react react-dom`

4. Create a `src/` and `build/` folder. The src folder is used as the dev env, and build is where the compiled js file will be placed.

5. Create an `index.html` file and place any html content in it.

6. Create an `index.js` file. Make sure to import `react` and `react-dom` using `require('react')` and `require('react-dom')` respectively. Finally, make sure the file contains `ReactDOM.render()`

7. Run `npm install -g browserify`

8. Run `npm install --save babelify babel-preset-react babel-preset-es2015`

9. Run `browserify -t [ babelify --presets [ react es2015 ] ] src/index.js -o build/app.js` to build the compiled js file into the build dir.

10. (OPTIONAL) Create a script for the previous command in `package.json`. 

Note: This allows you to add the compiled app.js file to your html through the script tag, but is a pain for developing compared to create-react-app.

This project is a tldr of the article found here:
https://codeutopia.net/blog/2016/01/25/getting-started-with-npm-and-browserify-in-a-react-project/