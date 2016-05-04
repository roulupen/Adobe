 1) Routing
 2) Data Binding
----------------------

Angular JS framework Modules

			Module
			  |
			Config
			  |
			Router
			 |
	|----------------------------|---------------------------|
	View <---Scope--->			Controller					Service
	Directive												Factory
															Provider

 -------------------------------------------------------------------

 CSS3
 	provides @media 


 	angular.bootstrap(document.body,["CustomerModule"]);


 	$('.ng-scope').css({'border':'1px solid red'}).css({'margin':'1px'});
 -------------------------------------------------------------------------


 Directives

 Predefiend Angular Directives:
 1) ng-app
 2) ng-controller
 3) ng-repeat
 4) ng-model
 5) ng-click
 6) ng-change
 7) ng-if
 8) ng-show
 9) ng-hide

 	ng-app or ng:app or ng_app or data-ng-app
 	will evaluate to ngApp

 Custom Directives:

 	cardView

 	<card-view></card-view>

 	<div card-view></div>

 	<td>
 	<!-- directive:card-view -->
 	</td>


 	Without promise

 	$scope.customers = CustomerService.getCustomers();

 	use $scope.customers;

 	With promise

 	CustomerService.getCustomers().then(function(data){
 		$scope.customers =  data.data;
 	});
 ---------------------------------------------------------

 Day 3
 -----

 controller

 directive

 service

 ---------------------------------

 Directive

    <div ng-controller="SampleController">

 	<first>
 		<second>
 			<third>
 			</third>
 		</second>
 	<first>

 	</div>
 -------

 <div ng-controller="SampleController">

 	<first>
 	<first>

 </div>

 Scopes in directives:
 1) Shared Scope scope:false
 2) Inherited scope scope: true
 3) Isolated Scope scope: {}

 In Shared Scope

 Directive first and SampleController will share the same scope area


Reusable components:
-------------------
<card-view></card-view>

 <div class="cardHeader">
        	{{a}} {{b}}
        	<span class="pull-right" ng-click="delete(item)">
        		&times;
        	</span>
        </div>
        <div class="cardBody">
        	<img ng-src="images/{{img}}.png" class="cardImage" />
        	{{c}}
        	<span class="glyphicon glyphicon-edit pull-right">
        	</span>
        </div>



<div class="card col-xs-6 col-md-4 col-lg-3" 
        		ng-repeat="customer in customers">
       
</div>

Directive attributes:
a) template
b) templateUrl
c) scope
d) restrict [ Element Attribute Class M-comment]
e) replace
f) link
g) compile

i) transclude [ Read more]

	Note:
		<hello_world>
			some text......
		</hello_world>


--------------------------------------------		

json-server --watch app.json --port 9000 --static .

--------------

Angular Router

UI-Router
Angualar-Bootstrap project
Advantages of using UI-Router over basic Router
1) Master - Child
2) Multiple views

is based on state where as Anugular Router is based on RouterProvider[url]

----------------------------------------

Testing your code
------------------

1) Unit Testing
	Different Frameworks available:
	a) Jasmine
	b) Chai
	c) Sinon
	d) Mocha
	e) Qunit

	KARMA is a test runner for Unit Testing

	npm install karma 
	npm install karma-jasmine karma-chrome-launcher

	karma init ==> will create karma.conf.js


2) E2E testing
	
	Selenium
	Protractor


	npm install -g protractor
	webdriver-manager update
	webdriver-manager start

	Steps:
	1) Start JSON-server
	json-server --watch app.json --static . --port 9000

	2) Start selenium
	webdriver-manager start

	3) Run Protractor [ test/e2e folder]
	protractor conf.js

	