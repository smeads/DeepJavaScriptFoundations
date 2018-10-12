# DeepJavaScriptFoundations

Notes on Kyle Simpson's course Deep JavaScript Foundations on Frontend Masters

### Scope & Closures

**Scope:** Set of rules for storing variables in some location and for finding those variables at a later time. Where to look for things.

- JavaScript is a compiled language. It's a common misconseption that it's an interpreted language.
- A good question to ask when thinking about scope is, _Who is doing the looking?_
- Scope is a compiled time process. It's at compile time that all scope decisions are made.
- JavaScript makes two passes before actually executing.
  ..._ On the first pass, compilation, the lexical scope is set up.
  ..._ First pass when compiling look for all variable declarations and all the scopes they get added to.
  ...\_ The compiler and scope manager have a conversations.
- The individual unit of scope is the function.
