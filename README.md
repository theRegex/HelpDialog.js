# HelpDialog.js
A simple help solution for showing user how to navigate and interact with with your web application .

HelpDialog.js uses native javascript functionality , logic and calculation to run , this plugin requires no external libraries such as 
jQuery to function . 

## Browser support
HelpDialog.js works browsers IE 10+ , Chrome , Firefox , and Safari


## Getting started
HelpDialog includes one javascript and css file , these both must be included in head . 



## API in examples

Create a button and give it an id of `helper` :

```html

<button id="helper"></button>


```

Create an instance of HelpDialog :

```javascript

var helper = new HelpDialog;


```


HelpDialog relies on an array of objects to be passed at initialization , each object must contain a key of id , header , and text.

The `id` will represent the id of your element without the hash.
The `header` will represent the title of the help component.
The `text` will represent the body/description of the help component.

```javascript

var data = [

{id : "elementID" , header: "Header Content" , text : "This content will go in the body"}

]; ect...


helper.init(data);

```

## destroy() 

To stop HelpDialog programatically , just call destroy on your instance :

```javascript

helper.destroy();

```
All data will still be in sessionStorage via `helpcontents` and clicking help button will re-spawn this data and refresh the object .

## FYI

HelpDialog.js also relies on localStorage to restrict dialog from auto starting.
 
The auto start data object is stored in `insession` variable and can be cleared using logic below :

```javascript

localStorage.removeItem('insession');

```


## Credits

Software designed by [Keinan Pace] https://github.com/theRegex

Thanks for all of your support!
