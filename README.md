## Challenges

### Chapter 4: Scanning

1. The lexical grammars of Python and Haskell are not _regular_. What does that mean, and why aren't they?
   * They aren't regular because some lexical elements can lead to more than one derivation. This introduces non-regular
   ambiguity to the language.
2. Aside from separating tokens- distinguishing `print foo` from `printfoo`- spaces aren't used for much in most
languages. However, in a couple of dark corners, a space _does_ affect how code is parsed in CoffeeScript, Ruby, and the
C preprocessor. Where and what effect does it have in each of those languages?
   * In each of the example languages, the edge case that leads to significant whitespace considerations
   revolve around function definitions and invocations. It leads to weird behavior.
3. Our scanner here, like most, discards comments and whitespace since those aren't needed by the parser. Why might you 
want to write a scanner that does _not_ discard those? What would it be useful for?
   * Retaining comments would be good for writing tangle-style literate compilers.
4. Add support to Lox's scanner for C-style `/* ... */` block comments. Make sure to handle newlines in them. Consider
allowing them to nest. Is adding support for nesting more work than you expected? Why?
   * Added as Issue #1.