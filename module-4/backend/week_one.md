Week One, Mod 4 Checks for Understanding

1. What's the most useful thing you learned from completing the intermission week work?
  The different options for debugging and 'prying' into javascript.  I use the console, node, and 'pryjs' regularly to try and figure out what exactly my code is doing.

2. What are some tools to help debug JavaScript code?
  debugger, pryjs, the console, and the node console in your terminal window

3. What are some tools you need in order to unit test your JavaScript?
  You need to make sure you have installed mocha and chai.  You also need to make sure you export the file containing the functions you are testing.  I also find installing pry particularly useful for figuring out how/why tests are not passing.

4. What is the syntax for invoking a function?
  To invoke a function you type the function's name followed by ().  If the function takes arguments, the argument(s) go inside the parenthesis.

5. What's the difference between == and === in JavaScript?
  == is the 'abstract equality comparison operator'.  This will attempt to resolve the datatypes via type conversion being compared before comparing. So, console.log(1 == '1') is true.  The string and integer are the equal because both are one.
  === is the 'strict equality comparison operator'.  This will not try to resolve the datatype and will compare literally.  So, console.log(1 === '1') is false, because one datatype is a string and the other is an integer.

6. What's the difference between asynchronous and synchronous JavaScript?
  Synchronous javascript runs code one thing after the next, or in order.
  Asynchronous is not completed in any specific order; one thing does not necessarily wait for the thing before it to finish before executing.

7. How do we setup a route when creating an API with Node and Express?
  Right now, we include a server.js file in our project.  This is where our app is initialized as a instance of express.  Within this file we write methods for API calls, for example app.get('/') would be a get request to the root.

8. What do we use Knex for?
  We use knex for working with and querying our database within a javascript/node/express project. It allows us to run migrations within the database and write raw sql queries within our code.

9. What's npm and what do we use it for?
  npm = Node package manager.  It is used to install different packages.  So far, it seems very similar to how we would install gems with ruby/rails.

Review

What's the MVC design pattern? Describe each part of MVC?
  MVC stands for Models Views Controllers.  A request is made by a user and the request is sent to the appropriate controller depending on the type of request. Next the controller, connects to the model (which in turn interacts with the database) to acquire the data needed to respond to the original request made.  This data is relayed back to the user via a response that is displayed within the view.

What is AJAX? What are some benefits of using AJAX?
  AJAX is a javascript library. It allows us to make requests and alter a webpage without refreshing it.

What's a background worker? When would we want to use a background worker?
  A background worker is something that goes to work after the normal request/response cycle takes place. It happens later so as to speed up the response time. You'd want to use this whenever you have something that may take longer to process, but you don't want your user to have to sit an wait for the processing to take place. A good example might be sending email.  A response can be sent to the user, and a background worker can then take over to implement the sending of the email after the user has received a response.
