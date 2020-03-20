---
layout: post
title:      "Model View Controller (MVC)"
date:       2020-03-20 06:27:40 +0000
permalink:  model_view_controller_mvc
---


Model View Controller: a structural, design, or architectural pattern that is shared by apps and everyday interactions using three components.

Components of the Model View Controller pattern:

* **Model** (database): The data. 
Interacts with the database when presented with queries that select, insert, update and delete data. 
Communicates with the controller.

* **View** (browser): The interface. 
The view shows the user content or serves as the interface that will display content and interact with the user. 
Communicates with the Controller.

* **Controller** (server): The handler or brains. 
The controller gets instructions from the View to send to the Model, then gets the appropriate information from the Model to be sent to the View. This includes processing get, post, put and delete requests.
Communicates with the Model and the View. 


Model View Controler Flow Example:

End User makes a Request =>

Request accepted by Controller

Controller takes the Request to the Model  =>

Model uses tools and data to respond to the Controllers Request

Model generates a Response to the Controller =>

Controller takes the response back to the User =>

User receives(or views) the response


As I was learning and researching more about the Model View Controller(MVC) pattern, I found many different view points on the concept and still haven't formed my own opinion on the design, but I can currently see the different benefits to the framework:
-Commonly used and understood design pattern (or at least quickly teachable)
-Separates functionality within your application to make it easy to follow or read
-Can be used as a "best practices" model to promote organized programming
-Allows multiple people to work simultaneously on the model, controller, and view

I look forward to how this is going to be used in Rails and was successful at using this pattern in my Sinatra Application.

