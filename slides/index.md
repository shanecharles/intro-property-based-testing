- title : Intro to Property Based Testing
- description : An introduction to property based testing.
- author : Shane Charles
- theme : night
- transition : default

***

### Intro to Property Based Testing

![F#](images/fsharp256.png)

***

### Thank the Sponsors

![Sponsors](images/sponsors.png)

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
      | Email   -> "shanecharles@burningicesolutions.com"

***

### We've got TDD

---

### TDD is Good

- Build code one test at a time
- Growth with stability

---

### TDD has Limits

- Testing through example
- All tests have exactly expected results 
- Limited to the imagination of the developer

***

### What is property based testing?

> The thing that QucikCheck does.

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

### Reworked Definition

A trait belonging to a function or process with results common to all members of a group of inputs.

***

### Extra Resources

- F# for Fun and Profit (https://fsharpforfunandprofit.com)
- Testing the Hard Stuff and Staying Sane (https://www.youtube.com/watch?v=zi0rHwfiX1Q)
- Winnipeg .Net Slack (http://winnipegdotnet.org)


    type ContactType = | Email | Twitter | Blog | GitHub

    let getContactInfo = function
      | Twitter -> "@dead_stroke"
      | Blog    -> "http://geekeh.com"
      | GitHub  -> "shanecharles"
      | Email   -> "shanecharles@burningicesolutions.com"

***