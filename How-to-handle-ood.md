## Purpose
Interviews ask OOD problems to gain insights in interviewees coding style and thought process in problem solving. **Key point is not to design perfect design patterns**
## How to Approach OOD problems:
**1. Handle ambiguity**
- Problems are often asked intentionally vague for you to ask for clarification
- Inquire who and how are they going to use it. six W's: who, what, where, when, how, why.

**Example - coffee maker**: for industrial machine at starbucks for 100s of customers vs. home machine for <3 people

**2. Define core objects**\
\
**Restaurant Example**: core objects ight be Table, Guest, Party, Order, Meal, Employee, Server, Host


**3. Analyze relationship**
- What objects are members of which other objects? 
- Do any objects inherit from any other relationships? 
- Are relationships many to many or one to many?

**Table example continued:**
- Party should have an array of guests
- Server and Host inherit from Employee
- Each Table has one Party, but each party may have multiple Tables
- There is one Host for the Resturant

**4. Investigate Actions**\
Consider the key action the objects take and how they relate to each other. Might need to update design.\
\
**Table example continued:**
- *Guest* requests a *Table* from the *Host*
- *Host* look up *Reservation*, if exists, assigns *Party* to *Table*, otherwise add to end of list.
- When a *Party* leaves, *Table* is freed and assigned to a new *Party* in the list