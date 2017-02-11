#Front-end Job Interview Questions

This file contains a number of front-end interview questions that can be used when vetting potential candidates. It is by no means recommended to use every single question here on the same candidate (that would take hours). Choosing a few items from this list should help you vet the intended skills you require.

**Note:** Keep in mind that many of these questions are open-ended and could lead to interesting discussions that tell you more about the person's capabilities than a straight answer would.

## Table of Contents

  1. [General Questions](#general-questions)
  1. [HTML Questions](#html-questions)
  1. [CSS Questions](#css-questions)
  1. [JS Questions](#js-questions)
  1. [Testing Questions](#testing-questions)
  1. [Performance Questions](#performance-questions)
  1. [Network Questions](#network-questions)
  1. [Coding Questions](#coding-questions)
  1. [Fun Questions](#fun-questions)

## Getting Involved

  1. [Contributors](#contributors)
  1. [How to Contribute](https://github.com/h5bp/Front-end-Developer-Interview-Questions/blob/master/CONTRIBUTING.md)
  1. [License](https://github.com/h5bp/Front-end-Developer-Interview-Questions/blob/master/LICENSE.md)

#### General Questions:

* What did you learn yesterday/this week?
* What excites or interests you about coding?
* What is a recent technical challenge you experienced and how did you solve it?
* What UI, Security, Performance, SEO, Maintainability or Technology considerations do you make while building a web application or site?
* Talk about your preferred development environment.
* Which version control systems are you familiar with?
* Can you describe your workflow when you create a web page?
* If you have 5 different stylesheets, how would you best integrate them into the site?
* Can you describe the difference between progressive enhancement and graceful degradation?
* How would you optimize a website's assets/resources?
* How many resources will a browser download from a given domain at a time?
  * What are the exceptions?
* Name 3 ways to decrease page load (perceived or actual load time).
* If you jumped on a project and they used tabs and you used spaces, what would you do?
* Describe how you would create a simple slideshow page.
* If you could master one technology this year, what would it be?
* Explain the importance of standards and standards bodies.
* What is Flash of Unstyled Content? How do you avoid FOUC?
* Explain what ARIA and screenreaders are, and how to make a website accessible.
* Explain some of the pros and cons for CSS animations versus JavaScript animations.
* What does CORS stand for and what issue does it address?

#### HTML Questions:

* What does a `doctype` do?
* What's the difference between full standards mode, almost standards mode and quirks mode?
* What's the difference between HTML and XHTML?
* Are there any problems with serving pages as `application/xhtml+xml`?
* How do you serve a page with content in multiple languages?
* What kind of things must you be wary of when design or developing for multilingual sites?
* What are `data-` attributes good for?
* Consider HTML5 as an open web platform. What are the building blocks of HTML5?
* Describe the difference between a `cookie`, `sessionStorage` and `localStorage`.
* Describe the difference between `<script>`, `<script async>` and `<script defer>`.
* Why is it generally a good idea to position CSS `<link>`s between `<head></head>` and JS `<script>`s just before `</body>`? Do you know any exceptions?
* What is progressive rendering?
* Have you used different HTML templating languages before?

#### CSS Questions:

* What is the difference between classes and IDs in CSS?
* What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?
* Describe Floats and how they work.
* Describe z-index and how stacking context is formed.
* Describe BFC(Block Formatting Context) and how it works.
* What are the various clearing techniques and which is appropriate for what context?
* Explain CSS sprites, and how you would implement them on a page or site.
* What are your favourite image replacement techniques and which do you use when?
* How would you approach fixing browser-specific styling issues?
* How do you serve your pages for feature-constrained browsers?
  * What techniques/processes do you use?
* What are the different ways to visually hide content (and make it available only for screen readers)?
* Have you ever used a grid system, and if so, what do you prefer?
* Have you used or implemented media queries or mobile specific layouts/CSS?
* Are you familiar with styling SVG?
* How do you optimize your webpages for print?
* What are some of the "gotchas" for writing efficient CSS?
* What are the advantages/disadvantages of using CSS preprocessors?
  * Describe what you like and dislike about the CSS preprocessors you have used.
* How would you implement a web design comp that uses non-standard fonts?
* Explain how a browser determines what elements match a CSS selector.
* Describe pseudo-elements and discuss what they are used for.
* Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.
* What does ```* { box-sizing: border-box; }``` do? What are its advantages?
* List as many values for the display property that you can remember.
* What's the difference between inline and inline-block?
* What's the difference between a relative, fixed, absolute and statically positioned element?
* The 'C' in CSS stands for Cascading.  How is priority determined in assigning styles (a few examples)?  How can you use this system to your advantage?
* What existing CSS frameworks have you used locally, or in production? How would you change/improve them?
* Have you played around with the new CSS Flexbox or Grid specs?
* How is responsive design different from adaptive design?
* Have you ever worked with retina graphics? If so, when and what techniques did you use?
* Is there any reason you'd want to use `translate()` instead of *absolute positioning*, or vice-versa? And why?

#### JS Questions:

* Explain event delegation
* Explain how `this` works in JavaScript
* Explain how prototypal inheritance works
* What do you think of AMD vs CommonJS?
* Explain why the following doesn't work as an IIFE: `function foo(){ }();`.
  * What needs to be changed to properly make it an IIFE?
* What's the difference between a variable that is: `null`, `undefined` or undeclared?
  * How would you go about checking for any of these states?
* What is a closure, and how/why would you use one?
* What's a typical use case for anonymous functions?
* How do you organize your code? (module pattern, classical inheritance?)
* What's the difference between host objects and native objects?
* Difference between: `function Person(){}`, `var person = Person()`, and `var person = new Person()`?
* What's the difference between `.call` and `.apply`?
* Explain `Function.prototype.bind`.
* When would you use `document.write()`?
* What's the difference between feature detection, feature inference, and using the UA string?
* Explain Ajax in as much detail as possible.
* What are the advantages and disadvantages of using Ajax?
* Explain how JSONP works (and how it's not really Ajax).
* Have you ever used JavaScript templating?
  * If so, what libraries have you used?
* Explain "hoisting".

In javascript, every time that we create a new function or object, all variable declarations and named functions are hoisted to the top. 
* Describe event bubbling.

Event bubbling is another term for event propagation. If a particular DOM node, let's say a p element, has a child button element, and that button has a click event listener, then the parent p element will also receive the click event when the button is clicked. The click event 'bubbles up', or propagates onto all the parent elements, all the way up to the root of the document, and finally it will even send the event onto the entire window object. It is important to remember, that any DOM node can call the stopPropagation method to stop the event from bubbling up to further parent nodes. 
Here is an example: 
```
<p>
  Demo paragraph
  <button>button</button>
</p>
<script>
  var p = document.querySelector("p");
  var button = document.querySelector("button");
  p.addEventListener("mousedown", function() {
    console.log("Handler for paragraph.");
  });
  button.addEventListener("mousedown", function(event) {
    console.log("Handler for button.");
    if (event.which == 3)
      event.stopPropagation();
  });
</script>
```
Example taken from Eloquent Javascript (excellent book by the way)

The 'event' argument that we added to the button event listener is an object that represents the mousedown event. It has a 'which' property that usually represents more detail about the particular event. For a mousedown event, the which property can be a 1 to represent the left button, a 2 for the middle button, and a 3 if it was a right mouse button click. In the example above, if the button receives a left mouse button click then the following will log in your console: 
```
Handler for button.
Handler for paragraph.
```
If the button is clicked with the right button, then only "Handler for button" will log, because we have stoped any further bubbling up. 


* What's the difference between an "attribute" and a "property"?
* Why is extending built-in JavaScript objects not a good idea?
* Difference between document load event and document DOMContentLoaded event?
* What is the difference between `==` and `===`?
* Explain the same-origin policy with regards to JavaScript.
* Make this work:
```javascript
duplicate([1,2,3,4,5]); // [1,2,3,4,5,1,2,3,4,5]
```
* Why is it called a Ternary expression, what does the word "Ternary" indicate?
* What is `"use strict";`? what are the advantages and disadvantages to using it?
* Create a for loop that iterates up to `100` while outputting **"fizz"** at multiples of `3`, **"buzz"** at multiples of `5` and **"fizzbuzz"** at multiples of `3` and `5`
* Why is it, in general, a good idea to leave the global scope of a website as-is and never touch it?
* Why would you use something like the `load` event? Does this event have disadvantages? Do you know any alternatives, and why would you use those?
* Explain what a single page app is and how to make one SEO-friendly.
* What is the extent of your experience with Promises and/or their polyfills?
* What are the pros and cons of using Promises instead of callbacks?
* What are some of the advantages/disadvantages of writing JavaScript code in a language that compiles to JavaScript?
* What tools and techniques do you use debugging JavaScript code?
* What language constructions do you use for iterating over object properties and array items?
* Explain the difference between mutable and immutable objects.
  * What is an example of an immutable object in JavaScript?
  * What are the pros and cons of immutability?
  * How can you achieve immutability in your own code?
* Explain the difference between synchronous and asynchronous functions.

A synchronous function is simple - it runs, and the runtime environment will only continue to the rest of the code once it has returned a value from the current synchronous function. In other words, it is _blocking_, it only runs the rest of your code once the current synchronous task has completed. It is crucial to understand that Javascript itself is single threaded and synchronous. It has no inherent asynchronous functions that it may perform, with the exception of the primitive Promises that have come with ES6. (if you are confused, keep reading below). 

On the other hand, an asynchronous function is non-blocking, it starts to run the function, and then continues to perform other operations while continuing to run the original async function. It is much smarter to use aysnc functions on operations that may be intensive (such as database operations). Here is a simple example:
```
database.query("SELECT People FROM myTable", function(result) {
    console.log("found all People from myTable");
});
console.log("We are pulling from the database");
=> 
We are pulling from the database
found all People from myTable
```
What you CAN do with javascript is run async functions that use some sort of API provided by the runtime environment. For example, the browser provides an HTML Timing API which allows you to run setTimeout (first places it in a task queue before the JS event loop pushes it into the call stack). Similaryly, the Node.js environment allows you to schedule async tasks. 


* What is event loop? (answer joined with next answer below)
 * What is the difference between call stack and task queue?
  
Javascript is a single threaded programming language, meaning that the javascript runtime only has one single call stack. This also implies that the javascript runtime can only run one unit of code at a time. It can only do one thing at a time. Everytime your code hits an invoked function, that function is added to the stack. "Blowing your call stack" is when you find yourself in an infinite loop of additions to the stack (function invocations). For example: 
```
function peh() {
  return peh()
}
```
will give you an error: 
```
RangeError: Maximum call stack size exceeded
```
Your browser was smart, and was able to recognize that far too many functions were being added to the callstacks (thousands), and that probably wasn't your intent, so time to find that bug. 

So this begs the question- why is javascript non-blocking/Async in it's nature? As mentioned, indeed there is only one call stack; however, certain async functions operate through a WebAPI, such as the well known setTimeout function. This function is actually not part of the javascript V8 runtime, but is part of the browser. The browser makes a webAPI call, where there will be a clock tick for the amount of time you alloted in your setTimeout function. As soon as the that time is up, the webAPI will take the callback that you provided to the callback function, and push it into something called the task queue. 

Now, the EVENT LOOP has a simple task- it watches the call stack and runs the next function, or if the call stack is empty, it will go down and grab the next callback from the task queue and add it to the call stack, which will essentially run that callback right away. 
  
* Explain the differences on the usage of `foo` between `function foo() {}` and `var foo = function() {}`

The first is a named function. The second is a variable declaration (the variable happens to hold a function). 
Imagine we have the following code: 
console.log('noo is ', noo);
console.log('foo is ', foo)
console.log('joo is ', joo);
function noo() {};
var foo = function() {};

The output will be the following:
noo is  function noo() {}
foo is  undefined
console.log('joo is ', joo);
                       ^
ReferenceError: joo is not defined

Because of javascript hoisting, named functions, as well as variable declarations, are brought to the top of the scope. In other words, you can imagine the code working like this behind the scenes:
function noo() {};
var foo;

console.log('noo is ', noo);
console.log('foo is ', foo)
console.log('joo is ', joo);
foo = function() {};

Running the code will produce the same as the above code. The console logs that 'foo is undefined' because indeed it has reference to foo (remember it was hoisted to the top of the scope), but ONLY to the declaration of the variable foo, and not to the value. You can think of the machine saying "ok, sure I have allocated memory to a variable called foo. It still only has it's default value of undefined, but it's there... it exists.'



#### Testing Questions:

* What are some advantages/disadvantages to testing your code?

Of course writing tests takes time. In the case that there is an important deadline centered around a client request, a company may choose to delay writing tests in order to meet that deadline. 

However, the whole point of functional/integration tests is to save you and your organization headache in the future by finding bugs early on. If the user sign up page breaks right when you happen to push an improvement to the photo uploader, then it is almost certain that the new photo uploader is causing the break. On the other hand, if the sign up bug is not discovered until a week later after a customer sends a complaint email, then it can be from the photo uploader, or from any of the other 10 pushes that came in the last week. 



* What tools would you use to test your code's functionality?

To unit test, I usually resort to using the Google Developer Console Debugger, or simply old fashioned console logs. I would highly recommend installing a javascript console directly into sublime text, here are instructions how. http://www.wikihow.com/Create-a-Javascript-Console-in-Sublime-Text

For functional/integration tests I would recommend Travis, especially if you have your code on Github since it integrates automatically. It is free for open source, and costs for private repos. It also has cool features, such as integration with Slack, so can give your team a heads up when a pull request passes tests and is safe to merge. https://github.com/travis-ci/travis-ci


* What is the difference between a unit test and a functional/integration test?

A unit test is concerned with testing if a specific encapsulated portion of code produces the desired result. This 'encapsulated portion of code' is usually a single function or algorithm. A solid unit test will also test for edge cases. 

On the other hand, a functional/integration test covers a much larger portion of your application, and the intent is to test whether any new code that has been introduced has broken anything. Ideally, in a production level application, you would want to have 100% code coverage, meaning that all corners of the app are being tested any time new code is pushed. 



* What is the purpose of a code style linting tool?

A linting tool is typically an add-on to your code editor, that keeps the developer 'in check' with their code style by highlighting or giving some sort of indication in your code editor that whatever code you just wrote does not follow certain guidelines. Even if your code technically has proper syntax, it is also important for it to be standard and legible for other colleagues, and a linting tool helps with that. Eslint is what I personally use. 

#### Performance Questions:

* What tools would you use to find a performance bug in your code?
* What are some ways you may improve your website's scrolling performance?
* Explain the difference between layout, painting and compositing.

#### Network Questions:

* Traditionally, why has it been better to serve site assets from multiple domains?

The biggest reason is for performance. Traditionally, a browser has only been able to serve two concurrent requests to a single domain at the same time. However, you can send concurrent requests to various domains at the same time. This is not as much of an issue now as it used to be, since most modern browsers can serve at least 6 concurrent requests to a single domain, but the principle remains the same. 

A secondary benefit would be not being overly reliant on a single source. If all of your assets come from the exact same domain, then if that domain is down, or being slow, then every single resource on your page will be laggy or fail. 


* Do your best to describe the process from the time you type in a website's URL to it finishing loading on your screen.

Even before you hit 'Enter' on your keyboard, there is a lot of code being run behind the scene. First the browser is looking to make your life easier by pre-populating the url input for you, based on bookmarks, history, and favorites. 

As soon as you hit enter, whatever you had in the url bar is parsed- there is a protocol (http or https), and there is a domain. If there is not a valid domain (for example https://github.com) provided, then it will treat whatever you typed as web search term, and redirect the user to google search results. If a protocol is not provided, but the domain is legit (www.github.com or github.com), then the browser will check an HSTS list (HTTP Strict Transport Security), which is essentially a list of websites that have opted to only be communicated with via HTTPS. Otherwise the browser will assume HTTP. 

The next step is DNS lookup. A domain name is actually the more 'human friendly' way (www.github.com) to mask an ip address that is in decimal format, such as 192.30.253.113. First the browser checks the cache, and then checks a local "hosts" file whose location on the computer varies by computer and operating system. Only if the domain cannot be "resolved" in this way, will the browser make a request to a DNS server. This lookup should be very fast, as DNS servers essentially have one purpose, and are optimized for this quick retrieval (similar in structure to a hashing function). 

Once the IP address has been optained, the browser takes the IP and the Port number (the HTTP protocol defaults to port 80, and HTTPS to port 443), and requests a TCP socket stream. In order for this TCP socket stream (connection) to happen, one computer must be waiting, or listening, for other computers to start talking to it. In order for this computer to be able to listen to multiple computers, and to open up multiple connections, it has different ports. Protocols also have defaults (which makes it easier for everyone), sending an email requires the SMTP protocol, and the expectation is that port 25 is used. Once the correct port number has been selected, a connection is established, and the listening computer is the server and the connecting computer is the client. 

TCP stands for Transmission Control Protocol, and it is a protocol that all internet connected devices can follow, in fact most of the communication on the internet is built on top of it. When there is communication via the internet, it is important that the individual bits of data that flow from one computer to another arrive to the correct destination in the correct order, and TCP is what ensures this. 



* What are the differences between Long-Polling, Websockets and Server-Sent Events?
The most traditional and common form of communication between a client and a server is through a series of requests from the client and responses from the server using HTTP, which has become the standard. Websockets are revolutionary in that they allow for the server to send unsolicited information directly to the client. It is important to note that in websocket communication, the client can still communicate/send real-time messages to the server. Browsers first introduced support for websocket in 2010. The Websocket communications protocol is completely separate from HTTP, except for the initial 'handshake' that establishes the websocket connection between client and server in the first place. The handshake HTTP request must include an 'Upgrade: websocket' header. 

HTML5 SSE (Server-sent events), are a similar form of communication, in the sense that the client can send unsolicited real-time messages to the client. However, it is not a two-way flow of communication, so the client cannot send real-time messages to the server like in Websockets. Another key difference is that with SSE the client cannot connect to a server on another domain. 

Long-Polling is similar to the standard form of HTTP communication between client and server, but in the case that it receives a request from the client and has no response data available, it will not send back an empty response, but rather, hold onto that request until some data is available. As soon as the client receives a response, it will send out another request to the server, so the server will always have a pending request to respond to. 

* Explain the following request and response headers:
 * Diff. between Expires, Date, Age and If-Modified-...
  
Expires and Cache-Control: max-age= are both headers that dictate when a cached item will expire. However, the Expires merely gives the date and time after which the response is considered 'stale.' However, the original resource that was sent will still exhist and will not be changed after the expiration date. The Cache-Control: max-age header indicates the max age that the client is willing to accept of an incoming response (the only exception is if there is _also_ a max-stale header present). 

Date indicates the date at which the message was created. Clients should only send a Date header in messages that include a significant body, as in the case of the PUT and POST requests, and even then it is optional.

The If-Modified-Since header will only return a response IF the resource has been modified since the indicated date. If there has been no recent modification since the date, then the resource is considered stale, and a 304 (not modified) response will be returned without any message-body.

Here is the proper formatting for each header: 
- Expires: Thu, 01 Dec 1994 16:00:00 GMT
- Cache-Control: max-age= 3360 
- Date: Tue, 15 Nov 1994 08:12:31 GMT
- If-Modified-Since: Sat, 29 Oct 1994 19:43:31 GMT

 * Do Not Track
 
The DNT Header was first implemented by Mozilla Firefox in 2010, and requests that a web-app disables its tracking. The DNT header can accept one of three values: a 1 is when a user 'opts out' and does not want to be tracked, a 0 is when a user consents to being tracked, or null when there has been no value set because the user has not set a preference. The default is no header sent (same as null value). There was controversy at one point when IE 10 set the default value of 1 for users, when the Digital Advertising Alliance claimed that such a decision must be made by the user. 
 
 * Cache-Control
 
The Cache-Control header gives the specification for caching. A client request can have the following cache-control headers:
```
Cache-Control: max-age=<seconds>
Cache-Control: max-stale[=<seconds>]
Cache-Control: min-fresh=<seconds>
Cache-control: no-cache 
Cache-control: no-store
Cache-control: no-transform
Cache-control: only-if-cached
```

The first 3 all refer to cache expirations. Cache-Control: max-age=10000 indicates that the cached item will be considered "fresh" (not expired) for 10K seconds from when the item is cached. The Cache-Control: max-stale[10000] indicates that the client is willing to accept a cached item that is past its expiration time by 10K seconds; the cached item may be stale, but the client is still willing to accept. Cache-Control: min-fresh=2000 indicates that the client is willing to accept a cached item that will still remain fresh for a minimum of 2000 seconds. 

The Cache-control: no-store specifically requests that the cache should not store anything. 
The Cache-control: only-if-cached header is included when the client does not want anything new from the server, only a cached response.

The Server response can include the following Cache-Control headers: 
```
Cache-control: must-revalidate
Cache-control: no-cache
Cache-control: no-store
Cache-control: no-transform
Cache-control: public
Cache-control: private
Cache-control: proxy-revalidate
Cache-Control: max-age=<seconds>
Cache-control: s-maxage=<seconds>
```

The Cache-control: must-revalidate indicates that each cached item may only be used if it has not expired, and they must be validated. 

Also, to turn off caching you can send the following header: 
```
Cache-Control: no-cache, no-store, must-revalidate
```

 * Transfer-Encoding
 * ETag
 * X-Frame-Options
  
  
  
* What are HTTP methods? List all HTTP methods that you know, and explain them.

HTTP stands for Hypertext Transfer Protocol, it is the primary format by which the client and server communicate. The 'type' of HTTP request that is sent out from the client to the server indicates what sort of communication is in place. The two most common HTTP methods are a 'GET' and a 'POST'; 'GET' request is primarily for retreiving some sort of data from a resource, while a 'POST' is primarily for sending over some sort of data. For example, a 'GET' request is the most standard for retreiving the homepage from a server when a user lands on a website (as the verb 'get' indicates, you are getting the initial homepage served to you). While a 'POST' request will be more standard for when a user clicks the submit button after leaving a comment on an article. However, the type of request that is sent out is not just for convention, but also has subtle differences: 
- GET requests can be cached
- GET requests remain in browser history
- GET requests should never be used for sensitive data (the data is public and visible in the url)
- POST requests cannot be cached
- POST requests are not in browser history
- POST requests have no restrictions on data length
- POST requests are more secure than GET requests

There are additional HTTP Methods: 
OPTIONS - These are sent out automatically by the browser to a server that there has been a connection established with. An OPTIONS request gets a response from the server with all of the HTTP methods that it supports. It is a 'check' done by the browser primarily behind the scenes. 
DELETE - Whenever the intention is to delete a certain resource. An example would be if a user wishes to permanently delete their user data from a website.
HEAD - A request method that is exactly the same as a GET, but only receives the HTTP Headers in the response, and not the body. 
PUT - A PUT request is very similar to a POST; in fact, it can be seen as a more specific type of POST request (both send over data to the server). A POST request is more general in the sense that the URI in the request can indeed be a data-accepting process, but can also be a gateway to another protocol, or have some sort of other action that is taken. On the other hand, a PUT request must be accepted by the server at that exact URI; the only other option is to send a 301 'Moved Permanently' response, at which point the user may choose to redirect the request. An example of a PUT request would be uploading a file to a specific uri. 
CONNECT - Converts the request connection to a transparent TCP/IP tunnel (not used so often). 



#### Coding Questions:

*Question: What is the value of `foo`?*
```javascript
var foo = 10 + '20';
```
'1020'

An integer plus a string always results in a string. Even 10 + 'twenty' === '10twenty'

*Question: How would you make this work?*
```javascript
add(2, 5); // 7
add(2)(5); // 7
```
var add = (x, y = 0) => {
  let next = x + y;
  return (g = 0) => {
    return g + next;
  };
};

This is basic currying in Javascript. Both add(2, 5) and add(2)(5) will return 7. Note that default parameters are much smoother and easier to define with ES6 than with ES5.

*Question: What value is returned from the following statement?*
```javascript
"i'm a lasagna hog".split("").reverse().join("");
```
"goh angasal a m'i"


*Question: What is the value of `window.foo`?*
```javascript
( window.foo || ( window.foo = "bar" ) );
```
The value of window.foo will be "bar". We are running an "or" expression above. Since the first part, window.foo is undefined for now, it is falsey, and therefore will attempt to run the other half, in this case window.foo = 'bar', and since variable assignment is truthy, this portion will execute and successfully define the foo variable on the window object as "bar".

*Question: What is the outcome of the two alerts below?*
```javascript
var foo = "Hello";
(function() {
  var bar = " World";
  alert(foo + bar);
})();
alert(foo + bar);
```
First there will be a "Hello World" alert, since the immediately invoked function has variable bar defined inside of it, and also has access to its global scope, where foo was defined. Then the browser will attempt to give you a 2nd alert but will give you a reference error since bar is not defined (var bar = ' World' is private to the immediately invoked function). 

*Question: What is the value of `foo.length`?*
```javascript
var foo = [];
foo.push(1);
foo.push(2);
```
2

*Question: What is the value of `foo.x`?*
```javascript
var foo = {n: 1};
var bar = foo;
foo.x = foo = {n: 2};
```
foo.x is undefined. The code on the last line moves from right to left, so first foo is reassigned to object {n: 2}, then foo.x is assigned foo. Yet it comes out as undefined. Interestingly, if we replace foo with another variable, such as bar:
foo.x = bar = {n: 2}
then foo === {n: 1, x: {n: 2}} which is more consistent with what we would expect it to be. 


*Question: What does the following code print?*
```javascript
console.log('one');
setTimeout(function() {
  console.log('two');
}, 0);
console.log('three');
```
It prints
'one'
'three'
'two'

I was under the impression that occasionally it may print "one" "two" "three", since the setTimeout function has a 0 second interval, and because wrapping the console.log('two') in the setTimeout is not a time intensive operation, but after testing indeed it seems to consistently console.log in the order above.



#### Contributors:

Questions answered by Aljosha Novakovic @ollynov

Please feel free to contribute edits or to improve any of the answers. 

This document started in 2009 as a collaboration of [@paul_irish](https://twitter.com/paul_irish) [@bentruyman](https://twitter.com/bentruyman) [@cowboy](https://twitter.com/cowboy) [@ajpiano](https://twitter.com/ajpiano)  [@SlexAxton](https://twitter.com/slexaxton) [@boazsender](https://twitter.com/boazsender) [@miketaylr](https://twitter.com/miketaylr) [@vladikoff](https://twitter.com/vladikoff) [@gf3](https://twitter.com/gf3) [@jon_neal](https://twitter.com/jon_neal) [@sambreed](https://twitter.com/sambreed) and [@iansym](https://twitter.com/iansym).

It has since received contributions from over [100 developers](https://github.com/h5bp/Front-end-Developer-Interview-Questions/graphs/contributors).
