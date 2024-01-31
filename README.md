# 2024front

https://velog.io/@gene028/JavaScript-%EB%B0%94%EB%8B%90%EB%9D%BC-JS%EB%A1%9C-TodoList-%EB%A7%8C%EB%93%A4%EA%B8%B0

1. html로 뼈대 만들기.


// https://kr.vuejs.org/v2/examples/todomvc.html
var STORAGE_KEY = 'todos-vuekr-demo'
var todoStorage = {
  fetch: function() {
    var todos = JSON.parse(
      localStorage.getItem(STORAGE_KEY) || '[]'
    )
    todos.forEach(function(todo, index) {
      todo.id = index
    })
    todoStorage.uid = todos.length
    return todos
  },
  save: function(todos) {
    localStorage.setItem(STORAGE_KEY, JSON.stringify(todos))
  }
}
