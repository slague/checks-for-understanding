## Week Two - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR.

1. What is Webpack and why is it useful?
  Webpack is a build tool that contains a number of packages (babel, jQuery, mocha, chai, etc...). It works like the asset pipeline in a rails project. It compiles all your assets, finds any dependencies, and creates one .js file that is ready for production.

2. When do you want to use event delegation?
  You would use event delegation in order to have a "parent watch its children" for events. Instead of putting the event listener on the child, you'd put it on the parent. This will allow the bubbled up events to get to the parent, which can then delegate what to do.

3. What's one difference between ES5 and ES6?
  ES6:
    got rid of semi-colons,
    uses let and const instead of var,
    Uses arrow notation for fucntions,
    Uses backticks for interpolation,
    Allows you to set default parameters to a function (like ruby)
    Allows you to build classes (very similar to a ruby class) with instance (no longer needs .prototype) and class methods (using static)

4. What's the deal with semi-colons in JavaScript?
  ES6 got rid of them, and they are now optional. If you use them, you should be consistent and always use them.

5. How are you using the MVC design pattern in your Quantified Self project?
  On the backend we have built our server routes (api endpoints) as a RESTful API. The server.js file is our controller (this could be pulled out into a controllers directory where he have two controllers, one for foods and one for meals, but we have not made that refactor yet).  We also use models in both our frontend and backend projects.  In the backend project this is where we interact with the database; in the frontend project this is where we've created functions to make requests to our backend and get/do stuff to different pieces of our model(s) (get all foods, get all meals create a food, delete a food, etc.) Our backend project really doesn't have any 'views', we just send the data as json.  However, our frontend does.  We use the html files to render the information we've pulled from our models.

6. How do you execute raw SQL in node?
  You will need to npm install knex. Knex is a library for working with databases. Then you can use the function knex.raw(_SQL goes here_) in your code to execute raw SQL

7. What's a callback function and what are some reasons when we use/need callback functions?
  A callback is a function that is being passed as a parameter. It will be "called", or invoked later. (You will want to check docs regularly as you are learning what parameters will be passed to your callback function.)

8. What is CORS?
  According to what Nate dropped in our slack channel: "CORS is a dumb thing, and I don't want to waste any time on it.... CORS will allow your two codebases to talk to each other via AJAX." According to google: "Cross-origin resource sharing (CORS) is a mechanism that allows restricted resources (e.g. fonts) on a web page to be requested from another domain outside the domain from which the first resource was served"

9. What are some steps to avoid CORS?
  I'm not sure...for our project we included `var cors = require('cors')` in our backend project and this took care of the issue...

#### Review  

10. Why do people say "HTTP is stateless"?
  Because it does not have memory. There is a new connection between server and browser each time a request is made. A second (or third or 100th) request does not know anything about the requests that came before it.

11. What is a RESTful API?
  REST stands for Representational State Transfer. When you build a RESTful API you use only the "crud" verbs- GET, POST, PUT, DELETE requests. This means you only have methods within your controller that match these requests.  

12. What are some main characteristics of a team following an agile workflow?
  Using some kind of project management tool (waffle, pivotal tracker, trello, etc.) to track features/user stories. Agile workflow means being in regular contact with your client/users, getting feedback and incorporating that feedback into the design and development of the project throughout the build.

13. What are some advantages/disadvantages to using OAuth to authenticate a user?
  Pro: It allows you to 'outsource' the authentication process, so that you don't have to build it yourself. It is likely more secure in the hands of a third party.

  Con: Your users need to all have the thing you are using to OAuth, for example if you set up a log in with github, you need to make sure your users are developers who have github accounts. 
