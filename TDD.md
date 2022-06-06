# I'm trying to get better at TDD

## Why
- I've heard a lot about how it's ~~good~~ best practice, saves time, prevents bugs, leads to better code, etc., but it's always felt impossible.
- I've never enjoyed or felt great writing tests after writing the code.
- We need to improve test coverage in our products and we will be writing a lot of new code.
- Maybe the barrier isn't coming from the concept.


## How 
I started reading a book:
*Mastering React Test-Driven Development:
Build rock-solid, well-tested web apps with React, Redux, and GraphQL* 
by Daniel Irvine


#### Red -> Green Development
1. Write simplest failing test (Red)
2. Write simplest code to make the test pass (Green)
3. Refactor (feature code & tests)
4. Repeat by writing tests to make the feature code more accurate


#### Guiding Principles
- Only refactor on green.
- **Always** refactor on green.
- Small tests document a feature.
- Write simplest code possible to make a test pass. It doesn't need to be correct.
- Write more tests to shape the code into what is correct.
- Tests are treated with the same care and respect as the feature code.
- The best time to refactor is immediately after writing the code.
- Experiment/explore before writing tests, then write a test that will only pass once the experiment/exploration is cleaned up.


### Example:
Data:
```typescript
{
	household: {
		doNotContact: boolean
		parent: {
			hasValidEmail: boolean
	}
}
```


Requirements:
- Display `<NoValidEmailIcon />` if `household.parent.hasValidEmail` is `false`
- Display `<OptedOutIcon />` if `houseold.doNotContact` is `true`
- Only display `<OptedOutIcon />` if both icons could be displayed. 

Tests:
	✓ does not render icons for full communication household and parent
	✓ renders NoValidEmailIcon if parent does not have valid email
	✓ renders OptedOutIcon when household is set to "doNotContact"
	✓ does not render NoValidEmailIcon when household is set to "doNotContact"

#### Show Quick Sample

#### What I've Experienced
- Supercharge refactor cycles.
- Passing tests can be refactored.
- Prove that tests can fail.
- Benefits are felt exponentially relative to the amount of code written.
- The first pass at feature code can be sloppy.
- Focus on test data makes for good demo display.
- It's actually more fun.


#### So far, it feels like
- 1 hour of feature code in 2 hours (includes test coverage)
- tests are free
- 1.5 hours of refactoring in 30 minutes
- 3x confidence writing and changing code, and grows relational to amount of code


#### Caveats
- I've only worked like this on two non-interactable views (Recipients Modal Parents and Campers List)
	- This turned out to be a good thing because I could practice this way of working with a lower barrier to entry.
- I need to learn more about how to write tests that are style focussed.
- In a couple cases, I wrote some feature code first so there was something that I could figure out how to write tests against. This gave me an opportunity to write a negative test.
- I've had really great requirements that have not changed.


