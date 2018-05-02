## Logistics
1. Student Introductions
2. Self Introductions
3. Courseware
4. Internet Access
5. Phones on silent

-


## How you will Benefit
* Learn to build Hybrid apps for mobile devices
* Gain hands-on experience
	- Generous mixture of presentation and labs
* Access to expereinced intructors.
  
-

## Requirements - You!
* Experience
* Practical knowledge of Html, and Javascript

* Equipment
	* Your own laptop
	* Node and Ionic and course-material installed
	* IDE of your choice, we suggest Visual Studio Code
	* PDF Reader

-

## Course Agenda: Morning

### Ionic Basics
* Generating your first project
* Anatomy of an Ionic Project
* Ionic CLI Commands
* Decorators
* Classes

-

## Course Agenda: Afternoon
* Templates
* Styling & Theming
* Navigation
* User Input
* Saving Data
* Fetching Data, Observables and Promises

-

## Covered in this section

* Agenda
* Installation
* New Concepts
	* EMCAScript 6
	* TypeScript
	* Web Components
	
-
-

####Sample Ionic HTML Template

```
<ion-menu [content]="content">	<ion-toolbar>		<ion-title>Pages</ion-title>	</ion-toolbar>	<ion-content>		<ion-list>			<button ion-item *ngFor="let p of pages" 
			(click)="openPage(p)"></button>		</ion-list>	</ion-content>
</ion-menu><ion-nav id="nav" [root]="rootPage" #content></ion-nav>
```
-
-
####Sample Ionic TypeScript Template

```
import { Component } from '@angular/core';import { Platform } from 'ionic-angular';import { HomePage } from './pages/home/home';@Component({	template: `<ion-nav [root]="rootPage"></ion-nav>`}) export class MyApp {		rootPage: any = HomePage;		constructor(platform: Platform) {		platform.ready().then(() => {});	}}
```


-
-

# ECMAScript 6 (ES6)

-

### ECMAScript 6 (ES6)

* ECMAScript is a standard,Javascript is an implementation of that standard. ECMAScript defines the standard and browsers implementit.

-

### ECMAScript 6 (ES6)

* In a similar way, HTML specifications (most recently HTML5) are defined by the organising body and are implemented by the browser vendors. Different browsers implement specifications in differentways, and there are varying amounts of support for different features, which is why some things workdifferently in different browsers.

-

# Classes

-
### Classes in Javascript

You can now use and implement Classes as a part of the language, instead of having an approximation of them. 

-

### Classes in Javascript

```
class Shape {	constructor (id, x, y) {		this.id = id		this.move(x, y)	}	move (x, y) {		this.x = x
		this.y = y	}}
		
```
-

# Modules

-

### Modules

Modules allow you to modularise your code into packages that can be imported anywhere you need inyour application, this is something that is going to be heavily used in Ionic.

-

### Modules

```
// lib/math.js	export function sum (x, y) { return x + y }	export var pi = 3.141593
```
```// someApp.js	import * as math from "lib/math"	console.log("2PI = " + math.sum(math.pi, math.pi))
```
```// otherApp.js	import { sum, pi } from "lib/math"	console.log("2PI = " + sum(pi, pi))
```

-

# Promises

-

### Promises

Promises are something that have been made available by services like ngCordova previously, but nowthey are natively supported, meaning you can do something like this:

```
doSomething().then((response) => {	console.log(response);});

```

-

# Block Scoping

-

### Block Scoping (let Keyword )

Currently, if you define a variable in Javascript it is available anywhere within the function that it was definedin. The new block scoping features in ES6 allow you to use the let keyword to define a variable only withina single block of code like this:

```
for (let i = 0; i < a.length; i++) {	let x = a[i];}
```

-

# Fat Arrow Functions

-

### Fat Arrow Functions

New Way ( Good )

```
someFunction((response) => {	console.log(response);});

```
Old way (Meh)

```
someFunction(function(response){	console.log(response);});
```

-

### Fat Arrow Functions

Old way (Meh)

To access the parent method we have to do some work 
```
var me = this;

someFunction(function(response){	console.log(me.someVariable);});
```

-

### Fat Arrow Functions

New Way ( Good )

```
someFunction((response) => {	console.log(this.someVariable);});

```

-

# TypeScript

-

### Typescript

A typed superset of JavaScript that compiles to plain JavaScript

```
function add(x: number, y :number):number {	return x + y;}add('a', 'b'); // compiler error
// this function can only accept numerical input

```

-

# Transpiling

-

### Transpiling

Transpiling means converting from one language to another language. Why is this important to us? Basically,ECMAScript 6 gives us all of this cool new stuff to use, but ES6 is just a standard and it is notcompletely supported by browsers yet. 

