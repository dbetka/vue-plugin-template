# vue-plugin-template
Template for vue plugin project with SASS and global imports for SASS.

## Installation
```
npm i -D @dbetka/vue-plugin-template
```

## Building
```
npm run build                   Build js and css bundles from all js, vue and sass files.

npm run build-plugin            Build js bundle from js and vue files.

npm run build-css               Build css bundles from all sass files (run all scripts includes css in name).

npm run build-full-css          Build one css bundle from all sass files.
npm run build-wigets-css        Build css bundles for each sass component file which will has included base-file.sass on the beginning.
npm run build-themes-css        Build css bundles for each sass theme file.
```

## Usage outside of plugin

#### Full Bundle
```js
import VueAtomic from '@dbetka/vue-plugin-template'
import '@dbetka/vue-plugin-template/dist/index.css'

Vue.use(VueAtomic)
```

### Individual components
with default name
```js
import { OwnButton } from '@dbetka/vue-plugin-template'
import '@dbetka/vue-plugin-template/dist/own-button.css'

Vue.component(OwnButton.name, OwnButton) // component name is m-input
```
with own name
```js
import { OwnButton } from '@dbetka/vue-plugin-template'
import '@dbetka/vue-plugin-template/dist/own-button.css'

Vue.component('new-button', OwnButton) // component name is new-input
```

## Project maintenance 

Scripts used in `package.json` has own docs [here](scripts/README.md)
