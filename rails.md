# ASSESSMENT 5: INTRO TO RAILS
## Interview Practice Questions

Answer the following questions. First, without external resources. Challenge yourself to answer from memory. Then, research the question to expand on your answer. Even if you feel you have answered the question completely on your own there is always something more to learn.

1. MVC (Model View Controller) is a pattern for the architecture of a software program. Give a brief description of each component and describe how Ruby on Rails handles MVC.

  Your answer: interact with the data base 

  Researched answer:
Model–view–controller (usually known as MVC) is a software design pattern[1] commonly used for developing user interfaces which divides the related program logic into three interconnected elements.
Model is the central component of the pattern. It is the application's dynamic data structure, independent of the user interface.[5] It directly manages the data, logic and rules of the application.
View is a representation of information such as a chart, diagram or table. Multiple views of the same information are possible, such as a bar chart for management and a tabular view for accountants.
Controller accepts input and converts it to commands for the model or view

2. Using the information given, fill in the blanks to complete the steps for creating a new view in a Rails application.

  Step 1: Create the Route in the file config/routes.rb
  ```
  get '/about' => 'statics#about'
 
  ```

  Step 2: Create the Controller in the file controller/app_controller.rb
  ```
 class AppController < ApplicationController
  def index
    render json: app
  end
end

  Step 3: Create the View in the file view/index.html.erb code:

  ```
  <div>This is the About page!</div>
  ```


3a. Consider the Rails routes below. Describe the responsibility of  each route.


/users/ method="GET" # :controller => 'users', :action => 'index' Used to show all stored information

/users/1 method="GET" # :controller => 'users', :action => 'show' Used to show the information for a specified object

/users/new method="GET" # :controller => 'users', :action => 'new' Used to accept informtation in a form, which will then be used to create a new object

/users/ method="POST" # :controller => 'users', :action => 'create' Used to complete the creation of the new object using the information given by the user

/users/1/edit method="GET" # :controller => 'users', :action => 'edit' Used to accept informtation in a form, which will then be used to update an existing object

/users/1 method="PUT" # :controller => 'users', :action => 'update' Used to change the information of an existing object using the information given by the user

/users/1 method="DELETE" # :controller => 'users', :action => 'destroy' Used to remove information of an existing object



3b. Which of the above routes must always be passed params and why?
Only show, edit, update, destroy pass params. for the example of wildlife tracker we were passing the :id param and we needed the id to be able to show, edit, update, or delete a specific animal.
 





4. What is the public folder used for in Rails?

  Your answer: 

  Researched answer:  Has files that come with making an app



5. Write a rails route for a controller called "main" and a page called "game" that takes in a parameter called "guess"

  GET '/game/:guess' => 'main#game'


6. In an html form, what does the "action" attribute tell you about the form? How do you designate the HTTP verb for the form?

  Your answer:

  Researched answer: The HTML | action Attribute is used to specify where the formdata is to be sent to the server after submission of the form. It can be used in the

element. The method attribute specifies the HTTP method (GET or POST) to be used when submitting the form data



7. Name two rails generator commands and what files they create:

  Your answer:

  Researched answer: $ rails generate controller Usage: rails generate controller NAME [action action] [options] $ rails generate controller Greetings hello It made sure a bunch of directories were in our application, and created a controller file, a view file, a functional test file, a helper for the view, a JavaScript file, and a stylesheet file.


8. Rails has a great community and lots of free tutorials to help you learn. Choose one of these resources and look through the material for 10-15 min. List three new things you learned about Rails:
- [Ruby on Rails Tutorial](https://www.tutorialspoint.com/ruby-on-rails/index.htm)
- [Rails for Zombies](http://railsforzombies.org)
- [Rails Guides](http://guides.rubyonrails.org/getting_started.html)

1. You could develop a web application at least ten times faster with Rails than you could with a typical Java framework.

2. Ruby is interpreted like Perl, Python, Tcl/TK.

3. Ruby is the successful combination of − Python's ease of use and learning, andPerl's pragmatism.


9. STRETCH: What are cookies? What is the difference between a session and a cookie?

  Your answer:

  Researched answer: Session A session creates a file in a temporary directory on the server where registered session variables and their values are stored. This data will be available to all pages on the site during that visit. A session ends when the user closes the browser or after leaving the site, the server will terminate the session after a predetermined period of time, commonly 30 minutes duration.

Cookies Cookies are text files stored on the client computer and they are kept of use tracking purpose. Server script sends a set of cookies to the browser. For example name, age, or identification number etc. The browser stores this information on a local machine for future use. When next time browser sends any request to web server then it sends those cookies information to the server and server uses that information to identify the user.
