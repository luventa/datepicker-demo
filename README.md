# datepicker-demo

> A Vue.js project

# What i did
`vue init webpack datepicker-demo`

## install dependencies
`yarn install`

# install datepicker and bulma
`yarn add vue-bulma-datepicker bulma`

# install loaders
`yarn add node-sass sass-loader stylus stylus-loader --dev`

# add an exclude to rules.
add exclude: [new RegExp(`node_modules\\${path.sep}(?!vue-bulma-.*)`)] to webpack.base.conf.js

## Run demo

`yarn install`
`npm run dev`

For detailed explanation on how things work, checkout the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).
