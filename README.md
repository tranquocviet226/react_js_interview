## :question: React JS Interview Questions & Answers

|No  |Questions  |
|--|--|
|1 |[What is React?](#what-is-react)   |
|2 |[What are the features of React?](#what-are-the-features-of-react)|
|3 |[Can web browsers read JSX directly?](#can-web-browsers-read-jsx-directly)|
|4 |[What is difference between Real DOM and Virtual DOM?](#what-is-difference-between-real-dom-and-virtual-dom)|
|5 |[What is the difference between the ES6 and ES5 standards?](#what-is-the-difference-between-the-es6-and-es5-standards)|
|6 |[Explain how lists work in React?](#explain-how-lists-work-in-react)| 
|7 |[Why is there a need for using keys in Lists?](#why-is-there-a-need-for-using-keys-in-lists)|
|8|[What is difference between Regular function and Arrow function?](#what-is-difference-between-regular-function-and-arrow-function)|
|9 |[What is difference between Class component and Function component?](#what-is-difference-between-class-component-and-function-component)|
|10|[What is a state in React?](#what-is-a-state-in-react)|
|11|[What are props in React?](#what-are-props-in-react)|
|12|[What are the differences between state and props?](#what-are-the-differences-between-state-and-props)|
|13|[What is Redux?](#what-is-redux)
|14|[What are the components of Redux?](#what-are-the-components-of-redux)
|15|[Middlewares of Redux?](#middlewares-of-redux)

### Content questions

1. ### What is React?
React is a JavaScript library for building user interfaces

2. ### What are the features of React?

|  Features | Description |
|--|--|
|**JSX:** JSX is a syntax extension to JavaScript. It is a shorthand for JavaScript XML. It is used with React to describe what the user interface should look like. By using JSX, we can write HTML structures in the same file that contains JavaScript code. | ![JSX react](https://www.simplilearn.com/ice9/free_resources_article_thumb/jsx-react.JPG) |
|**Virtual DOM:** It uses the virtual DOM instead of the real DOM. When the state of an object changes, virtual DOM changes only that object in the real DOM, rather than updating all the objects.| ![Virtual DOM](https://www.simplilearn.com/ice9/free_resources_article_thumb/virtual-dom.JPG)|
|**Components:** Components are the building blocks of any React application, and a single app usually consists of multiple components. It splits the user interface into independent, reusable parts that can be processed separately.| ![Components](https://www.simplilearn.com/ice9/free_resources_article_thumb/components.JPG)|
|**One-way data-binding:** React’s one-way data binding keeps everything modular and fast. A unidirectional data flow means that when designing a React app, you often nest child components within parent components. |![Data binding](https://www.simplilearn.com/ice9/free_resources_article_thumb/data-binding.JPG)|

3. ### Can web browsers read JSX directly?

-  Web browsers cannot read JSX directly. This is because they are built to only read regular JS objects and JSX is not a regular JavaScript object
-  For a web browser to read a JSX file, the file needs to be transformed into a regular JavaScript object. For this, we use Babel
![babel](https://www.simplilearn.com/ice9/free_resources_article_thumb/babel.JPG)

4. ### What is difference between Real DOM and Virtual DOM?
|Real DOM|Virtual DOM|
|--|--
|It updates slow|It updates faster|
|Can directly update HTML|Can’t directly update HTML|
|Creates a new DOM if element updates|Updates the JSX if element updates|
|DOM manipulation is very expensive|DOM manipulation is very easy|
|Too much of memory wastage|No memory wastage |

5. ### What is the difference between the ES6 and ES5 standards?

-  **Components and Function**
```javascript
// ES5
var MyComponent = React.createClass({
	render: function(){
		return <h1>Hello world</h1>
	}
})

// ES6
class MyComponent extends React.Component{
	render(){
		return <h1>Hello world </h1>
	}
}

const MyComponent = () => {
	return <h1>Hello world </h1>
}
```
- **Require and Import**
```javascript
// ES5
var React = require('react')

// ES6
import React from 'react'
```

6. ### Explain how lists work in React?
-   We create lists in React as we do in regular JavaScript. Lists display data in an ordered format
-   The traversal of lists is done using the map() function
```javascript
const ListOfName = () => {
	const data = ['Hung', 'Manh', 'Hai'] 
	const renderList = data.map(name => <li key={name}>{name}</li>)
	
	return <ul>{renderList}</ul>
}
```

7. ### Why is there a need for using keys in Lists?
-   A key is a unique identifier and it is used to identify which items have changed, been updated or deleted from the lists.
-   It also helps to determine which components need to be re-rendered instead of re-rendering all the components every time. Therefore, it increases performance, as only the updated components are re-rendered.

8. ### What is difference between Regular function and Arrow function?
| Regular function | Arrow function  |
|--|--|
|**Syntax:** `const add = function(x, y) {return x + y}` | `const add = (x, y) => x + y` |
|**This:** Regular function uses `this` keyword | Arrow functions do not have their own `this`|
|**Using new keyword:** Regular functions created using function declarations or expressions are constructible and callable. Since regular functions are constructible, they can be called using the `new` keyword.| The arrow functions are only callable and not constructible, i.e arrow functions can never be used as constructor functions. Hence, they can never be invoked with the `new` keyword.|

9. ### What is difference between Class component and Function component?
|Class component  |Function component  |
|--|--|
| - A class component requires you to extend from React. Component and create a render function which returns a React element. |- A functional component is just a plain JavaScript function that accepts props as an argument and returns a React element. 
|- It must have the render() method returning HTML |- There is no render method used in functional components.
|- React lifecycle methods can be used inside class components (for example, componentDidMount). |- React lifecycle methods (for example, componentDidMount) cannot be used in functional components.
|- It requires different syntax inside a class component to implement hooks. | - Hooks can be easily used in functional components. 
|- Constructor are used as it needs to store state. | - Constructors are not used .|

10.  ### What is a state in React?
 - The state object is where you store property values that belongs to the component. When the state object changes, the component re-renders.
 -  The change in state can happen as a response to user action or system-generated events. It determines the behavior of the component and how it will render.

11. ### Why should we not update the state directly?
It schedules an update to a component's state object. When state changes, the component responds by re-rendering

12. ### What are props in React?
-   **Props** are short for Properties. It is a React built-in object that stores the value of attributes of a tag and works similarly to HTML attributes.
-   Props provide a way to pass data from one component to another component. Props are passed to the component in the same way as arguments are passed in a function.

13. ### What are the differences between state and props?
|  | State | Props |
|--|--|--|
| Use | Holds information about the components | Allows to pass data from one component to other components as an argument |
| Mutability| Is mutable | Are immutable|
|Read-Only| Can be changed|Are read-only |
|Child components|Child components cannot access|Child component can access|

14. ### What is Redux?
Redux  is an open-source, JavaScript library used to manage the application state. React uses Redux to build the user interface. It is a predictable state container for JavaScript applications and is used for the entire application’s state management.

15. ### What are the components of Redux?
-   **Store:**  Holds the state of the application.
-   **Action:**  The source information for the store.
-   **Reducer:**  Specifies how the application's state changes in response to actions sent to the store.

![action](https://www.simplilearn.com/ice9/free_resources_article_thumb/action.JPG)

15. ### How is the data flow of redux?
- An action is dispatched when a user interacts with the application. 
- The root reducer function is called with the current state and the dispatched action. The root reducer may divide the task among smaller reducer functions, which ultimately returns a new state. 
- The store notifies the view by executing their callback functions. 
- The view can retrieve updated state and re-render again.

16. ### Middlewares of Redux?
- Redux-thunk
- Redux-saga
- Redux-observable
- ...

17. ### What is React Router?
React Router is a routing library built on top of React, which is used to create routes in a React application.

18. ### Why do we need to React Router?
-   It maintains consistent structure and behavior and is used to develop single-page web applications.
-   Enables multiple views in a single application by defining multiple routes in the React application.

19. ### How do you style React components?
- Inline Styling
- JavaScript Object
- CSS Stylesheet
