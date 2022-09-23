# Assignment For Front-end Developer

## Explain what the simple List component does.

Here, in this code, List component is rendering an _ul_ tag, and a prop named “items” is passed in List, which is an array of strings. Inside List, a state variable is created called as “selectedIndex”, which is used to store the index of the element in the array, which is clicked by the user. One function is defined, named as “handleClick”, which stores the index of clicked element in selectedIndex.

Inside return function of List, .map() function is called on items, which returns a “singleListItem” component. selectedIndex is passed in this singleListItem component, and depending upon its value, different stylings gets applied on singleListItem. 

So, in layman terms, List component renders a list of items that are defined in the “items” array, and when user clicks on any of that list item, it’s styling changes, which implies that the particular list item has been selected by the user. Since, memo is used to create List component, it is a pure component, and it only 
re-renders when its props or its state values changes, which leads to better performance of the app.

## What problems / warnings are there with code?

I have identified three problems in this code. 

* In SingleListItem component, in __li__ tag, on onClick event listener, onClickHandler function is passed as a reference, rather than as a arrow function, due to which application goes into a lifinite loop. When we have to pass a function inside onClick, we should pass that function inside an arrow function, so that it will get called only when that event will occur.

* In List component, In defining state using useState, the variables in useState array is reversed, which is leading to error in the code. In useState array, first element is the state variable and second element is a asynchronous function which changes the value of state variable. Since the variables are reversed, it is not syntactically incorrect, but it is logically correct.

* In defining the prop types for List component, .shape function is mistyped as .shapeOf, which is giving the error that .shapeOf is not an function. 
   
## Please fix, optimize, and/or modify the component as much as you think is necessary.


