# Beginner JavaScript 2

---

### Table of Contents
---

1. HTML
2. Tags
3. The DOM
4. CSS
8. IDs and Classes
11. JavaScript DOM Interaction
13. jQuery
14. AJAX
15. HTTP
16. XHR
17. CORS

---

### HTML
---
### Hypertext Markup Language

---

### What does the name mean?

- **Hypertext**: text which links to other text

- **Markup**: document annotation and formatting

---

### Tags

- Keywords which denote the structure of a document

- Parsed into the DOM and are stored internally

- Can hold attributes

		<div attr="dandy"> foo </div>

---

### The DOM
---
### The Document Object Model

---

### What is it?

- Just a **conventional representation** of your document created by the browser

- Convention extends to HTML, XML, and by extension SVG (in XML format)

---

### What the browser does with your documents

- How your document is represented and interacted with is based on the DOM, not the original document!

- This parsing process implemented because people are bad at coding

- Cleans up and standardizes the 'tag soup' to provide a valid model

---

### The DOM Tree

![DOM Tree](http://www.w3schools.com/js/pic_htmltree.gif)

---

### XML
---
### Extesnible Markup Language

- Designed for data interchange

- Less favorable than JSON because of its verbosity

[XML vs JSON](http://www.utilities-online.info/xmltojson/#.VgihbNsViko)

---

### SVG
---
### Scalable Vector Graphics

- Written in XML format

- Renders graphics based on vector quantities that don't lose quality when resized

[SVG Circle](https://jsfiddle.net/HeyZoos/90vsth3x/)

---

### CSS
---
### Cascading Style Sheets

---

- Defines presentation of a document, how it will be rendered

- Looks at and acts on element references throughout the DOM

- How to specify which element? CSS can look at it's element name...

---

### Select by element name

	div {

		border: 5px dashed blue;
		color: red;

	}

---

### IDs and Classes

- Or with it's attributes!

- Within the DOM elements carry around attributes which distinguish each other or carry data

- They can be selected for!

		<div id="someId"> I live in an ID! </div>
		<div class="someClass"> I live in a class! </div>

---

### IDs

- **ID** "id" attribute in HTML elements

- selected with a '#' in CSS

- represent a single, specific instance of an element with a special role or job

- convention dictates **there can only be one!** 

---

### Classes

- **Classes** "class" attribute in HTML elements

- selected with a '.' in CSS

- represents a category of elements with certain jobs

- you can make plenty of these!

---

### IDs and Classes

	#id {

	}

	.class {

	}

---

### JavaScript DOM Interaction

---

### The 'window' object

- Reference to the window itself!

---
### The 'document' object

- A reference to the document loaded into the browser

---

### JavaScript DOM Interaction

- Both of these references and the majority of their methods provided by the DOM!

- When JavaScript creates an execution context, it creates a reference to a global object

- Attaches global variables to this object

---

### JavaScript DOM Interaction

- Within browsers, that ends up being window, but that doesn't always have to be the case!

- When JavaScript is run outside of the browser (for example in node) something else is used in that environment

---

### Query Selectors

- An example of a method provided by the DOM

- Performs a fundamental task of returning a reference to an HTML element

- Can be assigned to local references in JavaScript using the 'var' keyword

		var targetElement = document.querySelector("selector");

		targetElement.innerHTML = "I EXIST.";

---

### jQuery

---

### What is it?

- A lightweight JavaScript library

- Simplifies a lot of the common use-cases of JavaScript

- Very extensible, has been designed to work across all major browsers

		$("selector").text("I STILL EXIST.")

---

### AJAX
---
### Asynchronous JavaScript and XML

---

### What is it?

- It is just an approach to make fast responsive user interfaces.

- Involves all above mentioned technologies and the very important **XMLHTTPRequest Object**.

- Makes small updates to subsections of the page without refreshing the entire thing.

- This enables the development of **single-page** applications

---

### Why is it 'asynchronous'?

- Client and server run independently of each other.

- The browser doesn't freeze until response is received from the server.

- Following a call, control is returned immediately to you as the user.

- But never forget: JavaScript itself is **synchronous**.

---

### HTTP
---
### Hypertext Transfer Protocol

---

### What is it?

- **Protocol** Agreed upon format for data exchange between two parties

- Determines how data is transmitted and how servers and browsers are meant to handle it

- Involves a series of request and response actions

		GET /foo.html HTTP/1.1     (This is the Client Request-Line)

		HTTP/1.1 200 OK            (This is Server Status-Line)

---

### XHR
---
### XMLHTTPRequest

---

### What is it?

- A JavaScript object that provides a way to retrieve piece of a data

- Can be used to retrieve any type of data, not just XML

- It allows for you to update just a part of your page without doing a full refresh

- Involved heavily in AJAX programming

		var xmlhttp = new XMLHttpRequest();
		xmlhttp.open("GET", url, true);
		xmlhttp.send();

---

### CORS
---
### Cross Origin Resource Sharing

---

- Many servers place restrictions on where a domain can make requests (of the XML variety) from

- A way to safely circumvent the same-origin policy

- You can set HTTP headers which describe other domains from which requests are approved

---

### Thank you!

---
