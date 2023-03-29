# eslint-config-ferns

An eslint and prettier set up for fullstack dev: Node, React, and React Native

# Installation

Install the config and its peer dependencies:

    yarn add -D eslint-config-ferns \
      @typescript-eslint/eslint-plugin@^5.57.0 \
      @typescript-eslint/parser@^5.57.0 \
      eslint@^8.37.0 \
      eslint-config-prettier@^8.8.0 \
      eslint-plugin-import@^2.27.5 \
      eslint-plugin-lodash@^7.1.0 \
      eslint-plugin-prettier@^4.2.1 \
      eslint-plugin-react@^7.32.2 \
      eslint-plugin-react-native@^4.0.0 \
      eslint-plugin-react-hooks@^4.6.0 \
      eslint-plugin-simple-import-sort@^10.0.0 \
      eslint-plugin-unused-imports@2.0.0\
      prettier@^2.8.7 \
      typescript@~5.0.2

## Update package.json

Add:

     "eslintConfig": {
       "extends": [
         "ferns"
       ],
       "settings": {
         "react": {
           "version": "detect"
         }
       }
     },


Note: Even if you aren't using React in the project (for example, your API), add this to suppress a warning.

# Usage

Add to your NPM scripts in package.json:

    "scripts": {
      ...
      "lint": "eslint \"src/**/*.ts*\"",
      "lintfix": "eslint --fix \"src/**/*.ts*\"",
    }

Then run:

    yarn lintfix

    yarn lint
