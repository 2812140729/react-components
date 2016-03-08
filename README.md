# React Components

This repository is used to distribute reusable React components.

## Installation

We use node 5.x and npm 3.x, so you may need to download a new version of node. The easiest way is to download [nvm](https://github.com/creationix/nvm). We have a `.nvmrc` file in the root of the project, so you can just run `nvm use` to switch to the correct version of node.

Install dependencies by running the following in the root of the project:
 - `npm i`
 - **Note:** You must use npm 3. Type `npm -v` to ensure you have a 3.x version.

## NPM Commands
- To run locally, run `npm run dev` and head to `localhost:8080`
- To create the build: `npm run build`
- To run the test runner: `TODO: need to update`
- To make sure your code passes linting: `npm run lint`

## Recommended Developer Tools

Syntax highlighting for ES6 and React JSX
- Install [babel](https://packagecontrol.io/packages/Babel) via the package manager in Sublime Text
  - **Note:** Sublime Text 3 is required for this plugin
- Set the plugin as the default syntax for a particular extension
  - Open a file with the `.js` extension
  - Select `View` from the menu
  - Then `Syntax -> Open all with current extension as...`
  - Then `Babel -> JavaScript (Babel)`
  - Repeat for any other extensions, e.g. `.jsx`

Recommended Theme
- Install [Oceanic Next Color Theme](https://github.com/voronianski/oceanic-next-color-scheme) via the Sublime Text package manager.
- Add the following to `Sublime Text -> Preferences -> Settings-User` (`⌘ + ,` on Mac)
```
{
  "color_scheme": "Packages/Oceanic Next Color Scheme/Oceanic Next.tmTheme",
  "theme": "Oceanic Next.sublime-theme"
}
```

Code expander
- Examples:
  - `div.cool-class` becomes `<div className="cool-class"></div>`
  - `a` becomes `<a href=""></a>`
- Install [Emmet](https://github.com/sergeche/emmet-sublime) via Sublime Text package manager
- Configure Emmet to work with React, e.g. classes expand to `className` instead of `class`
- Follow the instructions under [Get Emmet working](http://www.nitinh.com/2015/02/setting-sublime-text-react-jsx-development/)
  - **Note:** Add the last snippet of code to `reg_replace.sublime-settings` by navigating to  `Sublime Text -> Preferences -> Package Settings -> Reg Replace -> Settings-User`

JavaScript linting
- `npm run lint` will lint your files for you. Please make sure all `.jsx` and `.js` code passes linting, otherwise the Travis build will fail.

Automatic JavaScript linting in Sublime Text
- Install [SublimeLinter](http://sublimelinter.readthedocs.org/en/latest/installation.html) following the instructions under "Installing via Package Control"
- Install [SublimeLinter-eslint](https://github.com/roadhump/SublimeLinter-eslint) with the package manager. The package is called `SublimeLinter-contrib-eslint`

## Contributing

### Style Guide and Naming Conventions

Please use `npm run lint` to make sure your code follows the proper code style specifications for ES6.

### Pull Requests

To contribute to the repository, please create a feature branch off of the dev branch. Once you're finished working on the feature, make a pull request to merge it into dev. Please make sure that every pull request has passed the build checks, which appear just before the "Merge pull request" button in github.

### Adding New Content

SCSS Files
  - Use SCSS syntax, but do not overly nest
  - Use variables, mixins, and classes as much as possible from our [style guide](https://github.com/appirio-tech/styles)
  - When adding media queries, nest them inside the element, rather than creating a new section
  ```
  .box {
    height: 50px;
    width: 50px;
    @media screen and (min-width: 768px) {
      height: 100px;
      width: 100px;
    }
    
    .inside-box {
      font-size: 14px;
      @media screen and (min-width: 768px) {
        font-size: 18px;
      }
    }
  }
  ```
  - This repository uses flexbox for arranging content. The use of any extra CSS libraries should be discussed with the team

JavaScript
  - See this section on [naming conventions and style guide](https://github.com/appirio-tech/topcoder-app/blob/dev/README.md#style-guide-and-naming-conventions)

## Using React Components in your app

## Install

```
npm install appirio-tech-react-components
```

## Developing

```
nvm use
npm install
npm run dev
```
