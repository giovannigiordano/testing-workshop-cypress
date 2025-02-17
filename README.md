# testing-workshop-cypress [![CircleCI][ci-badge]][ci-url] [![Build status](https://ci.appveyor.com/api/projects/status/lflec2iwjc8gbhki/branch/master?svg=true)](https://ci.appveyor.com/project/giovannigiordano/testing-workshop-cypress/branch/master) [![renovate-app badge][renovate-badge]][renovate-app]

> A full day testing workshop complete with application, exercise tests and speaker slides for [Cypress.io](https://www.cypress.io/)

## Requirements ⚙️

- Any computer: Mac, Windows, Linux
- [Node 6+](https://nodejs.org/)
- [git](https://git-scm.com)

In order to get the code and install dependencies

```bash
git clone git@github.com:giovannigiordano/testing-workshop-cypress.git
cd testing-workshop-cypress
npm install
```

If necessary, install dependencies inside TodoMVC folder

```bash
cd todomvc
npm install
```

### Quick check ✅

You can test the installation by starting TodoMVC in the first terminal window

```shell
cd todomvc
npm start
```

and you should see in the terminal

```text
> json-server --static . data.json --middlewares ./node_modules/json-server-reset


  \{^_^}/ hi!

  Loading data.json
  Loading ./node_modules/json-server-reset
  Done

  Resources
  http://localhost:3000/todos

  Home
  http://localhost:3000
```

Note for Windows users: if `npm start` throws an error, it is probably due to `cd todomvc; ...` first command in the `npm start `script. In this case change the working folder to "todomvc" and run `npm start` from there.

From the second terminal window you should be able to open Cypress with

```bash
$ npm run cy:open

> testing-workshop-cypress@1.0.0 cy:open /git/testing-workshop-cypress
> cypress open
```

### Tip

You can use the installed [start-server-and-test](https://github.com/bahmutov/start-server-and-test) utility to start the app, open Cypress and then shutdown the app when you exit Cypress.

```bash
$ npm dev
```

## Slides 🖥

See the presentation at [https://gitpitch.com/giovannigiordano/testing-workshop-cypress][presentation] with the starting file in [PITCHME.md](PITCHME.md) presented using [GitPitch](https://gitpitch.com/). The pitch file includes files from the [slides](slides) folder. Students should open the [presentation slides][presentation] and follow along. You can also show each section separately by clicking on the "slides" link in the table below. The full presentation includes all these presentations.

[presentation]: https://gitpitch.com/giovannigiordano/testing-workshop-cypress

## Content 🗂

### Beginner

| | topic                                  | folder                                                                                   | contents                                                       | slides |
| --- | -------------------------------------- | ---------------------------------------------------------------------------------------- | ------------------------------------------------------------- | ------ |
| [🔗](#intro) | Introduction, TodoMVC application      | [todomvc](todomvc)                                                                       | [intro.md](slides/intro/PITCHME.md)                                   | [link](https://gitpitch.com/giovannigiordano/testing-workshop-cypress?p=slides/intro)
| [🔗](#start) | Loading page                           | [00-start](00-start)                                                                     | [00-start](slides/00-start/PITCHME.md)                             | [link](https://gitpitch.com/giovannigiordano/testing-workshop-cypress?p=slides/00-start)
| [🔗](#basic) | `cypress open` vs `cypress run`        | [01-basic](cypress/integration/01-basic)                             | [01-basic](slides/01-basic/PITCHME.md)                             | [link](https://gitpitch.com/giovannigiordano/testing-workshop-cypress?p=slides/01-basic)
| [🔗](#adding-items) | Adding items test, `cypress.json` file | [02-adding-items](cypress/integration/02-adding-items)               | [02-adding-items](slides/02-adding-items/PITCHME.md)               | [link](https://gitpitch.com/giovannigiordano/testing-workshop-cypress?p=slides/02-adding-items)
| [🔗](#selector-playground) | Selector Playground                    | [03-selector-playground](cypress/integration/03-selector-playground) | [03-selector-playground](slides/03-selector-playground/PITCHME.md) | [link](https://gitpitch.com/giovannigiordano/testing-workshop-cypress?p=slides/03-selector-playground)
| [🔗](#reset-state) | Reset database using `cy.request`      | [04-reset-state](cypress/integration/04-reset-state)                 | [04-reset-state](slides/04-reset-state/PITCHME.md)                 | [link](https://gitpitch.com/giovannigiordano/testing-workshop-cypress?p=slides/04-reset-state)
| [🔗](#xhr) | Spy and stub XHR requests, fixtures    | [05-xhr](cypress/integration/05-xhr)                                 | [05-xhr](slides/05-xhr/PITCHME.md)                                 | [link](https://gitpitch.com/giovannigiordano/testing-workshop-cypress?p=slides/05-xhr)
| [🔗](#app-data-store) | Access application code and data       | [06-app-data-store](cypress/integration/06-app-data-store)           | [06-app-data-store](slides/06-app-data-store/PITCHME.md)           | [link](https://gitpitch.com/giovannigiordano/testing-workshop-cypress?p=slides/06-app-data-store)

### Intermediate
| | topic                                  | folder                                                                                   | contents                                                       | slides |
| --- | -------------------------------------- | ---------------------------------------------------------------------------------------- | ------------------------------------------------------------- | ------ |
| [🔗](#ci) | Setting up E2E tests on CI             | [07-ci](cypress/integration/07-ci)                                   | [07-ci](slides/07-ci/PITCHME.md)                                   | [link](https://gitpitch.com/giovannigiordano/testing-workshop-cypress?p=slides/07-ci)
| [🔗](#dashboard) | Setting up Cypress Dashboard           | [07-ci](cypress/integration/07-ci)                                   | [08-dashboard](slides/08-dashboard/PITCHME.md)                     | [link](https://gitpitch.com/giovannigiordano/testing-workshop-cypress?p=slides/08-dashboard)
| [🔗](#reporters) | Test reporters             | - | [09-reporters](slides/09-reporters/PITCHME.md)                     | [link](https://gitpitch.com/giovannigiordano/testing-workshop-cypress?p=slides/09-reporters)
| [🔗](#configuration) | Configuration | - | [10-configuration](slides/10-configuration/PITCHME.md) | [link](https://gitpitch.com/giovannigiordano/testing-workshop-cypress?p=slides/10-configuration)
| [🔗](#retry-ability) | Retry-ability | [11-retry-ability](cypress/integration/11-retry-ability) | [11-retry-ability](slides/11-retry-ability/PITCHME.md) | [link](https://gitpitch.com/giovannigiordano/testing-workshop-cypress?p=slides/11-retry-ability)
| [🔗](#custom-commands) | Custom commands | [12-custom-commands](cypress/integration/12-custom-commands) | [12-custom-commands](slides/12-custom-commands/PITCHME.md)| [link](https://gitpitch.com/giovannigiordano/testing-workshop-cypress?p=slides/12-custom-commands)

### Advanced
| | topic                                  | folder                                                                                   | contents                                                       | slides |
| --- | -------------------------------------- | ---------------------------------------------------------------------------------------- | ------------------------------------------------------------- | ------ |
| [🔗](#app-actions) | Page Objects vs App Actions | [13-app-actions](cypress/integration/13-app-actions) | [13-app-actions](slides/13-app-actions/PITCHME.md) | [link](https://gitpitch.com/giovannigiordano/testing-workshop-cypress?p=slides/13-app-actions)
| [🔗](#fixtures) | Fixtures | [14-fixtures](cypress/integration/14-fixtures) | [14-fixtures](slides/14-fixtures/PITCHME.md) | [link](https://gitpitch.com/giovannigiordano/testing-workshop-cypress?p=slides/14-fixtures)
| [🔗](#debugging) | Debugging | [02-adding-items/demo.js](cypress/integration/02-adding-items/demo.js) | [15-debugging](slides/15-debugging/PITCHME.md) | [link](https://gitpitch.com/giovannigiordano/testing-workshop-cypress?p=slides/15-debugging)
| [🔗](#preprocessors) | Preprocessors | [16-preprocessors](cypress/integration/16-preprocessors) | [16-preprocessors](slides/16-preprocessors/PITCHME.md) | [link](https://gitpitch.com/giovannigiordano/testing-workshop-cypress?p=slides/16-preprocessors)
| [🔗](#component-testing) | Component testing | [17-component-testing](cypress/integration/17-component-testing) | [17-component-testing](slides/17-component-testing/PITCHME.md) | [link](https://gitpitch.com/giovannigiordano/testing-workshop-cypress?p=slides/17-component-testing)
| [🔗](#backend) | Backend code | [18-backend](cypress/integration/18-backend) | [18-backend](slides/18-backend/PITCHME.md) | [link](https://gitpitch.com/giovannigiordano/testing-workshop-cypress?p=slides/18-backend)
| [🔗](#code-coverage) | Code coverage | [19-code-coverage](cypress/integration/19-code-coverage) | [19-code-coverage](slides/19-code-coverage/PITCHME.md) | [link](https://gitpitch.com/giovannigiordano/testing-workshop-cypress?p=slides/19-code-coverage)
| | The end                                | -                                                                                        | [end](slides/end/PITCHME.md)                                       | [link](https://gitpitch.com/giovannigiordano/testing-workshop-cypress?p=slides/end)

## Additional information 🗃

- https://www.cypress.io/
- https://docs.cypress.io/
- https://docs.cypress.io/api/api/table-of-contents.html

[ci-badge]: https://circleci.com/gh/giovannigiordano/testing-workshop-cypress.svg?style=svg
[ci-url]: https://circleci.com/gh/giovannigiordano/testing-workshop-cypress
[renovate-badge]: https://img.shields.io/badge/renovate-app-blue.svg
[renovate-app]: https://renovateapp.com/
