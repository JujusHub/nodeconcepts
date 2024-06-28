### Conceptual Exercise

Answer the following questions below:

- What are some ways of managing asynchronous code in JavaScript?
promises callbacks and async awaits
- What is a Promise?
promises are objects that hold the eventual value or failure of a async operation and its resulting value
- What are the differences between an async function and a regular function?
async functions return a promise and sets that as its value while regular functions just run top to bottom and doesnt wait for the async code to stop
- What is the difference between Node.js and Express.js?
node allows you to run javascript serverside while express allows for routes to be handles and is the middleware to your code and allows http request handling
- What is the error-first callback pattern?
node js error handling like if else patterns to detect issues or try catch to run code or then divert it if an error occurs.
- What is middleware?
Middleware can perform a variety of tasks, such as modifying the request and response objects, handling authentication, logging, and error handling.
- What does the `next` function do?
allows middleware functions to go from one to another without breaking the code
- What are some issues with the following code? (consider all aspects: performance, structure, naming, etc)

```js
async function getUsers() {
  const elie = await $.getJSON('https://api.github.com/users/elie');
  const joel = await $.getJSON('https://api.github.com/users/joelburton');
  const matt = await $.getJSON('https://api.github.com/users/mmmaaatttttt');

  return [elie, matt, joel];
}
```
no error handling could cause all code to fail. 3 seperate awaits that require one to finish before going onto the next making it slow
