# Javascript-Modules

## What I learned:

Javascript modules are reusable peices of code that can be exported from one program, and imported fro use in another program. Modules are particularly useful because they help to:

* find, fix, and debug code more easily.
* reuse and recycle defined logic in different parts of our application
* keep information private and protected from other modules.
* prevent pollution of the global namespace, and potential naming collisions by cautiously selecting variables and behavior we load into a program.

### Defining and Exporting Modules

The syntax for defining and exporting modules looks like this:

```
let Dinner = {};

Dinner.firstCourse = "Pizza";

module.exports = Dinner;
```

The pattern we use to export modules is thus:

1.  Define an object to represent the module
2.  Add data or behavior to the module
3.  Export the Module

We can also wrap any collection of data and functions in an object, and export the object using **module.exports**. Example syntax would look like this:

```
let Dinner = {};

module.exports = {
 firstCourse: = "Pizza";
 happyCamper:  function(){
 console.log('I am so excited that I am about to eat ' + this.firstCourse);
 }
};
```

#### Explort Defualt

### Importing the Module with **require()**

To make use of the module and the behavior we define in it, we **import** the module. A common way to do this is with the **require()** function.

Modules can be separated into individual documents, based on their specific feature, function, or goal, and then imported and exported back and forth, based on how you need to use them or combine them to make the program work.

require() syntax:

```
const Dinner = require('./dinner.js');
function happyCamper(){
 console.log('I am so excited that I am about to eat ' + Menu.firstCourse);
}
happyCamper();
```

The pattern we use to import modules is thus:

1.  Import the module using the **require()** function
2.  Us the module and it's properties within a program
