# ReduxAdvancedNotes

## Redux Thunk

[Redux Thunk](https://github.com/gaearon/redux-thunk) is a library designed to handle async action creators.

```js
import axios from 'axios'

export function fetchUsers() {
  const request = axios.get('gabagool.com/accounts')
  
  // Vanilla redux expects us to return an action, redux thunk allows us to return a plain javascript function
  
  return (dispatch) => { // actions passed into dispatch are sent off to all our other reducers
    request.then(({data}) => {
      dispatch({ type: 'TYPE', payload:data })
    }
  }
}
```

## Redux and Firebase

When using redux with firebase, you want to apply
