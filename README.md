# Code and notes from book Architecture Patterns with Python

## Chapter 1
The term `encapsulation` covers two closely ideas: simplifying behavior and hiding data. We encapsulate behavior by identifying a task that needs to be done in our code and giving that task to a well-defined object or function. We call that object or function an `abstraction`.

### Layering
Layered architecture is perhaps the most common pattern for building business software. In this model we have user-interface components, which could be a web page, an API, or a command line; these user-interface components communicate with a business logic layer that contains our business rules and our workflows; and finally, we have a database layer that’s responsible for storing and retrieving data.

### The Dependecy Inversion Principle
DIP’s formal definition: 

- High-level modules should not depend on low-level modules. Both should depend on abstractions.  
- Abstractions should not depend on details. Instead, details should depend on abstractions.

High-level modules are the code that your organization really cares about. Perhaps you work for a pharmaceutical company, and your high-level modules deal with patients and trials. Perhaps you work for a bank, and your high-level modules manage trades and exchanges. The high-level modules of a software system are the functions, classes, and packages that deal with our real-world concepts. By contrast, low-level modules are the code that your organization doesn’t care about. It’s unlikely that your HR department gets excited about filesystems or network sockets. It’s not often that you discuss SMTP, HTTP, or AMQP with your finance team. For our nontechnical stakeholders, these low-level concepts aren’t interesting or relevant.

`So the first part of the DIP says that our business code shouldn’t depend on technical details; instead, both should use abstractions.`

### The Domain Model
One of the most common reasons that our designs go wrong is that business logic becomes spread throughout the layers of our application, making it hard to identify, understand, and change.

Behavior should come first and drive our storage requirements. After all, our customers don’t care about the data model. They care about what the system does; otherwise they’d just use a spreadsheet.

