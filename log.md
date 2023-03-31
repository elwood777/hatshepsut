## Hatshepsut (log)
[hatshepsut](https://github.com/elwood777/ramessesII)
**Redux Simple Counter App**
A simple applicaion to showcase a solid understanding Redux.   

**Objective**   
Create a simple counter app that allows users to increment and decrement a counter.

## Getting Started  
Create a new React component called "hatshepsut" (To Do List) 
```
npx create-react-app hatshepsut
```  
  
## Create Store
In this code, we're using the "createStore" function from Redux to create a new store with our "counterReducer" function as the root reducer. The initial state of the store is an object with a "count" property set to 0.
```js
import { createStore } from 'redux';

const initialState = {
  count: 0,
};

function counterReducer(state = initialState, action) {
  switch (action.type) {
    case 'INCREMENT':
      return {
        ...state,
        count: state.count + 1,
      };
    case 'DECREMENT':
      return {
        ...state,
        count: state.count - 1,
      };
    default:
      return state;
  }
}

const store = createStore(counterReducer);

```  


## Redux Actions
Create two Redux actions to handle incrementing and decrementing the counter.  
```js  
function increment() {
  return {
    type: 'INCREMENT',
  };
}

function decrement() {
  return {
    type: 'DECREMENT',
  };
}
```  





## Other Commands
Starts the development server.
```  
$ npm start
```  

Bundles the app into static files for production.
```  
$ npm run build
``` 

Starts the test runner.
```  
$ npm test
``` 

Removes this tool and copies build dependencies, configuration files and scripts into the app directory.
```  
$ npm run eject
``` 