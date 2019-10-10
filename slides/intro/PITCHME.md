# Giovanni Giordano

- Frontend Developer @ brumbrum

+++

## What we are going to cover 1/2

As long as ⏳ permits

- example TodoMVC
  * web app, data store, REST calls
- basic page load test
- selector playground
- resetting state
- XHR spying and stubbing, fixtures

+++

## What we are going to cover 2/2

As long as ⏳ permits

- CI and Cypress dashboard
- test reporters
- configuration and environment variables
- retry-ability
- debugging
- visual testing

+++

## Requirements

You will need:

- `git` to clone this repo
- Node v6+ to install dependencies

```text
git clone <repo url>
cd testing-workshop-cypress
npm install
```

+++

## Repo organization

- `/todomvc` is a web application we are going to test
- all tests are in `cypress/integration` folder
  - there are subfolders for exercises
    - `01-basic`
    - `02-adding-items`
    - `03-selector-playground`
    - `04-reset-state`
    - etc
- keep application `todomvc` running!

Note:
We are going to keep the app running, while switching from spec to spec for each part.

+++

## `todomvc`

Let us look at the application.

- `cd todomvc`
- `npx http-server -p 3000`
- `npx json-server data.json -p 9000 --middlewares ./node_modules/json-server-reset`
- `open localhost:3000`

**important** keep application running through the entire workshop!

+++

It is a regular TodoMVC application, with a special sense of humor by the author.

![TodoMVC](/slides/intro/img/todomvc.png)

Look at XHR when using the app

![Network](/slides/intro/img/network.png)

## Questions

- what happens when you add a new Todo item?
- how does it get to the server?
- where does the server save it?
- what happens on start up?

Note:
 You should find `todomvc/data.json` file with saved items.

