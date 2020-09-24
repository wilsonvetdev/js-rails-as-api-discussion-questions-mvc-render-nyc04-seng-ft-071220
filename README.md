# Discussion Questions: MVC and Rails Render

## Objectives

* Recall the MVC pattern from Rails
* Identify what `render` does in a Rails controller
* Implement controller actions that render different types

## MVC Review Questions

Write your best answers to the following questions, then discuss with your group.

1. What is the _Model_ responsible for in MVC?  What about the _Controller_? The _View_?

The model is a container that holds the objects, methods, and properties.
The controller delegates to the view of what to render.
The view renders what the controller passes in.

2. Now that we are using JavaScript to build Single Page Applications, what changes do we need to make to the division of responsibilities in MVC? What is JavaScript responsible for? What is Rails responsible for?

Views is not needed anymore.
Rails is responsible for backend and serves data in JSON format.
Javascript is responsible for the interaction between user and browser.
Javascript also communicates with the server and it also enables fetching without trigger a full-page refresh.

3. What kinds of formats can Rails render? List as many as you can. When you think you've got a full list, check out [Rails Guide on Rendering](https://guides.rubyonrails.org/layouts_and_rendering.html#using-render) to see if you missed any.

Text, JSON. 
HTML, vanilla JS, XML, raw file.

4. Check out the other ways of sending data in Rails in the [ActionController::DataStreaming documentation](https://api.rubyonrails.org/v5.2.3/classes/ActionController/DataStreaming.html). Draw out how you would build a file download button. 

create an element for a button
fetch request to download 
draw a route in config/routes
route to controller#action
controller serves up the file for user to download on client-side

## Exercise

Check out the rails app in the `rendering` folder. `bundle install` and `rails s` to get things running.

Open `config/routes.rb` and `app/controllers/responses_controller.rb`. Add the `render`, `send_data`, and `send_file` lines to the controller so that all the routes work. Check them all by visiting the urls in the browser.

