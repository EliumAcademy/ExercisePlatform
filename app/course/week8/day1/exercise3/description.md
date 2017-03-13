#### Log new Info

Extend the previous exercise so that you can console.logs the meessage ```"state has changed"``` if and only if the state changes. Make sure that you dispatch functions can handle the case in which the user is trying to delete or update information from the state without appropriate information (Ex: if you are trying to delete a record with an ID that does not exist); in that case the state of the store should not be change and thus we should not log any information to console.


```jsx
// Add one Tool
let todoId = 1
let tool = ["shoes"]

store.dipatch(addTool(todoId, tool))
store.getState()
//{
//  todos: [{id: 0, title: "Sleep"}, {id: 1, title: "Walk"}, {id: 2, title: "Study"}, {id: 3, title: "Eat"}],
//  todoTools: [{id:0, todoId: 1, title: "Shoes"}]
//}

// console.logs
// state has changed


// Remove Tool
let todoId = 100
let tool = ["shoes"]

store.dipatch(addTool(todoId, tool))
store.getState()
//{
//  todos: [{id: 0, title: "Sleep"}, {id: 1, title: "Walk"}, {id: 2, title: "Study"}, {id: 3, title: "Eat"}],
//  todoTools: [{id:0, todoId: 1, title: "Shoes"}]
//}

// Nothing will be logged!
```