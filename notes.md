what is it
	- no one definition
	- first class functions
	- some things that are generally part of it

what most people mean (give or take)
	- math functions have no side effects, same input, same output, do not change state, referentially transparent, "honest"
	- immutability plays into this, things don't change. need to change something? new object
	- side effects are avoided, but are made explicit (CQS)
	- type system encodes application rules (applies less to C#)
	- can be tough on memory, but good compliers and data structures can fix this, C# has some nice things
	- things you don't need to worry about: monads, monoids, functors, endofunctors, etc
	- popular in academic circles years ago, react, redux, c# are gateway drugs


why do you care?
	- makes code more explicit, declarative, and readable
	- tests are actually fun
	- a strong type system makes code more safe, less bugs, some states are impossible to get into
	- elm has no errors in production
	- haskell won't compile if it's unsafe
	- thread safety increasingly important
	- might be less readable if you aren't used to it, makes things more verbose generally

example
	- Problems
		- conflates deciding what to do with actually doing it
		- Explicityly applying state
		- hiding information about how things happen, need to actually view code to understand what is happening inside.
		- writing tests for this won't be fun, even if we use dependency injection
	- Fixing it
		- removing all explicit calls to the file system
		- create some data structures to represent our data and what we want to do with it
		- class that does mutation and simple shell to coordinate work
		- looks familiar, no?
		- tests will be easy for the immutable parts, the other parts need few if any tests
	- this was just a quick sample, there is a lot more to dig into, getting rid of exceptions, avoiding primitives, map, reduce, filter, currying, things other languages do that are harder to express in C# or JS
