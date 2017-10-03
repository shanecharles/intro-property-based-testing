- title : Intro to Property Based Testing
- description : An introduction to property based testing.
- author : Shane Charles
- theme : night
- transition : default

***

### Intro to Property Based Testing

![F#](images/fsharp256.png)

***

### About me

- Shane Charles
- Consultant with White Light Computing, Inc.
- Functional programming enthusiast
- Board member for Winnipeg .Net UG


    type ContactType = | Email | Twitter | Blog | GitHub

    let getContactInfo = function
      | Twitter -> "@dead_stroke"
      | Blog    -> "http://geekeh.com"
      | GitHub  -> "shanecharles"
      | Email   -> "shane_charles@outlook.com"

***

### Roadmap

- What
- Why
- How

***

### What is property based testing?

> The thing that QuickCheck does.<br/>
>
> ~ almost everybody

---

### Not Quite

    [lang=C#]
    public class SomeClass 
    {
        public string PropertyToTest { get; set; }
    }

---

### Merriam-Webster Definition of Property

- a quality or trait belonging and especially peculiar to an individual or thing
- an attribute common to all members of a class 

---

### Property Based Testing

A trait belonging to a process with results common to all members of a set of inputs.

---

### Example

Any positive number multiplied by negative one will have a result less than zero.

- Process: `(*) -1`
- Input Set: `Choose [1 .. ]`
- Result: `< 0`

***

### We Already Have TDD

- unit tests
- integration tests

---
### Test, Fail, Fix

![fail](images/wile-coyote-fail1.gif)

---

### Test, Fail, Fix

![fail](images/wile-coyote-fail2.gif)

---

### The Power of TDD

- Build code one failure at a time
- Growth with stability
- Regression checks

---

### TDD has Limits

- Testing through specific examples
 - How many is enough?
- Active becomes passive testing
- Legacy code with no tests
- Race conditions?

***


### Where to start

- Get a chunk of code or a library you commonly use
 - Don't start with nothing (this isn't TDD)

---

### Make Some Assumptions

What do you think is true about the code or service?

---

##### Use Testing Library

![libs](images/testing-libraries.png)

[http://hypothesis.works/articles/quickcheck-in-every-language/](http://hypothesis.works/articles/quickcheck-in-every-language/)

---

### Generate inputs

![haskell](images/haskell.png)

---

### Question Everything

- Is it an actual failure or a problem with property?

> Properties can require a lot of thought and can be difficult to come up with.

***

### Patterns for Properties

- Starting point for creating properties

---

### There and Back

- Serialization and deserialization
- Encryption and decryption
- Set value and get value
- Write and read

---

### Different Paths Same Destination

- a + b = b + a
- a + a = a * 2
- F() |> G() = G() |> F()

---

### Some Things Never Change

- Size of collection
- elements of a collection after a sort

---

### Hard to Prove Easy to Verify

- String tokenizer
 - Verify by concatenating the tokens
- Sorting

---

### Test Oracle

- Compare your results to a different 'proven' solution
  - Performance optimizations
- Model your state as linerizable steps
  - Concurrency, race conditions, deadlocks

---

### Should not crash

- Generate http requests
 - Get, Post, etc.
 - Accepted HttpStatuses

***

### Summary

- Coming up with Properties can be difficult
- Forces us to better understand the domain
- Not meant for building
- The more complex the problem the better

---

### Use Both

#### Unit Test

![tdd](images/wile-coyote-fail.gif)

#### Property Based Test

![property-based-testing](images/naruto-property-based.gif)

***

### Extra Resources

- F# for Fun and Profit 
 - https://fsharpforfunandprofit.com/posts/property-based-testing/
- Testing the Hard Stuff and Staying Sane by John Hughes
 - https://www.youtube.com/watch?v=zi0rHwfiX1Q
- Winnipeg .Net Slack (http://winnipegdotnet.org)


    type ContactType = | Email | Twitter | Blog | GitHub

    let getContactInfo = function
      | Twitter -> "@dead_stroke"
      | Blog    -> "http://geekeh.com"
      | GitHub  -> "shanecharles"
      | Email   -> "shane_charles@outlook.com"

***
