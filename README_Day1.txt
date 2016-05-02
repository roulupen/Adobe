
	JavaScript and AngularJS
	------------------------

	Banuprakash.C
	banuprakashc@yahoo.co.in
	------------------------

	Softwares Required:
	1) Editor
		SublimeText / VisualStudio Code / Eclipse JEE/ Notepad++
	2) Browser
		Chrome
	3) NodeJS
	4) npm modules will be installed as and when required.
	5) AngularJS files and bootstrap libraries will be shared in github.

-----------------------------------------------------------

JavaScript
	scripting language
	Interpreted
	Loosely typed

	var name = "Smith";

	var age = 22;

	JavaScript supports the following types of values:

	a) String
	b) Number
	c) boolean
	d) undefined
	e) null
	f) Object


	var result;

	--------------------------------

	JavaScript functions


	function  name(parameters) {

	}

	Every function is inherited from Function type

	---------------------

	functions can be pure functions or high order functions.

	----------

	var a = 10;

	function test() {
		console.log(a);
	}

	SpiderMonkey [ Acrobat ]

	V8 [ Chrome and nodeJS ]

	Continum 

	----------

		Window will be a global object
		and Windows lexical environment contains

		{a: 10, function:test}

		test contains <<scope>> which points to Window


	var a = 10;

	function test() {
		var a = 25;
		function inner() {
			console.log(a);
		}
		
	}
--------------------------------------------------------


	semicolon insertions

	var a = 10
	var b = 20;


	function test() {

	}
---------------------------------------------------------------


var f = function(no) { }

f(5);
-----------------------------------

more high order functions

passing function parameters

without high order
function forEach(values) {
	for(i=0; i < values.length; i++) {
		console.log(values[i]);
	}
}

var data = [56,3,788,3];

forEach(data);

-----

with high order

function print(elem) {
	console.log(elem);
}
	
function createMenu(elem) {
	code to create menu for elem;
}

function forEach(values, action) {
	for(i=0; i < values.length; i++) {
		action(values[i]);
	}
}
var data = [56,3,788,3];
forEach(data, print);
forEach(data, createMenu);
forEach(data, function (elem) { // });
----------------------------------------

Common high order functions used are:

1) MAP
	Given a collection, return a modified collection
2) REDUCE
	find sum, avg, max, min, etc
3) FILTER
	needs a collection and a predicate
4) sort	

-------------------------

OOP

JavaScript provides many built-in objects: 
String, Math, Date, XmlHttpRequest,JSON

User defined objects

1) JSON notation
 JavaScript Object notation.
 Restful Services
 Representational State Transfer
 	JSON, XML, RSS, ATOM

 	{} is used to represent an object
 	[] is used for array
 	data is stored in the form of key : value.
 	JSON understands the following types:
 	 String, number, boolean, undefied, null, objects

Example:

var products = [ { "id":100, "name":"Dell Laptop", "available": true }, 
			  	  { "id":101, "name":"MotoG", "available": true }
			  	 ];

2) by using Object constructor

  var emp = new Object();
  emp.id= 100;
  emp.firstName = 'Raj';
  emp[lastName] = 'Kumar';


3) Factory pattern

  var manager = Object.create(emp);
  manager.incharge = 'ABC';

4) Constructor pattern
	
	Adding State: 

 	function Employee(name, age) {
 		this.name = name;
 		this.age = age;
 	}
 	// this.name is the state of an object [ instance varaible]
 	var raj = new Employee('Raj',26);

 	var shyam = new Employee('Shyam',39);

 	Add behaviour:

 	function Employee(name, age) {
 		this.name = name;
 		this.age = age;
  	}

  	Employee.prototype// object owned instance methods
 		this.getDetails = function() {
 			return this.name + " , " + this.age;
 		}
// object owned instance methods
 		this.getDetails = function() {
 			return this.name + " , " + this.age;
 		}

 	var shyam = new Employee('Shyam',39);
 	shyam.getDetails();

 	var raj = new Employee('Raj',26);
 	raj.getDetails();

 	-------------

 	class owned instance methods [ Behaviour ]

 	function Employee(name, age) {
 		this.name = name;
 		this.age = age;
  	}
  	// class owned instance method
  	Employee.prototype.getDetails = function() {
 			return this.name + " , " + this.age;
 	}
 	//class owned static methods
 	Employee.doTask = function() {

 	}
 	var shyam = new Employee('Shyam',39);
 	shyam.getDetails();

 	var raj = new Employee('Raj',26);
 	raj.getDetails();

----------------------------------------------------------------

var update = function(name, age) {
	this.name = name;
	this.age = age;
}

var obj1 = {"name": "Smith", "age" : 22};

var obj2 = {"name": "Peter", "age" : 29};

update.call(obj1,"Raj",33);

update.call(obj2,"Rani",30);

update.call(obj2,["Rani",30]);
---------------------------------------


	JavaScript Patterns
	-------------------
	IIFE or self-executing function
	Immeditely invoke function expression

	(function() {// code })();


	1) Module pattern
		allows encapsulation

	2) Chain of Responsibility
		


	3) Factory

	4) Observable

	5) Namespace

