<h1> React + Redux </h1>

[Redux For Beginners | React Redux Tutorial](https://www.youtube.com/watch?v=CVpUuw9XSjY&t=1780s)

[Redux](https://redux.js.org/) - A Predictable State Container for JS Apps<br>
[React Redux](https://react-redux.js.org/) - Official React bindings for Redux

</div>

**STORE** - Globalized State<br>
**ACTION** - Type action to be perform<br>
**REDUCER** - Check action type and transform state<br>
**DISPATCH** - Execute action to reducer<br>

```js
import { createStore } from "redux";

//ACTION
const increment = () => {
  return {
    type: "INCREMENT",
  };
};

const decrement = () => {
  return {
    type: "DECEREMENT",
  };
};

// REDUCER
const counter = (state = 0, action) => {
  switch (action.type) {
    case "INCREMENT":
      return state + 1;
    case "DECREMENT":
      return state - 1;
  }
};

// STORE
let store = createStore(counter);

//DISPATCH
store.dispatch(increment());
store.dispatch(increment());
store.dispatch(increment());

// SUBSCRIBER
store.subscribe(() => {
  console.log(store.getState());
});
```
