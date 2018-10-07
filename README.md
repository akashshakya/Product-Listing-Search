# Product-Listing-Search

# Product Search App in Laravel MVC

This Application is an Example implementation of Live search for product listing at various E-commerce website. 
  - Type some keyword in the input box
  - See dropdown matching keywords
  - select anyone to see product
  

### Tech

This App using following:

* [Laravel MVC] - One of the well organised MVC framework to develop web apps.
* [Xampp] - For PHP, MYSQL server
* [JQueryUI] - jQuery UI is a curated set of user interface interactions, effects, widgets, and themes built on top of the jQuery JavaScript Library.
* [Twitter Bootstrap] - great UI boilerplate for modern web apps
* [jQuery/Ajax] - jQuery is a fast, small, and feature-rich JavaScript library.
* [Composer] - Php package Manager

### Installation

Generally to install and run the Laravel Project, we need to install it via composer(see doc here:https://laravel.com/docs/5.7). But, I belive this package won't need to install via composer(as it includes all packages), but having composer installed in your system is good to go.

```sh
In order to run this, Download and Install Xampp Server.

Extract the Zip of Project package in directory: C:\xampp\htdocs

start the server.

###See Live Demo
Open any Browser(recommended Chrome), go to: http://localhost:port/package-name/public

***Note*** port is your working port number for localhost, by default its 80. change accordingly if its not available. 
```

# Tech Inside:

### LiveSearch.php 
LiveSearch.php is an Controller having a Class called LiverSearch. This is giving having two Functions:
-> index : return view live_search
-> action : utility api function that return the json object as per search query Request.

### live_search.blade.php
live_search.blade.php is the page that renders up as root url view('/').
This code includes:
-> Essential HTML code
-> Jquery and JavaScript Code to handle Event.
-> AJAX Function with API Request that returns the JSON obj as response(after matching query).
-> Function to handle Response and bind it as html after parsing.

### api.php
API routing:
Route::get('search', 'LiveSearch@action');

### REST API 
The REST Api end point for product search query is 
http://base_url/api/search

For eg: http://localhost/package-name/api/search?query=Apple

### Database(MySQL)
Database Schema for Product is as follows:
These are following Columns
->ProductName : Name of the Product
->Price : Price of the Product
->Brand : Name of Brand
->Category : Category of the Product
->Discount : % Discount to offer
->Img : Image url of the product
->Tags : Tags for the product to help in search Query.

### Front-End
->HTML, CSS, JavaScript, Bootstrap, Jquery, AJAX.

### Backend
->PHP(Laravel MVC), MYSQL. 

