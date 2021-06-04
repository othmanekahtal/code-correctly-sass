# Code Correctly SASS !

## Setup environment for sass :

- for config and setup environment for sass automatically :

  ```bash
  npm i install
  ```

  You can config and setup environment manually :

- 1- initialize npm for your project :

  ```bash
  npm init
  ```

- 2- install sass :

  ```bash
  npm i sass --save-dev
  ```

  to installing sass globally :

  ```bash
  npm i sass -g
  ```

- 3- install PostCSS-cli and autoprefixer (for auto prefixed your css to be supported in all browsers ):

  ```bash
  npm install postcss-cli autoprefixer --save-dev
  ```

- 5-install npm-run-all to run multiple npm-scripts in parallel or sequential:
  ```bash
  npm i npm-run-all --save-dev
  ```

## Getting started :

### Explain 7-1 SASS architecture :

It is always a good idea to keep things organized, today let’s organize SASS code. It’s really good for Front-End Developers and especially for Big projects.

Let me explain one of the best SASS architecture so-called 7-1 SASS architecture :

`Abstracts\ :`

> The abstract folder is different from other folders. Styles written in this folder do not compile to CSS. They are the helpers for other folders. Two major SASS Abstracts are variables,mixins,functions,placeholders,responsive rules,etc.

`Base\`

> The base folder is like a foundation style for the project,like a redefine rem unit and reset the style of the default HTML elements.

`Layout\`

> The layout folder contains the style for a website layout.This folder includes style for the navbar, sidebar, footer, header, etc.

`Components\`

> Components are a set of codes which has their character. It might be just one HTML element or a block of HTML elements.like : Alert box, button, label, badge, list group, panel, modal are some of the common components we see on websites.

`Pages\`

> The pages folder covers the style of specific pages. like a contact us,home,services,etc.

`Themes\`

> Themes folder is related to look of your project. It could be Light theme, dark theme, blue theme, etc..

`Vendors\`

> This Folder contains all external styles or 3rd party styles are placed in it. libraries,frameworks.
> The most commonly used vendors are Bootstrap,bulma,animate.css,tailwind.css,etc.

`main.scss`

> This file is the main sass file,that's will converted to css
> this file contains an access for other files like a components and responsive rules and more..

`When we have a web site contains a multi pages, we need to add sass file that contains components and requirement like: example_page.scss`

### Start coding Now :

<br>

**1-Development Mode :**

- To watch all changes happens in sass architecture :

  ```bash
  npm sass --watch sass/:dist/
  ```

  or use :

  ```bash
  npm run watch:sass
  ```

- To compile sass to css :

  ```bash
  npm sass sass/:dist/
  ```

  or use :

  ```bash
  npm run compile:sass
  ```

- To auto prefix all css files :

  ```bash
  npx postcss --use autoprefixer dist/ -o dist/
  ```

  or use :

  ```bash
  npm run prefix:css
  ```

- To compress css files :

  ```bash
  npm sass dist/*.css dist/*.compress.css --style=compressed
  ```

  or use :

  ```bash
  npm run compress:css
  ```

- To build all files :

  ```bash
  npm npm-run-all compile:sass prefix:css compress:css
  ```

  or use :

  ```bash
  npm run build
  ```

## Contributing :

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.😉

`enjoy !`
