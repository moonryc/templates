# VITE React + Typescript + ESlint + Prettier Template

## Table Of Context

* [Vite](#Vite)
* [Vite Plugins](#Vite Plugins)
* [ESLint and Prettier ](#ESLint and Prettier)
  * [Dependencies](#Dependencies)
  * [ESLint](#ESLint)
  * [Prettier](#Prettier)

## Vite

Set up the React project using Vite. To Accomplish this run the command ```yarn create vite```. This may take a moment,
Vite will then ask you what to name your project and what type of project. Select React and then choose the typescript
option.

## Vite Plugins

Vite does not include the plugins and types needed to import SVGs as components. To solve this, install
this [package](https://www.npmjs.com/package/@svgr/rollup) and add the plugin to ```vite.config.ts```

NOTE:

If you are using typescript then in the root of the React application create ```svg.d.ts``` and paste this into the file:
```
declare module '*.svg' {
  import * as React from 'react'
  export const ReactComponent: React.FunctionComponent<React.SVGProps<SVGSVGElement> & { title?: 'string' }>
}
```

Finally, add the recently created file to ts.config.json ex. ```"include": ["src", "svg.d.ts"],```

## ESLint and Prettier

* ### Dependencies

    ```yarn add @typescript-eslint/eslint-plugin @typescript-eslint/parser eslint eslint-config-prettier eslint-plugin-prettier eslint-plugin-react prettier -D```

* ### ESLint
  * See the .eslintrc.json file for eslint settings for react
  * See the .eslintignore file

* ### Prettier
  * See the .prettierrc.json file for eslint settings for react
  * See the .prettierignore file
