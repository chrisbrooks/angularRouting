angularRouting
=========

<h2>About</h2>

This is simply a simple angular JS routing example demonstrating how you can using angular to route to different pages on a site. For simplicity purposes botstrap was used for the styling.


```javascript
	// create the module and name it scotchApp
	var routingExample = angular.module('routingExample', ['ngRoute']);

	// configure our routes
	routingExample.config(function($routeProvider) {
		$routeProvider

			// route for the home page
			.when('/', {
				templateUrl : 'pages/home.html',
				controller  : 'mainController'
			})

			// route for the about page
			.when('/about', {
				templateUrl : 'pages/about.html',
				controller  : 'aboutController'
			})

			// route for the contact page
			.when('/contact', {
				templateUrl : 'pages/contact.html',
				controller  : 'contactController'
			});
	});

	// create the controller and inject Angular's $scope
	routingExample.controller('mainController', function($scope) {
		// create a message to display in our view
		$scope.message = 'This is the home page message';
	});

	routingExample.controller('aboutController', function($scope) {
		$scope.message = 'This is the about page message';
	});

	routingExample.controller('contactController', function($scope) {
		$scope.message = 'This is the contact page message';
	});
```
