# MVC, Routes and params discussion questions

Take 30 minutes to discuss the following questions with your table group.

## MVC

* What is the MVC Pattern?
* What are the distinct responsibilities of the Model, View and Controller?
* What advantages and trade-offs do you see in the MVC pattern?
* Who within the MVC pattern is responsible for:
  - knowing how to create database records?
  - Provide a visual representation of the data that can be sent to the user?
  - Connect the business logic with the visual representation?
* What do you find confusing about the MVC pattern?

## Routing

* Map the CRUD actions to the appropriate Rails route to the appropriate view, if any. What kind of HTTP request is sent for each CRUD action (`GET`, `POST`, etc)
* Let's say you have built a Rails app that is a news platform. You have an Article and an Author model and you have controllers and routes for the CRUD actions of each model. You sit down at your computer and visit `http://youramazingsinatranews.example.com/articles` (not a real link!):
  - What kind of web request is this making? (i.e. is it a `GET`, `POST`, etc request?)
  - What controller action (i.e. which route in which controller) will recieve that web request?
  - What is the response that your Sinatra app will send back to the client, i.e. the browser?
* You have the following form for a new article:

```html
<form action="?" method="?">

  <label>Title</label>
  <input type="text" name="article[title]">

  <label>Author</label>
  <input type="text" name="article[author]">

  <label>Content</label>
  <input type="text" name="article[content]">

  <input type="submit">

</form>
```

  - What action and what method should the form be defined to have?
  - Given the correct action and method, what controller action will this form submit the form data to?
  - Draw out the params that would be created by submitting this form?
  - Bonus: Currently, the form is structured such that the author field is a simple text field, and the user will have to input the name of an existing author. Can you change the form so that it offers a drop down menu of all of the existing authors from the database? What would the resulting params look like? How would you use these params to make a new article and associate it to the selected author?
* Spend a few minutes mapping out a domain model for a parking lot. How would you model the relationship between cars and spaces? How would you keep track of how long a car had been parked in a space? How would you keep track of how much money someone would need to pay for having parked a certain amount of time?
* Discuss the REST-ful routes of a Rails app. What is the rails convention in rendering?

## params

* Where does the params hash come from?
* What utility does the params hash provide?
* Given the two Rails scenarios below how would the params hash look like (What keys will the hash contain)?
  - Scenario 1: Rails route (get '/books/:name') and URL (/books/Just-for-Fun-The-Story-of-an-Accidental-Revolutionary)
  - Scenario 2: Rails route (get '/search/') and URL (/search?query=Just-for-Fun-The-Story-of-an-Accidental-Revolutionary)
