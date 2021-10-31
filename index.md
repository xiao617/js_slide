---

theme : "night"
transition: "slide"
highlightTheme: "monokai"
# logoImg: "logo.png"
slideNumber: true
title: "React overview"

---

### JS & TS fundamental


<style>
pre {
  background: #303030;
  padding: 10px 16px;
  border-radius: 0.3em;
  counter-reset: line;
}
pre code[class*="="] .line {
  display: block;
  line-height: 1.8rem;
  font-size: 1em;
}
pre code[class*="="] .line:before {
  counter-increment: line;
  content: counter(line);
  display: inline-block;
  border-right: 3px solid #6ce26c !important;
  padding: 0 .5em;
  margin-right: .5em;
  color: #afafaf !important;
  width: 24px;
  text-align: right;
}

.reveal .slides > section > section {
  text-align:left; 
}

h1,h2,h3,h4 {
  text-align: center
}

p {
  text-align: center;
}
</style>

---

### == vs ===

--

#### Abstract Equality Comparison(==)
```javascript=
const num = 0;
const str = '0';

console.log(num == str)
//output: true
```

--

#### Strict Equality Comparsion(===)

```javascript=
const num = 0;
const str = '0';

console.log(num === str)
//output: false
```
**check type!**

--

### [Ref](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Equality_comparisons_and_sameness)

---

### Primitives

--

#### String primitive and String object

```
let s_prim = 'foo';
let s_obj = new String('foo');

console.log(typeof s_prim)
// "string"
console.log(typeof s_obj)
// "object"
```
The same in **Boolean** and **Number**

--

### [Ref](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)

---

### Variable
#### var, let & const

--

### var

- Global scope or local scope
- Can re-declared and updated

--

### let

- Block scope
- Can be update but not re-declared
- Hoisting will into TDZ(Temporal Death Zone)

--

### const

- Block scope
- Cannot be updated or re-declared
- Hoisting will into TDZ(Temporal Death Zone)

--

### [About hoisting](https://blog.techbridge.cc/2018/11/10/javascript-hoisting/)

---

### Array render

--

#### forEach
```javascript=
forEach(() => {...})
forEach((value) => {...})
forEach((value,key) => {...})
forEach((value,key,array) => {...})
```

--

#### forEach
```javascript=
const arrayExample = ['a','b','c','d']

//forEach((value) => {...})
arrayExample.forEach((e)=>{
    console.log(e);
})
//output: 'a'
//output: 'b'
//output: 'c'
//output: 'd'
```

--

#### map
```javascript=
map(() => {...})
map((element) => {...})
map((element,key) => {...})
map((element,key,array) => {...})
```

--

#### map
```javascript=
const arrayExample = ['a','b','c','d']

//map((value) => {...})
const arrayMap = arrayExample.map((x)=>(`Get: ${x}`));
console.log(arrayMap)
//output: [ 'Get: a', 'Get: b', 'Get: c', 'Get: d' ]
```

---

### Arrow function & Function

--

### Function
```javascript=
function(arg1,arg2,...,argN)
{
  return expression;
}
```

--

### Arrow function
```javascript=
const testArrow = () => {
  return expression;
};

const testArrow2 = () => (expression);
```

--

### [Ref](https://javascript.info/arrow-functions-basics)

---

### Promise

--

![](./media/promise.png =400x)

--

#### Promise Example
```javascript=
promiseExampleFunction
.then(resolveExpression)
.catch(rejectExpression)
```

--

### [Ref](https://javascript.info/promise-basics)

---

## Async & sync

--

### Async & sync
![](./media/async_sync.jpeg =400x)

--

### [Ref](https://medium.com/itsems-frontend/javascript-sync-async-22e75e1ca1dc)

---

#### Type Aliases and Interfaces

--

#### Extending an interface
```javascript=
interface Animal {
    name: string
}

interface Bear extends Animal {
    honey: boolean
}

const bear = getBear();
bear.name;
bear.honey;
```

--

#### Adding new fields to an existing interface
```javascript=
interface Window {
    title: string
}

interface Window {
    status: string
}
```

--

#### Extending a type via intersections
```javascript=
type Animal = {
    name: string
}

type Bear = Animal & {
    honey: boolean
}

const bear = getBear();
bear.name;
bear.honey;
```

--

#### A type cannot be changed after being created
```javascript=
type Window = {
    title: string
}

type Window = {
    status: string
}

//Error: Duplicate identifier 'Window'
```

--

### [Ref](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html)

---

### JavaScript follow-up

--

### [Spread syntax(...)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_syntax)

--

### [Try Catch](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/try...catch)

--

### [Method definitions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Method_definitions)

--

### [Data Type](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures)

---

### TypeScript follow-up

--

### [Types](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html)

--

### [Utility Types](https://www.typescriptlang.org/docs/handbook/utility-types.html)

--

### [Enums](https://www.typescriptlang.org/docs/handbook/enums.html)

--

