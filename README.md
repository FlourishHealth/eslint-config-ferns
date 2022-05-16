# eslint-config-ferns
An eslint and prettier set up for fullstack dev: Node, React, and React Native

# Installation

Install the config and its peer dependencies:

    yarn add -D eslint-config-ferns \
      @typescript-eslint/eslint-plugin@^5.23.0 \
      @typescript-eslint/parser@^5.23.0 \
      eslint@^8.15.0 \
      eslint-config-prettier@^8.5.0 \
      eslint-plugin-import@^2.26.0 \
      eslint-plugin-lodash@^7.1.0 \
      eslint-plugin-prettier@^4.0.0 \
      eslint-plugin-react@^7.29.4 \
      eslint-plugin-react-native@^4.0.0 \
      eslint-plugin-simple-import-sort@^7.0.0 \
      prettier@^2.6.2 \
      typescript@~4.1.5
    
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
