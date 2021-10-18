# Component Testing Example: Vite + Vue

This is an example **Vite + Vue** project with Cypress component testing.

- `yarn` to install the dependencies
- `npx cypress open-ct` to run interactively
- `npx cypress run-ct` to run all tests headlessly

The following was done to create this example:

1. Initialize a baseline Vue project in the [vite-vue](.) subdirectory
   1. `yarn create vite vite-vue --template vue`
   2. Commit [`a293311`](https://github.com/cypress-io/cypress-component-testing-examples/commit/a2933118198f1db3016238b33612e92feff45735)
2. Install project dependencies
   1. `cd vite-vue`
   2. `yarn`
   3. Commit [`0679173`](https://github.com/cypress-io/cypress-component-testing-examples/commit/0679173ec39f51925b478d0855110213eb30c53d)
3. Update app to move global styles into main.css file
   1. Move global app styles from [src/App.vue](src/App.vue) into [src/main.css](src/main.css)
   2. Update [src/main.js](src/main.js)
   3. Commit [`b197f90`](https://github.com/cypress-io/cypress-component-testing-examples/commit/b197f906ba6c23ab65be740d54dd28cd48af2441)
4. Add Cypress component testing support with sample tests
   1. `yarn add -D cypress @cypress/vue@3 @cypress/vite-dev-server`
   2. Add [cypress.json](cypress.json)
   3. Add [cypress/plugins/index.js](cypress/plugins/index.js)
   4. Add [src/App.spec.ct.js](src/App.spec.ct.js), [src/components/HelloWorld.spec.ct.js](src/components/HelloWorld.spec.ct.js)
   5. `npx cypress open-ct` (Notice that the fonts don't inherit global app styles)
   6. Edit [cypress/support/index.js](cypress/support/index.js) to import global app styles, the Cypress test preview should update automatically
   7. Commit [`79388c8`](https://github.com/cypress-io/cypress-component-testing-examples/commit/79388c85625934811fd12bb712071247c371a31d)

_This example was generated by [vite-vue.sh](https://github.com/cypress-io/cypress-component-testing-examples/blob/scripts/vite-vue.sh) on 2021-08-05. The original README follows._

---

(no original readme)