-

### Transpiling

We use a transpiler to convert our ES6 code into ES5 code (i.e. theJavascript you’re using today) that is compatible with browsers.In the context of Ionic applications.

-
### Transpiling

* Here’s how the process works:	* You use ***ionic serve*** to run the application	* All the code inside of the app folder is transpiled into valid ES5 code	* A single bundled Javascript file is created and run
	* You don’t need to worry about this process as it is all automatically handled by Ionic.

-

# Web Components

-

### Old way

```
<div id="slider">	<input checked="" type="radio" name="slider" id="slide1" selected="false">	<input type="radio" name="slider" id="slide2" selected="false">	<input type="radio" name="slider" id="slide3" selected="false">	<input type="radio" name="slider" id="slide4" selected="false">	<div id="slides">		<div id="overflow">			<div class="inner">				<img src="images//rock.jpg">				<img src="images/grooves.jpg">				<img src="images/arch.jpg">				<img src="images/sunset.jpg">			</div>
		</div>	</div>	<label for="slide1"></label>	<label for="slide2"></label>	<label for="slide3"></label>	<label for="slide4"></label></div>
```

-

### Using Components

```
<img-slider>	<img src="images/sunset.jpg" alt="a dramatic sunset">	<img src="images/arch.jpg" alt="a rock arch">	<img src="images/grooves.jpg" alt="some neat grooves">	<img src="images/rock.jpg" alt="an interesting rock"></img-slider>

```

-
-

# Ionic Basics

* (Live Walkthrough)

-
-


# Decorators

-

### Decorators

Each class (which we will talk about in the next section) you see in an Ionic application will have a decorator.A decorator looks like this:

```
@Component({	someThing: 'somevalue',	someOtherThing: [Some, Other, Values]})
```

-

### Decorators

* They definitely look a little weird, but they play an important role. 
* Provide some metadata about the class you are defining, and 
* They always sit directly above your class

```
@Decorator({	/*meta data goes here*/})export class MyClass {	/*class stuff goes here*/}
```

-

### Decorators

The decorator name itself is quite useful, here’s a few you might see in an Ionic application:* @Component* @Pipe* @Directive

-

### @Component

* A @Component is not specific to Ionic, it is used generally in Angular 2. 
* A lot of the functionality provided by Ionic is done through using components. 
* In Ionic, for example, you might want to create a search bar,which you could do by using one of the components that Ionic provides like this:

```
<ion-searchbar></ion-searchbar>

```

-

### @Component

Ionic provides a lot of components but you can alsocreate your own custom components, and the decorator for that might look something like this:

```
@Component({	selector: 'my-cool-component'})
```

-

### @Component

Which would then allow you to use it in your templates like this:

```
	<my-cool-component></my-cool-component>
```

-

# @Directive

-

### @Directive

The @Directive decorator allows you to create your own custom directives. Typically, the decorator wouldlook something like this:

```
@Directive({	selector: '[my-selector]'})
```

-

### @Directive

Then in your template you could use that selector to trigger the behaviour of the directive you have createdby adding it to an element:

```
<some-element my-selector></some-element>
```

-

### @Directive

* It might be a little confusing as to when to use **@Component** and **@Directive** , as they are both quite similar.* The easiest thing to remember is that if you want to modify the behaviour of an existing component use adirective, if you want to create a completely new component use a component.

-

# @Pipe

-

### @Pipe
@Pipe allows you to create your own custom pipes to filter data that is displayed to the user, which canbe very useful. The decorator might look something like this:

```
@Pipe({	name: 'myPipe'})
```
-

### @Pipe

Which would then allow you to implement it in your templates like this:

```
<p>{{someString | myPipe}}</p>
```
Now someString would be run through your custom myPipe before the value is output to the user.

-

# @Injectable

-

### @Injectable

* An @Injectable allows you to create a service for a class to use. A common example of a service createdusing the @Injectable decorator, is a Data Service that is responsible for fetching and saving data. 

-

### @Injectable

* Rather than doing this manually in yourclasses, you can inject your data service into any number of classes you want, and call helper functionsfrom that Data Service.

-

# @IonicPage

-
### @IonicPage

* The @IonicPage decorator works in tandem with the NavController to help provide navigation, and “lazyload” pages. 
* It is included by default at the top of any “page” that is generated in your application, butit is worth noting that a “page” is nothing more than a normal @Component. 
* Adding the @IonicPagedecorator just builds a little more functionality into this @Component.

-

### @IonicPage 
```
@IonicPage()@Component({	selector: 'home-page',	templateUrl: 'home.html'})
```
