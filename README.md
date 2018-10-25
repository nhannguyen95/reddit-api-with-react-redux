Reddit API App from Redux documentation. [1]

## Redux-Thunk

Using Redux, whenever we dispatch actions with Action Creators, Action Creators return plain action objects, then reducers take the actions to define what will happen to the state (in the store).

Because reducers are pure functions, and Action Creators only return plain objects, we cannot do something fancy like API calls, call non-pure functions or trigger other actions.

In order to do them, one approach is to make Action Creators return functions. So now when Redux receives an action from Action Creators, it sends to reducers; when Redux receives a function, it executes that function.

As you might guess, we can now do side effects in that function.

Redux-Thunk does exactly that, it's a middleware for Redux that allows Action Creators return a function (this function is called a thunk [3]).

## References

[[1] Reddit API App](https://redux.js.org/advanced/exampleredditapi)

[[2] What the heck is a 'thunk'?](https://daveceddia.com/what-is-a-thunk/)

[[3] Thunk](https://en.wikipedia.org/wiki/Thunk)
