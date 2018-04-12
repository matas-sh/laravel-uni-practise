# laravel-uni-practise
This is a repository to work on the university exercises to learn lavarel

This document will contain some notes on how to use laravel and my understanding. It will be constantly updated to keep the usage up to date.

#structure
Laravel implements MVC structure. Traditionally, the view is presented to user, they may give inputs which will change the data that the model presents. The controller, manages how the model manipulates and displays the data that is used to create a view and displayed to the user.

In laravel, there is an introduction of flow and HTTPrequests. A user may access the website by entering a url, and so the send out a get request to the server for that url, behind the scenes the url is routed to an appropriate controller that sets out a way to deal with a requests. it interacts with the data model and gathers the data needed to display for the user and creates an appropriate view with the data. An example with path coverage would be something like this; A user clicks on a hyperlink account information, the server recieves a GET HTTPrequests with the url localhost/accountinfo/{user_id} and checks the routes in web.php, it finds that in the case where it recieves a GET request to accountinfo/{user} it will route the url to accountController@{specific method} which will combine the model's method and pass the results into the view. The view will be generated with data in mind and returned to the as a response user, the end result displaying data of user's account.

#Controller
has methods that make use of the model and manipulates it's data, and returns a view that will use that data

#Model
model allows the creation of methods that manipulate the data in a datatable

#Migrations
Allows the user to create migrations which in turn create datatables in the database, it allows for version control

#Routes
allows routing of urls so that the controller can deal with requests

#Views
displays the user with visual representation of the responses. displayed by the browser
