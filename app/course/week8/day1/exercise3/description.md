#### Log new Info

Extend the previous exercise so that you can console.logs the meessage ```"state has changed"``` if and only if the state changes. Make sure that you dispatch functions can handle the case in which the user is trying to delete or update information from the state without appropriate information (Ex: if you are trying to delete a record with an ID that does not exist); in that case the state of the store should not be change and thus we should not log any information to console.


```jsx
// Add one Todo
let todoId = 1
let tool = ["shoes"]

store.dispatch(addTodo(todoId, tool))
store.getState()
//{
//  todos: [{id: 0, todo: "Sleep"}, {id: 1, todo: "Walk"}, {id: 2, todo: "Study"}, {id: 3, todo: "Eat"}],
//  tools: [{id:0, todoId: 1, tool: "Shoes"}]
//}

// console.logs
// state has changed


// Remove Todo
let todoId = 100
let tool = ["shoes"]

store.dispatch(addTodo(todoId, tool))
store.getState()
//{
//  todos: [{id: 0, todo: "Sleep"}, {id: 1, todo: "Walk"}, {id: 2, todo: "Study"}, {id: 3, todo: "Eat"}],
//  tools: [{id:0, todoId: 1, tool: "Shoes"}]
//}

// Nothing will be logged!
```

**Attention**: In orther for your to pass all the test you need to only have one single console.log withing your solution.