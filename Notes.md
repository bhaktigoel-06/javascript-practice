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

```js
export function once(fn) {
  let hasRun = false;
  let result;

  return function (...args) {
    if (!hasRun) {
      result = fn(...args);
      hasRun = true;
    }
    return result;
  };
}
```


--here, hasRun is defined outside function() but is still used even after the function(where it has defined) ended

### Thursday task learnings

**Immutable Update:**

it means modifying an original array or object by making a copy of it

--why not simply change the original array??

-to avoid bugs

-to predict code

-useful in framework

**difference between value ?? fallback and value || fallback**

--|| (Logical OR)

Returns fallback if the value is falsy(false, 0, "", null, undefined, NaN)

--?? (Nullish Coalescing)

Returns fallback only if value is null or undefined

--Importance:

--||

when one have to replace all falsy values

--??

when one have to handle NULL and undefined values

**Await**

await pauses the execution of an async function until a Promise is resolved (or rejected).

--doing three things one after another(sequential)

Total time = a + b + c (slow)

--doing all three things at once(parallel)

Total time = max(a,b,c)(fast)