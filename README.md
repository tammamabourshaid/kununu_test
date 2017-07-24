# kununu Frontend Test

> ### ⚠️ Read it first!
> I know... you probably love to code (we also love it!). But please, read this file until the end and make sure to understand the requirements before you start coding! If you have any question, just let us know!

## Backstory

Over the years we accumulated a huge list of cities. Now we have a new set of official geographical data. Unfortunately, our old list has a lot of misspelt cities, so we can't simply let a `cron` job match our old data with the new data.

To solve this, we will ask one of our working students to check each of the old cities that we weren't able to match automatically. To make his task a little bit more bearable, you will write an application to help him find historical matches for each city in the new set.

## Goal

Build a city-matcher tool using two API endpoints.

 - The interface should have two columns:
   * The left side with cities from the new geographical data.
   * The right side with an autocomplete dropdown search for old historical data.
- In the autocomplete search, users can try out different spellings and select a city matching the left column.
- After an item is selected, it should `console.log()` the full data of both the city on the left and the selection on the right, so our working student can write down all the information.
- The final app should look somewhat similar to the mockup below, but as long as you meet the criteria described above, you can build it in whichever way you find appropriate.
    <img src="mockup.png?raw=true" width="480">

## Basic Tooling & API

To get you started in the right direction, we give you a couple of npm scripts. But feel free to improve and extend it as you go through the assignment.

```sh
> npm install

> npm run api       # run API on 0.0.0.0:8000
> npm run serve     # serve app and watch files using webpack-dev-server
> npm run build     # bundle app to the `dist` folder
```

The API serves the two endpoints you'll need:

```sh
/v1/cities                   # get the list of new geographical cities
/v1/autocomplete?q=<query>   # get the list of old historical city data matching a query
```

## Technology

This is your chance to show off. Use [React](https://reactjs.org/) to build a clearly-written application.

### Must haves

- Use some sort of client-side state management such as [Redux](https://redux.js.org/) or [React Context](https://reactjs.org/docs/context.html).
- Write your own CSS. No Bootstrap, please.
- Test your React components with something like [Jest](https://jestjs.io/) and add a `test` task to the npm scripts.

### Nice to haves

- We're showing too many cities in a single page. Implement pagination using client-side routing, so we only see 20 cities at a time.
- Let's say we need our application to support IE11, but [promises](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise) and [async/await](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/async_function) don't work there. To a reasonable extent, ensure we can support these modern constructs and APIs in not-so-modern browsers.
- We like tidy code! Configure linting for your JavaScript and CSS files.
- Anything else you think we'd like to see :)

## Tips

- Focus on completing the [Must haves](#must-haves) first.
- Don't use a `create-react-app` boilerplate. We want to see what your ideal project setup would look like.
- Using other libraries from the React ecosystem is completely fine, as long as you can explain what they do.
- In general, we'd rather see something simple you understand than something fancy you can't explain.
