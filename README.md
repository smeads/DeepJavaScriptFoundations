# DeepJavaScriptFoundations

Notes on Kyle Simpson's course Deep JavaScript Foundations on Frontend Masters

### Scope & Closures

**Scope:** Set of rules for storing variables in some location and for finding those variables at a later time. Where to look for things.

- JavaScript is a compiled language. It's a common misconseption that it's an interpreted language.
- A good question to ask when thinking about scope is, _Who is doing the looking?_
- Scope is a compiled time process. It's at compile time that all scope decisions are made.
- JavaScript makes two passes before actually executing.
- On the first pass, compilation, the lexical scope is set up.
- First pass when compiling look for all variable declarations and all the scopes they get added to.
- The compiler and scope manager have a conversations.
- The individual unit of scope is the function.
- As the JavaScript compiler enters a function, it will begin looking for declaration(s) inside that scope and recursively process them.
  - Once all scopes have been compiled, the execution phase can begin.
- As the execution phase continues within the function scope, the same Left-Hand Side (LHS) and Right-Hand Side (RHS) operations are applied.
  - Things get a little interesting with undeclared variables. They are automatically declared in the global scope.
  - LHS is the target of an assignment.
  - RHS is the source of an assignment.

**Scope Manager && Compiler Dialogue**

```javascript
var foo = "bar";

function bar() {
  var foo = "baz";
}

function baz(foo) {
  foo = "bam";
  baz = "yay";
}
```
