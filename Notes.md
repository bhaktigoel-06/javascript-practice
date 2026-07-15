### Monday task learnings

-- let vs const

**let:**
It is a block-scoped variable.  
By this, variables can be updated but cannot be redeclared.

**const:**
It is also a block-scoped variable.  
By this, variables can neither be updated nor redeclared.


### Tuesday task learnings

-- map,filter,reduce

**map:** 
Takes an array and returns a new array by applying a function to every element.

**filter:** 
Takes an array and returns a new array with only the elements that pass a condition.

**reduce:** 
Takes an array and combines all its elements into a single value using a function.

### Wednesday task learnings

**closures:**

Closure is when a function remembers variables from its lexical scope even after the outer function has finished execution.

**example from code **

export function once(fn) {

  let hasRun = false;

  let result;

  return function(...args) {

    if (!hasRun) {

      result = fn(...args);

      hasRun = true;

    }

    return result;

  };
  
}


--here, hasRun is defined outside function() but is still used even after the function(where it has defined) ended
