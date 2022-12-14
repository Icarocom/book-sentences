
![Cover](./assets/clean-architecture.png)

# Clean Architecture. A Craftsman's Guide to Software Structure and Design

Robert C. Martin - 2017

## Table of Contents

- [Foreword](#foreword)
- [Preface](#preface)
- [PART I Introduction](#part-i-introduction)
- [Chapter 1 What Is Design and Architecture?](#chapter-1-what-is-design-and-architecture)
  - [The Goal?](#the-goal)
  - [Case Study](#case-study)
  - [Conclusion](#conclusion)
- [Chapter 2 A Tale of Two Values](#chapter-2-a-tale-of-two-values)
  - [Behavior](#behavior)
  - [Architecture](#architecture)
  - [The Greater Value](#the-greater-value)
  - [Eisenhower’s Matrix](#eisenhowers-matrix)
  - [Fight for the Architecture](#fight-for-the-architecture)
- [PART II Starting with the Bricks: Programming Paradigms](#part-ii-starting-with-the-bricks-programming-paradigms)
- [Chapter 3 Paradigm Overview](#chapter-3-paradigm-overview)
  - [Structured Programming](#structured-programming)
  - [Object-Oriented Programming](#object-oriented-programming)
  - [Functional Programming](#functional-programming)
  - [Food for Thought](#food-for-thought)
  - [Conclusion](#conclusion-1)
- [Chapter 4 Structured Programming](#chapter-4-structured-programming)
  - [Proof](#proof)
  - [A Harmful Proclamation](#a-harmful-proclamation)
  - [Functional Decomposition](#functional-decomposition)
  - [No Formal Proofs](#no-formal-proofs)
  - [Science to the Rescue](#science-to-the-rescue)
  - [Tests](#tests)
  - [Conclusion](#conclusion-2)
- [Chapter 5 Object-Oriented Programming](#chapter-5-object-oriented-programming)
  - [Encapsulation?](#encapsulation)
  - [Inheritance?](#inheritance)
  - [Polymorphism?](#polymorphism)
    - [The Power of Polymorphism](#the-power-of-polymorphism)
    - [Dependency Inversion](#dependency-inversion)
  - [Conclusion](#conclusion-3)
- [Chapter 6 Functional Programming](#chapter-6-functional-programming)
  - [Squares of Integers](#squares-of-integers)
  - [Immutability and Architecture](#immutability-and-architecture)
  - [Segregation of Mutability](#segregation-of-mutability)
  - [Event Sourcing](#event-sourcing)
  - [Conclusion](#conclusion-4)
- [PART III Design Principles](#part-iii-design-principles)
- [Chapter 7 SRP: The Single Responsibility Principle](#chapter-7-srp-the-single-responsibility-principle)
  - [Symptom 1: Accidental Duplication](#symptom-1-accidental-duplication)
  - [Symptom 2: Merges](#symptom-2-merges)
  - [Solutions](#solutions)
  - [Conclusion](#conclusion-5)
- [Chapter 8 OCP: The Open-Closed Principle](#chapter-8-ocp-the-open-closed-principle)
- [A Thought Experiment](#a-thought-experiment)
  - [Directional Control](#directional-control)
  - [Information Hiding](#information-hiding)
  - [Conclusion](#conclusion-6)
- [Chapter 9 LSP: The Liskov Substitution Principle](#chapter-9-lsp-the-liskov-substitution-principle)
  - [Guiding the Use of Inheritance](#guiding-the-use-of-inheritance)
  - [The Square/Rectangle Problem](#the-squarerectangle-problem)
  - [LSP and Architecture](#lsp-and-architecture)
  - [Example LSP Violation](#example-lsp-violation)
  - [Conclusion](#conclusion-7)
- [Chapter 10 ISP: The Interface Segregation Principle](#chapter-10-isp-the-interface-segregation-principle)
  - [ISP and Language](#isp-and-language)
  - [ISP and Architecture](#isp-and-architecture)
  - [Conclusion](#conclusion-8)
- [Chapter 11 DIP: The Dependency Inversion Principle](#chapter-11-dip-the-dependency-inversion-principle)
  - [Stable Abstractions](#stable-abstractions)
  - [Factories](#factories)
  - [Concrete Components](#concrete-components)
  - [Conclusion](#conclusion-9)
- [PART IV Component Principles](#part-iv-component-principles)
- [Chapter 12 Components](#chapter-12-components)
  - [A Brief History of Components](#a-brief-history-of-components)
  - [Relocatability](#relocatability)
  - [Linkers](#linkers)
  - [Conclusion](#conclusion-10)
- [Chapter 13 Component Cohesion](#chapter-13-component-cohesion)
  - [The Reuse/Release Equivalence Principle](#the-reuserelease-equivalence-principle)
  - [The Common Closure Principle](#the-common-closure-principle)
    - [Similarity with SRP](#similarity-with-srp)
  - [The Common Reuse Principle](#the-common-reuse-principle)
    - [Relation to ISP](#relation-to-isp)
  - [The Tension Diagram for Component Cohesion](#the-tension-diagram-for-component-cohesion)
  - [Conclusion](#conclusion-11)
- [Chapter 14 Component Coupling](#chapter-14-component-coupling)
  - [The Acyclic Dependencies Principle](#the-acyclic-dependencies-principle)
    - [The Weekly Build](#the-weekly-build)
    - [Eliminating Dependency Cycles](#eliminating-dependency-cycles)
    - [The Effect of a Cycle in the Component Dependency Graph](#the-effect-of-a-cycle-in-the-component-dependency-graph)
    - [Breaking the Cycle](#breaking-the-cycle)
    - [The "Jitters"](#the-jitters)
  - [Top-Down Design](#top-down-design)
  - [The Stable Dependencies Principle](#the-stable-dependencies-principle)
    - [Stability](#stability)
    - [Stability Metrics](#stability-metrics)
    - [Not All Components Should Be Stable](#not-all-components-should-be-stable)
    - [Abstract Components](#abstract-components)
  - [The Stable Abstractions Principle](#the-stable-abstractions-principle)
    - [Where Do We Put the High-Level Policy?](#where-do-we-put-the-high-level-policy)
    - [Introducing the Stable Abstractions Principle](#introducing-the-stable-abstractions-principle)
    - [Measuring Abstraction](#measuring-abstraction)
    - [The Main Sequence](#the-main-sequence)
    - [The Zone of Pain](#the-zone-of-pain)
    - [The Zone of Uselessness](#the-zone-of-uselessness)
    - [Avoiding the Zones of Exclusion](#avoiding-the-zones-of-exclusion)
    - [Distance from the Main Sequence](#distance-from-the-main-sequence)
  - [Conclusion](#conclusion-12)
- [PART V Architecture](#part-v-architecture)
- [Chapter 15 What Is Architecture?](#chapter-15-what-is-architecture)
  - [Development](#development)
  - [Deployment](#deployment)
  - [Operation](#operation)
  - [Maintenance](#maintenance)
  - [Keeping Options Open](#keeping-options-open)
  - [Device Independence](#device-independence)
  - [Junk Mail](#junk-mail)
  - [Physical Addressing](#physical-addressing)
  - [Conclusion](#conclusion-13)
- [Chapter 16 Independence](#chapter-16-independence)
  - [Use Cases](#use-cases)
  - [Operation](#operation-1)
  - [Development](#development-1)
  - [Deployment](#deployment-1)
  - [Leaving Options Open](#leaving-options-open)
  - [Decoupling Layers](#decoupling-layers)
  - [Decoupling Use Cases](#decoupling-use-cases)
  - [Decoupling Mode](#decoupling-mode)
  - [Independent Develop-ability](#independent-develop-ability)
  - [Independent Deployability](#independent-deployability)
  - [Duplication](#duplication)
  - [Decoupling Modes (Again)](#decoupling-modes-again)
  - [Conclusion](#conclusion-14)
- [Chapter 17 Boundaries: Drawing Lines](#chapter-17-boundaries-drawing-lines)
  - [A Couple of Sad Stories](#a-couple-of-sad-stories)
  - [FitNesse](#fitnesse)
  - [Which Lines Do You Draw, and When Do You Draw Them?](#which-lines-do-you-draw-and-when-do-you-draw-them)
  - [What About Input and Output?](#what-about-input-and-output)
  - [Plugin Architecture](#plugin-architecture)
  - [The Plugin Argument](#the-plugin-argument)
  - [Conclusion](#conclusion-15)
- [Chapter 18 Boundary Anatomy](#chapter-18-boundary-anatomy)
  - [Boundary Crossing](#boundary-crossing)
  - [The Dreaded Monolith](#the-dreaded-monolith)
  - [Deployment Components](#deployment-components)
  - [Threads](#threads)
  - [Local Processes](#local-processes)
  - [Services](#services)
  - [Conclusion](#conclusion-16)
- [Chapter 19 Policy and Level](#chapter-19-policy-and-level)
  - [Level](#level)
  - [Conclusion](#conclusion-17)
- [Chapter 20 Business Rules](#chapter-20-business-rules)
  - [Entities](#entities)
  - [Use Cases](#use-cases-1)
  - [Request and Response Models](#request-and-response-models)
  - [Conclusion](#conclusion-18)
- [Chapter 21 Screaming Architecture](#chapter-21-screaming-architecture)
  - [The Theme of an Architecture](#the-theme-of-an-architecture)
  - [The Purpose of an Architecture](#the-purpose-of-an-architecture)
  - [But What About the Web?](#but-what-about-the-web)
  - [Frameworks Are Tools, Not Ways of Life](#frameworks-are-tools-not-ways-of-life)
  - [Testable Architectures](#testable-architectures)
  - [Conclusion](#conclusion-19)
- [Chapter 22 The Clean Architecture](#chapter-22-the-clean-architecture)
  - [The Dependency Rule](#the-dependency-rule)
    - [Entities](#entities-1)
    - [Use Cases](#use-cases-2)
    - [Interface Adapters](#interface-adapters)
    - [Frameworks and Drivers](#frameworks-and-drivers)
    - [Only Four Circles?](#only-four-circles)
    - [Crossing Boundaries](#crossing-boundaries)
  - [A Typical Scenario](#a-typical-scenario)
  - [Conclusion](#conclusion-20)
- [Chapter 23 Presenters and Humble Objects](#chapter-23-presenters-and-humble-objects)
  - [The Humble Object Pattern](#the-humble-object-pattern)
  - [Presenters and Views](#presenters-and-views)
  - [Testing and Architecture](#testing-and-architecture)
  - [Database Gateways](#database-gateways)
  - [Data Mappers](#data-mappers)
  - [Service Listeners](#service-listeners)
  - [Conclusion](#conclusion-21)
- [Chapter 24 Partial Boundaries](#chapter-24-partial-boundaries)
  - [Skip the Last Step](#skip-the-last-step)
  - [One-Dimensional Boundaries](#one-dimensional-boundaries)
  - [Facades](#facades)
  - [Conclusion](#conclusion-22)
- [Chapter 25 Layers and Boundaries](#chapter-25-layers-and-boundaries)
  - [Hunt the Wumpus](#hunt-the-wumpus)
  - [Clean Architecture?](#clean-architecture)
  - [Crossing the Streams](#crossing-the-streams)
  - [Splitting the Streams](#splitting-the-streams)
  - [Conclusion](#conclusion-23)
- [Chapter 26 The Main Component](#chapter-26-the-main-component)
  - [The Ultimate Detail](#the-ultimate-detail)
  - [Conclusion](#conclusion-24)
- [Chapter 27 Services: Great and Small](#chapter-27-services-great-and-small)
  - [Service Architecture?](#service-architecture)
  - [Service Benefits?](#service-benefits)
  - [The Kitty Problem](#the-kitty-problem)
  - [Objects to the Rescue](#objects-to-the-rescue)
  - [Component-Based Services](#component-based-services)
  - [Cross-Cutting Concerns](#cross-cutting-concerns)
  - [Conclusion](#conclusion-25)
- [Chapter 28 The Test Boundary](#chapter-28-the-test-boundary)
  - [Tests as System Components](#tests-as-system-components)
  - [Design for Testability](#design-for-testability)
  - [The Testing API](#the-testing-api)
    - [Structural Coupling](#structural-coupling)
  - [Conclusion](#conclusion-26)
- [Chapter 29 Clean Embedded Architecture](#chapter-29-clean-embedded-architecture)
- [App-titude Test](#app-titude-test)
  - [The Target-Hardware Bottleneck](#the-target-hardware-bottleneck)
    - [A Clean Embedded Architecture Is a Testable Embedded Architecture](#a-clean-embedded-architecture-is-a-testable-embedded-architecture)
      - [Layers](#layers)
    - [Don’t Reveal Hardware Details to the User of the HAL](#dont-reveal-hardware-details-to-the-user-of-the-hal)
      - [The Processor Is a Detail](#the-processor-is-a-detail)
      - [The Operating System Is a Detail](#the-operating-system-is-a-detail)
    - [Programming to Interfaces and Substitutability](#programming-to-interfaces-and-substitutability)
    - [DRY Conditional Compilation Directives](#dry-conditional-compilation-directives)
  - [Conclusion](#conclusion-27)
- [PART VI Details](#part-vi-details)
- [Chapter 30 The Database Is a Detail](#chapter-30-the-database-is-a-detail)
  - [Relational Databases](#relational-databases)
  - [Why Are Database Systems So Prevalent?](#why-are-database-systems-so-prevalent)
  - [What If There Were No Disk?](#what-if-there-were-no-disk)
  - [Details](#details)
  - [But What about Performance?](#but-what-about-performance)
  - [Anecdote](#anecdote)
  - [Conclusion](#conclusion-28)
- [Chapter 31 The Web Is a Detail](#chapter-31-the-web-is-a-detail)
  - [The Endless Pendulum](#the-endless-pendulum)
  - [The Upshot](#the-upshot)
  - [Conclusion](#conclusion-29)
- [Chapter 32 Frameworks Are Details](#chapter-32-frameworks-are-details)
  - [Framework Authors](#framework-authors)
  - [Asymmetric Marriage](#asymmetric-marriage)
  - [The Risks](#the-risks)
  - [The Solution](#the-solution)
  - [I Now Pronounce You …](#i-now-pronounce-you-)
  - [Conclusion](#conclusion-30)
- [Chapter 33 Case Study: Video Sales](#chapter-33-case-study-video-sales)
  - [The Product](#the-product)
  - [Use Case Analysis](#use-case-analysis)
  - [Component Architecture](#component-architecture)
  - [Dependency Management](#dependency-management)
  - [Conclusion](#conclusion-31)
- [Chapter 34 The Missing Chapter](#chapter-34-the-missing-chapter)
  - [Package by Layer](#package-by-layer)
  - [Package by Feature](#package-by-feature)
  - [Ports and Adapters](#ports-and-adapters)
  - [Package by Component](#package-by-component)
  - [The Devil Is in the Implementation Details](#the-devil-is-in-the-implementation-details)
  - [Organization versus Encapsulation](#organization-versus-encapsulation)
  - [Other Decoupling Modes](#other-decoupling-modes)
  - [Conclusion: The Missing Advice](#conclusion-the-missing-advice)
- [Afterword](#afterword)
- [PART VII Appendix](#part-vii-appendix)
- [Appendix A Architecture Archaeology](#appendix-a-architecture-archaeology)
  - [Union Accounting System](#union-accounting-system)
  - [Aluminum Die-Cast Monitoring](#aluminum-die-cast-monitoring)
  - [4-TEL](#4-tel)
  - [The Service Area Computer](#the-service-area-computer)
    - [Dispatch Determination](#dispatch-determination)
    - [Architecture](#architecture-1)
    - [The Grand Redesign in the Sky](#the-grand-redesign-in-the-sky)
  - [C Language](#c-language)
    - [C](#c)
  - [BOSS](#boss)
    - [The Schedule Trap](#the-schedule-trap)
  - [DLU/DRU](#dludru)
    - [Architecture](#architecture-2)
  - [VRS](#vrs)
    - [Architecture](#architecture-3)
    - [VRS Conclusion](#vrs-conclusion)
  - [The Electronic Receptionist](#the-electronic-receptionist)
  - [Craft Dispatch System](#craft-dispatch-system)
  - [Clear Communications](#clear-communications)
    - [The Setup](#the-setup)
    - [Uncle Bob](#uncle-bob)
  - [ROSE](#rose)
    - [The Debates Continued](#the-debates-continued)
    - [... By Any Other Name](#-by-any-other-name)
  - [Conclusion](#conclusion-32)

## Foreword

As with any metaphor, describing software through the lens of architecture can hide as much as it can reveal. It can both promise more than it can deliver and deliver more than it promises.

It’s not obvious that software structure obeys our intuition the way building structure does.

Software is made of software. Large software constructs are made from smaller software components, which are in turn made of smaller software components still, and so on.

Software is recursive and fractal in nature, etched and sketched in code. Everything is details.

You can even argue quite convincingly that there is more design activity and focus in software than in building architecture—in this sense, it’s not unreasonable to consider software architecture more architectural than building architecture!

To mistake boxes for _the_ big picture— for _the_ architecture—is to miss the big picture and the architecture: Software architecture doesn’t look like anything.

Software may be such stuff as dreams are made on, but it runs in the physical world.

> This is the monstrosity in love, lady, that the will is infinite, and the execution confined; that the desire is boundless, and the act a slave to limit.
> — William Shakespeare

> Architecture represents the significant design decisions that shape a system, where significant is measured by cost of change.
> — Grady Booch

A good architecture meet the needs of its users, developers, and owners at a given point in time, but it also meets them over time.

> If you think good architecture is expensive, try bad architecture.
> — Brian Foote and Joseph Yoder

The kinds of changes a system’s development typically experiences should not be the changes that are costly, that are hard to make, that take managed projects of their own rather than being folded into the daily and weekly flow of work.

> Architecture is the decisions that you wish you could get right early in a project, but that you are not necessarily more likely to get them right than any other.
> — Ralph Johnson

Understanding the past is hard enough as it is; our grasp of the present is slippery at best; predicting the future is nontrivial.

The darkest path... ...strong and stable architecture comes from authority and rigidity. If change is expensive, change is eliminated... ...The architect’s mandate is total and totalitarian, with the architecture becoming a dystopia for its developers and a constant source of frustration for all... ...another path... ...speculative generality. A route filled with hard-coded guesswork, countless parameters, tombs of dead code, and more accidental complexity than you can shake a maintenance budget at... ...The path...cleanest... ...recognizes the softness of software and aims to preserve it as a first-class property of the system. It recognizes that we operate with incomplete knowledge, but it also understands that, as humans, operating with incomplete knowledge is something we do, something we’re good at. It plays more to our strengths than to our weaknesses. We create things and we discover things. We ask questions and we run experiments. A good architecture comes from understanding it more as a journey than as a destination, more as an ongoing process of enquiry than as a frozen artifact.

A good architecture comes from understanding it more as a journey than as a destination, more as an ongoing process of enquiry than as a frozen artifact.

> Architecture is a hypothesis, that needs to be proven by implementation and measurement.
> — Tom Gilb

> The only way to go fast, is to go well.
> — Robert C. Martin

## Preface

_The rules of software architecture are independent of every other variable._

There is one thing about the software we have now, compared to the software from back then: _It’s made of the same stuff._ It’s made of `if` statements, assignment statements, and `while` loops... ...you might object and say that we’ve got much better languages and superior paradigms... ...True—and yet the code is still just an assemblage of sequence, selection, and iteration, just as it was back in the 1960s and 1950s.

Changelessness of the code is the reason that the rules of software architecture are so consistent across system types. The rules of software architecture are the rules of ordering and assembling the building blocks of programs. And since those building blocks are universal and haven’t changed, the rules for ordering them are likewise universal and changeless.

## PART I Introduction

It doesn’t take a huge amount of knowledge and skill to get a program working... ...Getting it right is another matter entirely.

Getting software right is _hard._ It takes knowledge and skills... ...discipline and dedication... ...Mostly, it takes a passion for the craft and the desire to be a professional.

When software is done right, it requires a fraction of the human resources to create and maintain.

It is far more common to fight your way through terrible software designs than it is to enjoy the pleasure of working with a good one.

## Chapter 1 What Is Design and Architecture?

What is design? What is architecture? What are the differences between the two?... ...there is no difference between them. _None at all._

The low-level details and the high-level structure are all part of the same whole. They form a continuous fabric that defines the shape of the system. You can’t have one without the other; indeed, no clear dividing line separates them. There is simply a continuum of decisions from the highest to the lowest levels.

### The Goal?

_The goal of software architecture is to minimize the human resources required to build and maintain the required system._

The measure of design quality is simply the measure of the effort required to meet the needs of the customer. If that effort is low, and stays low... ...the design is good. If that effort grows with each new release, the design is bad.

### Case Study

“The race is not to the swift, nor the battle to the strong.”

“The more haste, the less speed.”

Modern developers... ...work their butts off. But a part of their brain _does_ sleep—the part that knows that good, clean, well-designed code _matters._

A familiar lie: “We can clean it up later; we just have to get to market first!” Of course, things never do get cleaned up later, because market pressures never abate. Getting to market first simply means that you’ve now got a horde of competitors on your tail, and you have to stay ahead of them by running as fast as you can.

Developers are overconfident in their ability to remain productive. But the creeping mess of code that saps their productivity never sleeps and never relents. If given its way, it will reduce productivity to zero in a matter of months.

The bigger lie that developers buy into is the notion that writing messy code makes them go fast in the short term, and just slows them down in the long term. Developers who accept this lie exhibit... ...overconfidence in their ability to switch modes from making messes to cleaning up messes sometime in the future, but they also make a simple error of fact. The fact is that _making messes is always slower than staying clean,_ no matter which time scale you are using.

_Making messes is always slower than staying clean._

_The only way to go fast, is to go well._

The only way to reverse the decline in productivity and the increase in cost is to get the developers to stop thinking... ...overconfident... ...and start taking responsibility for the mess that they’ve made.

_Their overconfidence will drive the redesign into the same mess as the original project._

### Conclusion

The best option is for the development organization to recognize and avoid its own overconfidence and to start taking the quality of its software architecture seriously.

To take software architecture seriously, you need to know what good software architecture is.

## Chapter 2 A Tale of Two Values

Every software system provides two different values to the stakeholders: behavior and structure.

### Behavior

The first value of software is its behavior. Programmers are hired to make machines behave in a way that makes or saves money for the stakeholders... ...Many programmers believe that is the entirety of their job. They believe their job is to make the machine implement the requirements and to fix any bugs. They are sadly mistaken.

### Architecture

Software was invented to be “soft.” It was intended to be a way to easily change the behavior of machines. If we’d wanted the behavior of machines to be hard to change, we would have called it _hardware._

Software must be soft—that is, it must be easy to change.

The difficulty in making a change should be proportional only to the scope of the change, and not to the _shape_ of the change.

It is this difference between scope and shape that often drives the growth in software development costs... ...From the stakeholders’ point of view, they are simply providing a stream of changes of roughly similar scope. From the developers’ point of view, the stakeholders are giving them a stream of jigsaw puzzle pieces that they must fit into a puzzle of ever-increasing complexity. Each new request is harder
to fit than the last, because the shape of the system does not match the shape of the request.

The more architecture prefers one shape over another, the more likely new features will be harder and harder to fit into that structure. Therefore architectures should be as shape agnostic are practical.

### The Greater Value

Function or architecture? Which of these two provides the greater value? Is it more important for the software system to work, or is it more important for the software system to be easy to change?... ...simple logical tool of examining the extremes

- _If you give me a program that works perfectly but is impossible to change, then it won’t work when the requirements change, and I won’t be able to make it work. Therefore the program will become useless._
- _If you give me a program that does not work but is easy to change, then I can make it work, and keep it working as requirements change. Therefore the program will remain continually useful._

If you ask the business managers if they want to be able to make changes, they’ll say that of course they do, but may then qualify their answer by noting that the current functionality is more important than any later flexibility. In contrast, if the business managers ask you for a change, and your estimated costs for that change are unaffordably high, the business managers will likely be furious that you allowed the system to get to the point where the change was impractical.

### Eisenhower’s Matrix

> I have two kinds of problems, the urgent and the important. The urgent are not important, and the important are never urgent.
> — Dwight D. Eisenhower

| **Important Urgent**   | **Important Not Urgent**   |
| ---------------------- | -------------------------- |
| **Unimportant Urgent** | **Unimportant Not Urgent** |
Figure 2.1 Eisenhower matrix

The first value of software—behavior—is urgent but not always particularly important. The second value of software—architecture—is important but never particularly urgent.

four couplets into priorities:
1. Urgent and important
2. Not urgent and important
3. Urgent and not important
4. Not urgent and not important

The architecture of the code... ...is in the top two... ...whereas the behavior... ...occupies the first and _third_ positions.

The mistake... ...is to elevate items in position 3 to position 1... ...fail to separate those features that are urgent but not important from those features that truly are urgent and important... ...leads to ignoring the important architecture... ...in favor of the unimportant features.

Business managers are not equipped to evaluate the importance of architecture. _That’s what software developers were hired to do._ Therefore it is the responsibility of the software development team to assert the importance of architecture over the urgency of features.

### Fight for the Architecture

Remember, as a software developer, _you are a stakeholder._ You have a stake in the software that you need to safeguard. That’s part of your role, and part of your duty. And it’s a big part of why you were hired.

Software architects are... ...more focused on the structure of the system than on its features and functions... ...create an architecture that allows those features and functions to be easily developed, modified, and extended.

If architecture comes last, then the system will become ever more costly to develop, and eventually change will become practically impossible for part or all of the system.

## PART II Starting with the Bricks: Programming Paradigms

Software architecture begins with the code.

Alan Turing... ...was the first to understand that programs were simply data... ...writing real programs on real computers... ...in the late 1940s, came assemblers... ...relieved the programmers... ...of translating their programs into binary. In 1951, Grace Hopper invented A0, the first compiler. In fact, she coined the term _compiler._ Fortran was invented in 1953... ...What followed was an unceasing flood of new programming languages.

Paradigms are ways of programming, relatively unrelated to languages. A paradigm tells you which programming structures to use, and when to use them. 

## Chapter 3 Paradigm Overview

### Structured Programming

Dijkstra in 1968... ...showed that the use of unrestrained jumps (`goto` statements) is harmful to program structure... ...he replaced those jumps with... ...`if/then/else` and `do/while/until` constructs.

_Structured programming imposes discipline on direct transfer of control._

### Object-Oriented Programming

1966... ...Ole Johan Dahl and Kristen Nygaard... ...noticed that the function call stack frame in the `ALGOL` language could be moved to a heap, thereby allowing local variables declared by a function to exist long after the function returned. The function became a constructor for a class, the local variables became instance variables, and the nested functions became methods. This led inevitably to the discovery of polymorphism through the disciplined use of function pointers.

_Object-oriented programming imposes discipline on indirect transfer of control._

### Functional Programming

Its invention predates computer programming itself... ...Alonzo Church, in 1936 invented λ-calculus while pursuing the same mathematical problem that was motivating Alan Turing at the same time. His λ-calculus is the foundation of the LISP language, invented in 1958 by John McCarthy. A foundational notion of λ-calculus is immutability—that is, the notion that the values of symbols do not change. This effectively means that a functional language has no assignment statement.

_Functional programming imposes discipline upon assignment._

### Food for Thought

Each of the paradigms _removes_ capabilities from the programmer. None of them adds new capabilities. Each imposes some extra discipline that is _negative_ in its intent. The paradigms tell us what _not_ to do, more than they tell us what _to_ do.

The three paradigms together remove `goto` statements, function pointers, and assignment.

These three paradigms are likely to be the only three we will see... ...they were all discovered within the ten years between 1958 and 1968. In the many decades that have followed, no new paradigms have been added.

### Conclusion

What... ...paradigms have to do with architecture? Everything. We use polymorphism as the mechanism to cross architectural boundaries; we use functional programming to impose discipline on the location of and access to data; and we use structured programming as the algorithmic foundation of our modules... ...those three align with the three big concerns of architecture: function, separation of components, and data management.

## Chapter 4 Structured Programming

### Proof

Dijkstra recognized... ...that programming is _hard,_ and that programmers don’t do it very well... ...Dijkstra’s solution was to apply the mathematical discipline of _proof_... ...Dijkstra discovered that certain uses of `goto`... ...preventing use of the divide-and-conquer approach necessary for reasonable proofs. Other uses of `goto`, however, did not have this problem... ...these “good” uses of `goto` corresponded to... ...structures such as `if/then/else` and `do/while.` Modules that used those kinds of control structures _could_ be recursively subdivided into provable units... ...those control structures, when combined with sequential execution, were special... ...Böhm and Jacopini, who proved that all programs can be constructed from just three structures: sequence, selection, and iteration... ...The very control structures that made a module provable were the same minimum set of control structures from which all programs can be built. Thus structured programming was born.

### A Harmful Proclamation

Nowadays we are all structured programmers, though not necessarily by choice. It’s just that our languages don’t give us the option to use undisciplined direct transfer of control.

### Functional Decomposition

Structured programming allows modules to be recursively decomposed into provable units, which in turn means that modules can be functionally decomposed.

By following these disciplines, programmers could break down large proposed systems into modules and components that could be further broken down into tiny provable functions.

### No Formal Proofs

But the proofs never came. The Euclidean hierarchy of theorems was never built. And programmers at large never saw the benefits of working through the laborious process of formally proving each and every little function correct. In the end, Dijkstra’s dream faded and died.

### Science to the Rescue

Science is fundamentally different from mathematics, in that scientific theories and laws cannot be proven correct... ...I can demonstrate these laws to you, and I can make measurements that show them correct to many decimal places, but I cannot prove them in the sense of a mathematical proof...there is always the chance that some experiment will show that those laws... ...are incorrect.

Scientific theories and laws are _falsifiable_ but not provable.

Science does not work by proving statements true, but rather by _proving statements false._ Those statements that we cannot prove false, after much effort, we deem to be true enough for our purposes.

Not all statements are provable. The statement "This is a lie" is neither true nor false.

Mathematics is the discipline of proving provable statements true. Science, in contrast, is the discipline of proving provable statements false.

### Tests

> Testing shows the presence, not the absence, of bugs.
> — Dijkstra

A program can be proven incorrect by a test, but it cannot be proven correct.

Tests... ...after sufficient testing effort allow us to deem a program to be correct enough for our purposes.

Software development is not a mathematical endeavor, even though it seems to manipulate mathematical constructs. Rather, software is like a science. We show correctness by failing to prove incorrectness, despite our best efforts.

A program that is not provable... ...cannot be deemed correct no matter how many tests are applied to it.

Structured programming forces us to recursively decompose a program into a set of small provable functions. We can then use tests to try to prove those small provable functions incorrect. If such tests fail to prove incorrectness, then we deem the functions to be correct enough for our purposes.

### Conclusion

It is this ability to create falsifiable units of programming that makes structured programming valuable today... ...Moreover, at the architectural level, this is why we still consider _functional decomposition_ to be one of our best practices.

Software is like a science... ...is driven by falsifiability. Software architects strive to define modules, components, and services that are easily falsifiable (testable). To do so, they employ restrictive disciplines similar to structured programming, albeit at a much higher level.

## Chapter 5 Object-Oriented Programming

The basis of a good architecture is the understanding and application of the principles of object-oriented design (OO).

Three magic words to explain the nature of OO: _encapsulation, inheritance, and polymorphism_... ...an OO language must support these three things.

### Encapsulation?

OO languages provide easy and effective encapsulation of data and function.

A line can be drawn around a cohesive set of data and functions. Outside of that line, the data is hidden and only some of the functions are known. We see this concept in action as the private data members and the public member functions of a class.

This idea is certainly not unique to OO. Indeed, we had perfect encapsulation in C... ...But then came OO in the form of C++—and the perfect encapsulation of C was broken. Java and C# simply abolished the header/implementation split altogether, thereby weakening encapsulation even more. In these languages, it is impossible to separate the declaration and definition of a class. For these reasons, it is difficult to accept that OO depends on strong encapsulation... ...the languages that claim to provide OO have only weakened the once perfect encapsulation we enjoyed with C.

### Inheritance?

Inheritance is simply the redeclaration of a group of variables and functions within an enclosing scope.

We might say that we had a kind of inheritance long before OO languages were invented. That statement wouldn’t quite be true, though. We had a trick, but it’s not nearly as convenient as true inheritance. Moreover, multiple inheritance is a considerably more difficult to achieve by such trickery.

While OO languages did not give us something completely brand new, it did make the masquerading of data structures significantly more convenient.

### Polymorphism?

Polymorphic behavior before OO languages? Of course... ...Consider this simple C `copy` program.

```c
#include <stdio.h>
void copy() {
  int c;
  while ((c=getchar()) != EOF)
    putchar(c);
}
```

These functions are _polymorphic_—their behavior depends on the type of `STDIN` and `STDOUT`... ...The UNIX operating system requires that every IO device driver provide five standard functions: `open`, `close`, `read`, `write`, and `seek`. The signatures of those functions must be identical for every IO driver.

The bottom line is that polymorphism is an application of pointers to functions... ...since Von Neumann architectures were first implemented in the late 1940s... ...OO languages may not have given us polymorphism, but they have made it much safer and much more convenient.

The problem with explicitly using pointers to functions to create polymorphic behavior is that pointers to functions are _dangerous._ Such use is driven by a set of manual conventions... ...OO languages eliminate these conventions and, therefore, these dangers.

OO imposes discipline on indirect transfer of control.

#### The Power of Polymorphism

The IO devices have become plugins... ...our programs should be _device independent._

OO allows the plugin architecture to be used anywhere, for anything.

#### Dependency Inversion

Before a safe and convenient mechanism for polymorphism was available. In the typical calling tree, main functions called high-level functions, which called mid-level functions, which called low-level functions... ...source code dependencies inexorably followed the flow of control (Figure 5.1).

![Figure 5.1 Source code dependencies versus flow of control](./assets/figure5.1.jpg)

Figure 5.1 Source code dependencies versus flow of control

![Figure 5.2 Dependency inversion](./assets/figure5.2.jpg)

Figure 5.2 Dependency inversion

In Figure 5.2, module `HL1` calls the `F()` function in module `ML1`... ...At runtime, the interface doesn’t exist. `HL1` simply calls `F()` within `ML1`... ...the source code dependency (the inheritance relationship) between `ML1` and the interface `I` points in the opposite direction compared to the flow of control. This is called _dependency inversion,_ and its implications for the software architect are profound... ...convenient polymorphism means that _any source code dependency, no matter where it is, can be inverted_... ...software architects... ...have _absolute control_ over the direction of all source code dependencies in the system. They are not constrained to align those dependencies with the flow of control. No matter which module does the calling and which module is called, the software architect can point the source code dependency in either direction... ...That is the power that OO provides.

UI and the database can be plugins to the business rules... ...the source code of the business rules never mentions the UI or the database.

When the source code in a component changes, only that component needs to be redeployed. This is _independent deployability._

If the modules in your system can be deployed independently, then they can be developed independently by different teams. That’s _independent developability._

### Conclusion

OO is the ability, through the use of polymorphism, to gain absolute control over every source code dependency in the system.

It allows... ...to create a plugin architecture,... ...The low-level details are relegated to plugin modules that can be deployed and developed independently from the modules that contain high-level policies.

## Chapter 6 Functional Programming

Functional programming predate programming itself... ...is based on the λ-calculus invented by Alonzo Church in the 1930s.

### Squares of Integers

Java Program

```java
public class Squint {
  public static void main(String args[]) {
    for (int i=0; i<25; i++)
    System.out.println(i*i);
  }
}
```

Clojure Program

```clojure
(println (take 25 (map (fn [x] (* x x)) (range))))
```

```clojure
(println ;___________________ Print
  (take 25 ;_________________ the first 25
    (map (fn [x] (* x x)) ;__ squares 
      (range)))) ;___________ of Integers
```

The Java program uses a _mutable variable_—a variable that changes state during the execution of the program... ...In the Clojure program, variables like x are initialized, but they are never modified.

Variables in functional languages _do not vary._

### Immutability and Architecture

All race conditions, deadlock conditions, and concurrent update problems are due to mutable variables... ...all the problems that we face in concurrent applications—all the problems we face in applications that require multiple threads, and multiple processors—cannot happen if there are no mutable variables.

Immutability is practicable... ...if you have infinite storage and infinite processor speed. Lacking those infinite resources, the answer is a bit more nuanced.

### Segregation of Mutability

One of the most common compromises in regard to immutability is to segregate the application... ...into mutable and immutable components. The immutable components perform their tasks in a purely functional way, without using any mutable variables... ...communicate with... ...other components that are not purely functional, and allow for the state of variables to be mutated (Figure 6.1).

![Figure 6.1 Mutating state and transactional memory](./assets/figure6.1.jpg)

Figure 6.1 Mutating state and transactional memory

It is common practice to use... ..._transactional memory_ to protect the mutable variables from concurrent updates and race conditions... ...It protects those variables with a transaction-or retry-based scheme.

Well-structured applications will be segregated into those components that do not mutate variables and those that do... ...by the use of appropriate disciplines to protect those mutated variables. Architects would be wise to push as much processing as possible into the immutable components, and to drive as much code as possible out of those components that must allow mutation.

### Event Sourcing

The more memory we have, and the faster our machines are, the less we need mutable state.

Imagine a banking application that maintains the account balances of its customers. It mutates those balances when deposit and withdrawal transactions are executed. Now imagine that instead of storing the account balances, we store only the transactions. Whenever anyone wants to know the balance of an account, we simply add up all the transactions for that account, from the beginning of time. This scheme requires no mutable variables... ...Over time, the number of transactions would grow without bound, and the processing power required to compute the totals would become intolerable. To make this scheme work forever, we would need infinite storage and infinite processing power. But perhaps we don’t have to make the scheme work forever. And perhaps we have enough storage and enough processing power to make the scheme work for the reasonable lifetime of the application. This is the idea behind _event sourcing._

Event sourcing is a strategy wherein we store the transactions, but not the state. When state is required, we simply apply all the transactions from the beginning of time.

We can take shortcuts... ...and save the state every midnight. Then... ...we need compute only the transactions since midnight.

Nothing ever gets deleted or updated from such a data store. As a consequence, our applications are not CRUD; they are just CR... ...there cannot be any concurrent update issues.

If we have enough storage and enough processor power, we can make our applications entirely immutable—and, therefore, _entirely functional._

This is the way your source code control system works.

### Conclusion

- Structured programming is discipline imposed upon direct transfer of control.
- Object-oriented programming is discipline imposed upon indirect transfer of control.
- Functional programming is discipline imposed upon variable assignment.

Each of these three paradigms has taken something away from us. Each restricts some aspect of the way we write code. None of them has added to our power or our capabilities.

Software is not a rapidly advancing technology. The rules of software are the same today as they were in 1946, when Alan Turing wrote the very first code... ...The tools have changed, and the hardware has changed, but the essence of software remains the same.

Software—the stuff of computer programs—is composed of sequence, selection, iteration, and indirection. Nothing more. Nothing less.

## PART III Design Principles

Good software systems begin with clean code. On the one hand, if the bricks aren’t well made, the architecture of the building doesn’t matter much. On the other hand, you can make a substantial mess with well-made bricks. This is where the SOLID principles come in.

The SOLID principles tell us how to arrange our functions and data structures into classes, and how those classes should be interconnected. The use of the word "class" does not imply that these principles are applicable only to object-oriented software. A class is simply a coupled grouping of functions and data. Every software system has such groupings, whether they are called classes or not. The SOLID principles apply to those groupings.

The goal of the principles is the creation of mid-level software structures that:
- Tolerate change,
- Are easy to understand, and
- Are the basis of components that can be used in many software systems.

The term "mid-level" refers to the fact that... ...They are applied just above the level of the code and help to define the kinds of software structures used within modules and components.

The executive summary:
- **SRP:** The Single Responsibility Principle. An active corollary to Conway’s law: The best structure for a software system is heavily influenced by the social structure of the organization that uses it so that each software module has one, and only one, reason to change.
- **OCP:** The Open-Closed Principle. Bertrand Meyer made this principle famous in the 1980s. The gist is that for software systems to be easy to change, they must be designed to allow the behavior of those systems to be changed by adding new code, rather than changing existing code.
- **LSP:** The Liskov Substitution Principle. Barbara Liskov’s famous definition of subtypes, from 1988. In short, this principle says that to build software systems from interchangeable parts, those parts must adhere to a contract that allows those parts to be substi- tuted one for another.
- **ISP:** The Interface Segregation Principle. This principle advises software designers to avoid depending on things that they don’t use.
- **DIP:** The Dependency Inversion Principle. The code that implements high-level policy should not depend on the code that implements low-level details. Rather, details should depend on policies.

> Any organization that designs a system (defined broadly) will produce a design whose structure is a copy of the organization's communication structure.
> — Melvin E. Conway

## Chapter 7 SRP: The Single Responsibility Principle

The Single Responsibility Principle (SRP) might be the least well understood... ...It is too easy for programmers to hear the name and then assume that it means that every module should do just one thing... ...there _is_ a principle like that. A _function_ should do one, and only one, thing. We use that... ...when we are refactoring... ...at the lowest levels. But it is not one of the SOLID principles—it is not the SRP.

Historically, the SRP has been described this way: _A module should have one, and only one, reason to change_... ...satisfy users and stakeholders... ..._are_ the "reason to change"... ...Indeed, we can rephrase the principle to... ..._A module should be responsible to one, and only one, user or stakeholder_... ...the words "user" and "stakeholder" aren’t really the right words to use here... ...we’re really referring to a group... ...We’ll refer to that group as an _actor._ Thus the final version of the SRP is: _A module should be responsible to one, and only one, actor._

A module is just a cohesive set of functions and data structures... ..."cohesive" implies the SRP. Cohesion is the force that binds together the code responsible to a single actor.

The best way to understand this principle is by looking at the symptoms of violating it.

### Symptom 1: Accidental Duplication

![Figure 7.1 The Employee class](./assets/figure7.1.jpg)

Figure 7.1 The `Employee` class

`Employee` class three methods: _calculatePay()_, _reportHours()_, and _save()_ (Figure 7.1)... ...violates the SRP because those three methods are responsible to... ...different actors.
- The `calculatePay()`... ...by the accounting department, which reports to the CFO.
- The `reportHours()`... ...by the human resources department, which reports to the COO.
- The `save()`... ...by the database administrators (DBAs), who report to the CTO
By putting... ...these three methods into a single `Employee` class, the developers have coupled each of these actors to the others. This Symptom 1: Accidental Duplication coupling can cause the actions of the CFO’s team to affect something that the COO’s team depends on.

These problems occur because we put code that different actors depend on into close proximity. The SRP says to _separate the code that different actors depend on._

### Symptom 2: Merges

Merges will be common in source files that contain many different methods. This situation is especially likely if those methods are responsible to different actors.

Merges are risky affairs... ...no tool can deal with every merge case. In the end, there is always risk.

Multiple people changing the same source file for different reasons... ...to avoid this problem is to _separate code that supports different actors._

### Solutions

Many different solutions to this problem. Each moves the functions into different classes.

The most obvious way to solve the problem is to separate the data from the functions... ...

![Figure 7.3 The three classes do not know about each other](./assets/figure7.3.jpg)

Figure 7.3 The three classes do not know about each other

The downside of this solution is that the developers now have three classes that they have to instantiate and track. A common solution to this dilemma is to use the _Facade_ pattern (Figure 7.4).

![Figure 7.4 The Facade pattern](./assets/figure7.4.jpg)

Figure 7.4 The `Facade` pattern

The `EmployeeFacade` contains very little code. It is responsible for instantiating and delegating to the classes with the functions.

To keep the most important business rules closer to the data... ...can be done by keeping the most important method in the original Employee class and then using that class as a Facade for the lesser functions (Figure 7.5).

![Figure 7.5 The most important method is kept in the original Employee class and used as a Facade for the lesser functions](./assets/figure7.5.jpg)

Figure 7.5 The most important method is kept in the original `Employee` class and used as a Facade for the lesser functions

Every class would contain just one function. This is hardly the case. The number of functions required... ...is likely to be large in each case. Each of those classes would have many _private_ methods in them.

Each of the classes that contain such a family of methods is a scope. Outside of that scope, no one knows that the private members of the family exist.

### Conclusion

The Single Responsibility Principle is about functions and classes... ...At the level of components, it becomes the Common Closure Principle. At the architectural level, it becomes the Axis of Change responsible for the creation of Architectural Boundaries.

## Chapter 8 OCP: The Open-Closed Principle

The Open-Closed Principle (OCP) was coined in 1988 by Bertrand Meyer.

> A software artifact should be open for extension but closed for modification.
> — Bertrand Meyer.

The behavior of a software artifact ought to be extendible, without having to modify that artifact... ...is the most fundamental reason that we study software architecture... ...if simple extensions to the requirements force massive changes to the software, then the architects... ...have engaged in a spectacular failure.

## A Thought Experiment

Imagine... ...that we have a system... ...some new code must be written. But how much old code will have to change? A good software architecture would reduce the amount of changed code to the barest minimum. Ideally, zero. How? By properly separating the things that change for different reasons (the Single Responsibility Principle), and then organizing the dependencies between those things properly (the Dependency Inversion Principle).

![Figure 8.1 Applying the SRP](./assets/figure8.1.jpg)

Figure 8.1 Applying the SRP

Applying the SRP, we... ...come up with the data-flow view shown in Figure 8.1.... ...generating the report involves two separate responsibilities: the calculation of the reported data, and the presentation of that data into a web- and printer-friendly form.

Having made this separation, we need to organize the source code dependencies to ensure that changes to one of those responsibilities do not cause changes in the other. Also, the new organization should ensure that the behavior can be extended without undo modification.

Partitioning the processes into classes, and separating those classes into components, as shown... ...in the diagram in Figure 8.2. In this figure, the component at the upper left is the _Controller._ At the upper right, we have the _Interactor._ At the lower right, there is the _Database._ Finally, at the lower left, there are four components that represent the _Presenters_ and the _Views._ Classes marked with `<I>` are interfaces; those marked with `<DS>` are data structures. Open arrowheads are _using_ relationships. Closed arrowheads are _implements_ or _inheritance_ relationships.

![Figure 8.2 Partitioning the processes into classes and separating the classes into components](./assets/figure8.2.jpg)

Figure 8.2 Partitioning the processes into classes and separating the classes into components

All the dependencies are _source code_ dependencies. An arrow pointing from class A to class B means that the source code of class A mentions the name of class B, but class B mentions nothing about class A. 

all component relationships are unidirectional, as shown in the component graph in Figure 8.3. These arrows point toward the components that we want to protect from change.

![Figure 8.3 The component relationships are unidirectional](./assets/figure8.3.jpg)

Figure 8.3 The component relationships are unidirectional

If component A should be protected from changes in component B, then component B should depend on component A.

We want to protect the _Controller_ from changes in the _Presenters._ We want to protect the _Presenters_ from changes in the _Views._ We want to protect the _Interactor_ from changes in—well, _anything._... ...Because it contains the business rules. The Interactor contains the highest-level policies of the application. All the other components are dealing with peripheral concerns. The _Interactor_ deals with the central concern.

This creates a hierarchy of protection based on the notion of "level." _Interactors_ are the highest-level concept, so they are the most protected. _Views_ are among the lowest-level concepts, so they are the least protected. _Presenters_ are higher level than _Views,_ but lower level than the _Controller_ or the _Interactor._

How the OCP works at the architectural level. Architects separate functionality based on how, why, and when it changes, and then organize that separated functionality into a hierarchy of components. Higher-level components in that hierarchy are protected from the changes made to lower-level components.

### Directional Control

Much of the complexity... ...was intended to make sure that the dependencies between the components pointed in the correct direction. For example, the `FinancialDataGateway` interface between the `FinancialReportGenerator` and the `FinancialDataMapper` exists to invert the dependency that would otherwise have pointed from the _Interactor_ component to the _Database_ component.

### Information Hiding

The `FinancialReportRequester` is there to protect the `FinancialReportController` from knowing too much about the internals of the _Interactor._ If that interface were not there, then the _Controller_ would have transitive dependencies on the `FinancialEntities`.

Transitive dependencies are a violation of the general principle that software entities should not depend on things they don’t directly use.

Even though our first priority is to protect the _Interactor_ from changes to the _Controller,_ we also want to protect the _Controller_ from changes to the _Interactor_ by hiding the internals of the _Interactor._

### Conclusion

The OCP... ...goal is to make the system easy to extend without incurring a high impact of change. Accomplished by partitioning the system into components, and arranging those components into a dependency hierarchy that protects higher-level components from changes in lower-level components.

## Chapter 9 LSP: The Liskov Substitution Principle

> What is wanted here is something like the following substitution property: If for each object o1 of type S there is an object o2 of type T such that for all programs P defined in terms of T, the behavior of P is unchanged when o1 is substituted for o2 then S is a subtype of T.
> — Barbara Liskov, “Data Abstraction and Hierarchy,” SIGPLAN Notices 23, 5 (May 1988).

### Guiding the Use of Inheritance

Imagine... ...a class named `License`, as shown in Figure 9.1... ...`calcFee()`, is called by the `Billing` application... ...This design conforms to the LSP because the behavior of the `Billing` application does not depend,... ...on which of the two subtypes it uses. Both of the subtypes are substitutable for the `License` type.

![Figure 9.1 License, and its derivatives, conform to LSP](./assets/figure9.1.jpg)

Figure 9.1 `License`, and its derivatives, conform to LSP

### The Square/Rectangle Problem

![Figure 9.2 The infamous square/rectangle problem](./assets/figure9.2.jpg)

Figure 9.2 The infamous square/rectangle problem

The canonical example of a violation of the LSP is the... ...square/rectangle problem (Figure 9.2)... ...`Square` is not a proper subtype of `Rectangle` because the height and width of the `Rectangle` are independently mutable; in contrast, the height and width of the `Square` must change together... ...to defend against this kind of LSP violation... ...add mechanisms to the `User` (such as an `if` statement) that detects whether the `Rectangle` is, in fact, a `Square`. Since the behavior of the `User` depends on the types it uses, those types are not substitutable.

### LSP and Architecture

In the early years... ...LSP... ...way to guide the use of inheritance... ...However, over the years... ...has morphed into a broader principle of software design... ...to interfaces and implementations.

The LSP is applicable because there are users who depend on well-defined interfaces, and on the substitutability of the implementations of those interfaces.

The best way to understand the LSP from an architectural viewpoint is to look at what happens to the architecture of a system when the principle is violated.

### Example LSP Violation

No architect worth his or her salt would allow... ...Putting word... ...into the code itself creates an opportunity for all kinds of horrible and mysterious errors, not to mention security breaches.

### Conclusion

The LSP can, and should, be extended to the level of architecture. A simple violation of substitutability, can cause a system’s architecture to be polluted with a significant amount of extra mechanisms.

## Chapter 10 ISP: The Interface Segregation Principle

![Figure 10.1 The Interface Segregation Principle](./assets/figure10.1.jpg)

Figure 10.1 The Interface Segregation Principle

The Interface Segregation Principle (ISP) derives... ...from the diagram... ...in Figure 10.1... ...several users who use the operations of the `OPS` class... ...the source code of `User1` will... ...depend on `op2` and `op3`, even though it doesn’t call them... ...a change to the source code of `op2` in `OPS` will force `User1` to be recompiled and redeployed... ...This problem can be resolved by segregating the operations into interfaces as shown in Figure 10.2... ...`User1` will depend on `U1Ops`, and `op1`, but will not depend on `OPS`. Thus a change to `OPS` that `User1` does not care about will not cause `User1` to be recompiled and redeployed.

![Figure 10.2 Segregated operations](./assets/figure10.2.jpg)

Figure 10.2 Segregated operations

### ISP and Language

The previously description depends critically on language type. Statically typed languages force programmers to create declarations that users must `import`, or `use`, or otherwise `include`... ...that create the source code dependencies that force recompilation and redeployment. In dynamically typed languages... ...such declarations don’t exist... ...they are inferred at runtime. Thus there are no source code dependencies to force recompilation and redeployment.

Dynamically typed languages create systems that are more flexible and less tightly coupled than statically typed languages.

### ISP and Architecture

It is harmful to depend on modules that contain more than you need.

![Figure 10.3 A problematic architecture](./assets/figure10.3.jpg)

Figure 10.3 A problematic architecture

For example, an architect working on a system, S... ...So S depends on F. which depends on D (Figure 10.3). Now suppose that D contains features that F does not use and, therefore, that S does not care about. Changes to those features within D may well force the redeployment of F and, therefore, the redeployment of S. Even worse, a failure of one of the features within D may cause failures in F and S.

### Conclusion

Depending on something that carries baggage that you don’t need can cause you troubles that you didn’t expect.

## Chapter 11 DIP: The Dependency Inversion Principle

The Dependency Inversion Principle (DIP) tells us that the most flexible systems are those in which source code dependencies refer only to abstractions, not to concretions.

The `use`, `import`, and `include` statements should refer only to source modules containing interfaces, abstract classes, or some other kind of abstract declaration. Nothing concrete should be depended on.

Source code dependencies should not refer to concrete modules.

Treating this idea as a rule is unrealistic, because software systems must depend on many concrete facilities. For example, the `String` class in Java... ...dependency on the concrete `java.lang.string` cannot, and should not, be avoided.

We tend to ignore the stable background of operating system and platform facilities when it comes to DIP. We tolerate those concrete dependencies because we know we can rely on them not to change.

It is the _volatile_ concrete elements of our system that we want to avoid depending on... ...modules that we are actively developing, and that are undergoing frequent change.

### Stable Abstractions

Every change to an abstract interface corresponds to a change to its concrete implementations. Conversely, changes to concrete implementations do not always, or even usually, require changes to the interfaces that they implement. Therefore interfaces are less volatile than implementations.

Try to find ways to add functionality to implementations without making changes to the interfaces. This is Software Design 101.

Stable software architectures are those that avoid depending on volatile concretions, and that favor the use of stable abstract interfaces.

Coding practices:
- **Don’t refer to volatile concrete classes.** Refer to abstract interfaces instead.
- **Don’t derive from volatile concrete classes.** This is a corollary to the previous rule.
- **Don’t override concrete functions.** Concrete functions often require source code dependencies. When you override those functions, you do not eliminate those dependencies—indeed, you _inherit_ them... ...make the function abstract and create multiple implementations.
- **Never mention the name of anything concrete and volatile.** This is really just a restatement of the principle itself.

In statically typed languages, inheritance is the strongest, and most rigid, of all the source code relationships; consequently, it should be used with great care. In dynamically typed languages, inheritance is less of a problem, but it is still a dependency—and caution is always the wisest choice.

### Factories

The creation of volatile concrete objects requires special handling... ...because, in virtually all languages, the creation of an object requires a source code dependency on the concrete definition of that object.

In most object-oriented languages... ...we would use an _Abstract Factory_ to manage this undesirable dependency... ...Figure 11.1 shows the structure. The `Application` uses the `ConcreteImpl` through the `Service` interface. However, the `Application` must somehow create instances of the `ConcreteImpl`. To achieve this without creating a source code dependency on the `ConcreteImpl`, the `Application` calls the `makeSvc` method of the `ServiceFactory` interface. This method is implemented by the `ServiceFactoryImpl` class, which derives from `ServiceFactory`. That implementation instantiates the `ConcreteImpl` and returns it as a `Service`. The curved line in Figure 11.1 is an architectural boundary. It separates the abstract from the concrete. All source code dependencies cross that curved line pointing in the same direction, toward the abstract side.

![Figure 11.1 Use of the Abstract Factory pattern to manage the dependency](./assets/figure11.1.jpg)

Figure 11.1 Use of the _Abstract Factory_ pattern to manage the dependency

The abstract component contains all the high-level business rules of the application. The concrete component contains all the implementation details that those business rules manipulate.

The flow of control crosses the curved line in the opposite direction of the source code dependencies. The source code dependencies are inverted against the flow of control—which is why we refer to this principle as Dependency Inversion.

### Concrete Components

The concrete component in Figure 11.1 contains a single dependency, so it violates the DIP. This is typical. DIP violations cannot be entirely removed, but they can be gathered into a small number of concrete components and kept separate from the rest of the system.

Most systems will contain at least one concrete component—often called `main` because it contains the `main` function... ...in Figure 11.1, the `main` function would instantiate the `ServiceFactoryImpl` and place that instance in a global variable of type `ServiceFactory`. The `Application` would then access the factory through that global variable.

### Conclusion

DIP... ...will be the most visible organizing principle in our architecture diagrams.

The curved line in Figure 11.1 will become the architectural boundaries... ...The way the dependencies cross that curved line in one direction, and toward more abstract entities, will become... ...the _Dependency Rule._

## PART IV Component Principles

The SOLID principles tell us how to arrange the bricks into walls and... ...component principles tell us how to arrange the rooms into buildings. Large software systems, like large buildings, are built out of smaller components.

## Chapter 12 Components

Components are... ...the smallest entities that can be deployed as part of a system... ...In all languages, they are the granule of deployment.

Regardless of how they are eventually deployed, well designed components always retain the ability to be independently deployable and, therefore, independently developable.

### A Brief History of Components

In the early years of software development, programmers controlled the memory location and layout of their programs... ...This kind of programming is a foreign concept for most programmers today. They rarely have to think about where a program is loaded in the memory of the computer. But in the early days... ...programs were not relocatable.

How did you access a library function in those olden days?... ...Programmers included the source code of the library functions with their application code... ...Libraries were kept in source, not in binary.

The problem... ...was that... ...devices were slow and memory was expensive... ...Compiling a large program could take hours... ...To shorten the compile times, programmers separated the source code of the function library from the applications. They compiled the function library separately and loaded the binary at a known address... ...When they wanted to run an application, they would load the binary function library,2 and then load the application... ...soon applications grew to be larger than the space allotted... ...programmers had to split their applications into two address segments, jumping around the function library... ...this was not a sustainable situation. As programmers added more functions to the function library, it exceeded its bounds, and they had to allocate more space for it... ...This fragmentation of programs and libraries necessarily continued as computer memory grew. Clearly, something had to be done.

### Relocatability

Relocatable binaries... ...The compiler was changed to output binary code that could be relocated in memory by a smart loader. The loader would be told where to load the relocatable code. The relocatable code was instrumented with flags that told the loader which parts of the loaded data had to be altered to be loaded at the selected address. Usually this just meant adding the starting address to any memory reference addresses in the binary. Now the programmer could tell the loader where to load the function library, and where to load the application... ...This allowed programmers to load only those functions that they needed... ...The compiler was also changed to emit the names of the functions as metadata in the relocatable binary... ...Then the loader could _link_ the external references to the external definitions... ...And the linking loader was born.

### Linkers

The linking loader allowed programmers to divide their programs up onto separately compilable and loadable segments.

As programs grew larger and larger, and more library functions accumulated in libraries, a linking loader could take more than an hour just to load the program. Eventually, the loading and the linking were separated into two phases.... ...the slow part—the part that did that linking... ...into a separate application called the _linker._ The output... ...was a linked relocatable that a relocating loader could load very quickly. This allowed programmers to prepare an executable using the slow linker, but then they could load it quickly, at any time.

Then came the 1980s. Programmers were working in C or some other high- level language. As their ambitions grew, so did their programs. Programs that numbered hundreds of thousands of lines of code were not unusual... ...The linker would then take even more time. Turnaround had again grown to an hour or more in many cases... ...Throughout the 1960s, 1970s, and 1980s, all the changes made to speed up workflow were thwarted by programmers’ ambitions, and the size of the programs they wrote... ...of course... ..._Programs will grow to fill all available compile and link time._

In the late 1980s... ...Disks started to shrink and got significantly faster. Computer memory started to get so ridiculously cheap that much of the data on disk could be cached in RAM. Computer clock rates increased from 1 MHz to 100 MHz. By the mid-1990s, the time spent linking had begun to shrink faster than our ambitions could make programs grow. In many cases, link time decreased to a matter of _seconds._ For small jobs, the idea of a linking loader became feasible again... ...We could link together several... ...files, or several shared libraries in a matter of seconds, and execute the resulting program. And so the component plugin architecture was born.

### Conclusion

These dynamically linked files, which can be plugged together at runtime, are the software components of our architectures. It has taken 50 years, but we have arrived at a place where component plugin architecture can be the casual default as opposed to the herculean effort it once was.

## Chapter 13 Component Cohesion

Three principles of component cohesion:
- **REP:** The Reuse/Release Equivalence Principle
- **CCP:** The Common Closure Principle
- **CRP:** The Common Reuse Principle

### The Reuse/Release Equivalence Principle

_The granule of reuse is the granule of release._

The last decade... ...a vast number of reusable components and component libraries have been created. We are now living in the age of software reuse—a fulfillment of one of the oldest promises of the object- oriented model.

The Reuse/Release Equivalence Principle (REP)... ...components are tracked through a release process and are given release numbers... ...to ensure that all the reused components are compatible with each other... ...developers need to know when new releases are coming, and which changes those new releases will bring.

The release process must produce the appropriate notifications and release documentation so that users can make informed decisions about when and whether to integrate the new release.

Classes and modules that are formed into a component must belong to a cohesive group.

Classes and modules that are grouped together into a component should be _releasable_ together.

The fact that they share the same version number and the same release tracking, and are included under the same release documentation, should make sense both to the author and to the users.

It is hard to precisely explain the glue that holds the classes and modules together into a single component... ...violations are easy to detect— they don’t “make sense.” If you violate the REP, your users will know, and they won’t be impressed with your architectural skills.

The weakness of this principle is... ...compensated for by the strength of... ...the CCP and the CRP.

### The Common Closure Principle

_Gather into components those classes that change for the same reasons and at the same times. Separate into different components those classes that change at different times and for different reasons._

This is the Single Responsibility Principle restated for components. Just as the SRP says that a _class_ should not contain multiples reasons to change, so the Common Closure Principle (CCP) says that a _component_ should not have multiple reasons to change.

For most applications, maintainability is more important than reusability. If the code in an application must change, you would rather that all of the changes occur in one component, rather than being distributed across many components

If changes are confined to a single component, then we need to redeploy only the one changed component. Other components that don’t depend on the changed component do not need to be revalidated or redeployed.

This principle is closely associated with the Open Closed Principle (OCP). Indeed, it is "closure" in the OCP sense of the word that the CCP addresses. The OCP states that classes should be closed for modification but open for extension. Because 100% closure is not attainable, closure must be strategic. We design our classes such that they are closed to the most common kinds of changes that we expect or have experienced.

The CCP... ...by gathering together... ...those classes that are closed to the same types of changes... ...when a change in requirements comes along... ...being restricted to a minimal number of components.

#### Similarity with SRP

_Gather together those things that change at the same times and for the same reasons. Separate those things that change at different times or for different reasons._

### The Common Reuse Principle

_Don’t force users of a component to depend on things they don’t need._

The Common Reuse Principle (CRP)... ...helps us to decide which classes and modules should be placed into a component... ...classes and modules that tend to be reused together belong in the same component.

Classes are seldom reused in isolation. More typically, reusable classes collaborate with other classes that are part of the reusable abstraction... ...these classes belong together in the same component. In such... ...we would expect... ...classes that have lots of dependencies on each other.

The CRP... ...tells us which classes _not_ to keep together in a component. When one component uses another, a dependency is created between... ...The _using_ component depends on the _used_ component... ...every time the _used_ component is changed, the _using_ component will need corresponding changes.

When we depend on a component, we want to make sure we depend on every class in that component... ...we want to make sure that the classes that we put into a component are inseparable—that it is impossible to depend on some and not on the others. Otherwise, we will be redeploying more components than is necessary.

Classes that are not tightly bound to each other should not be in the same component.

#### Relation to ISP

The CRP is the generic version of the ISP. The ISP advises us not to depend on classes that have methods we don’t use. The CRP advises us not to depend on components that have classes we don’t use.

_Don’t depend on things you don’t need._

### The Tension Diagram for Component Cohesion

The three cohesion principles tend to fight each other. The REP and CCP are _inclusive_ principles: Both tend to make components larger. The CRP is an _exclusive_ principle, driving components to be smaller. It is the tension between these principles that good architects seek to resolve.

Figure 13.1 is a tension diagram that shows how the three principles of cohesion interact with each other. The edges of the diagram describe the _cost_ of abandoning the principle on the opposite vertex. 

![Figure 13.1 Cohesion principles tension diagram](./assets/figure13.1.jpg)

Figure 13.1 Cohesion principles tension diagram

An architect who focuses on just the REP and CRP will find that too many components are impacted when simple changes are made. In contrast, an architect who focuses too strongly on the CCP and REP will cause too many unneeded releases to be generated.

A good architect finds a position in that tension triangle that meets the _current_ concerns of the development team, but is also aware that those concerns will change over time.

Early in the development of a project, the CCP is much more important than the REP, because developability is more important than reuse.

Projects tend to start on the right hand side of the triangle... ...As the project matures, and other projects begin to draw from it, the project will slide over to the left.... ...the component structure of a project can vary with time and maturity. It has more to do with the way that project is developed and used, than with what the project actually does.

It has more to do with the way that project is developed and used, than with what the project actually does.

### Conclusion

In the past, our view of cohesion was... ...that cohesion was simply the attribute that a module performs one, and only one, function. However, the three principles of component cohesion describe a much more complex variety of cohesion... ...we must consider the opposing forces involved in reusability and develop-ability. Balancing these forces... ...is nontrivial. Moreover, the balance is almost always dynamic. That is, the partitioning that is appropriate today might not be appropriate next year... ...the composition of the components will jitter and evolve... ...as the focus of the project changes from develop-ability to reusability. 

## Chapter 14 Component Coupling

The forces that impinge upon the architecture of a component structure are technical, political, and volatile.

### The Acyclic Dependencies Principle

_Allow no cycles in the component dependency graph._

Worked all day, gotten some stuff working, and then gone home, only to arrive the next morning to find that your stuff no longer works? Why doesn’t it work? Because somebody stayed later than you and changed something you depend on!... ..."the morning after syndrome."

The "morning after syndrome" occurs in development environments where many developers are modifying the same source files. In small projects... ...it isn’t too big a problem. But as... ...the project and the development team grow, the mornings after can get pretty nightmarish... ...everyone keeps on changing and changing their code trying to make it work with the last changes that someone else made.

Two solutions... ..."the weekly build," and... ...the Acyclic Dependencies Principle (ADP).

#### The Weekly Build

The weekly build... ...All the developers ignore each other for the first four days of the week. They all work on private copies of the code, and don’t worry about integrating their work on a collective basis. Then, on Friday, they integrate all their changes and build the system... ...advantage of allowing the developers to live in an isolated world for four days out of five. The disadvantage... ...large integration penalty that is paid on Friday.

Eventually this situation becomes so frustrating that the developers, or the project managers, declare that the schedule should be changed to a biweekly build. This suffices for a time, but... ...this scenario leads to a crisis... ...Integration and testing become increasingly harder to do, and the team loses the benefit of rapid feedback.

#### Eliminating Dependency Cycles

Partition the development environment into releasable components.

Components become units of work that can be the responsibility of a single developer, or a team of developers... ...they release it for use by the other developers... ...They then continue to modify their component in their own private areas. Everyone else uses the released version.

As new releases of a component are made available, other teams... ...Once they decide that they are ready, they begin to use the new release.

No team is at the mercy of the others... ...Moreover, integration happens in small increments.

To make it work successfully, however, you must _manage_ the dependency structure of the components. _There can be no cycles._ If there are cycles in the dependency structure, then the "morning after syndrome" cannot be avoided.

The component diagram in Figure 14.1... ...this structure is a _directed graph._ The components are the _nodes,_ and the dependency relationships are the _directed edges_... ...Regardless of which component you begin at, it is impossible to follow the dependency relationships and wind up back at that component. This structure has no cycles. It is a _directed acyclic graph_ (DAG).

![Figure 14.1 Typical component diagram](./assets/figure14.1.jpg)

Figure 14.1 Typical component diagram

When `Main` is released, it has utterly no effect on any of the other components in the system... ...This is nice... ...the impact of releasing `Main` is relatively small.

When the developers working on the `Presenters` would like to run a test... ...just need to build... ...the versions of the `Interactors` and `Entities` components that they are currently using... ...This is nice... ...little work to do to set up a test, and... ...few variables to consider.

To release the whole system, the process proceeds from the bottom up... ...This process is very clear and easy to deal with... ...because we understand the dependencies between its parts.

#### The Effect of a Cycle in the Component Dependency Graph

Let’s say that the `User` class in `Entities` uses the `Permissions` class in `Authorizer`. This creates a dependency cycle, as shown in Figure 14.2... ...This makes `Database` much more difficult to release. `Entities`, `Authorizer`, and `Interactors` have, in effect, become one large component... ...developers working on any of those components will experience the dreaded "morning after syndrome."

![Figure 14.2 A dependency cycle](./assets/figure14.2.jpg)

Figure 14.2 A dependency cycle

When we want to test the `Entities` component... ...we must build and integrate with `Authorizer` and `Interactors`. This level of coupling between components is troubling, if not intolerable.

Cycles in the dependency graph... ...make it very difficult to isolate components. Unit testing and releasing become very difficult and error prone. In addition, build issues grow geometrically with the number of modules.

When there are cycles in the dependency graph, it can be very difficult to work out the order in which you must build the components. Indeed, there probably is no correct order.

#### Breaking the Cycle

It is always possible to break a cycle of components and reinstate the dependency graph as a DAG... ...two primary mechanisms

1. Apply the Dependency Inversion Principle (DIP)... ...in Figure 14.3... ...create an interface that has the methods that `User` needs... ...then put that interface into `Entities` and inherit it into `Authorizer`. This inverts the dependency between `Entities` and `Authorizer`, thereby breaking the cycle.

![Figure 14.3 Inverting the dependency between Entities and Authorizer](./assets/figure14.3.jpg)

Figure 14.3 Inverting the dependency between `Entities` and `Authorizer`

2. Create a new component that both `Entities` and `Authorizer` depend on... ...(Figure 14.4).

![Figure 14.4 The new component that both Entities and Authorizer depend on](./assets/figure14.4.jpg)

Figure 14.4 The new component that both `Entities` and `Authorizer` depend on

#### The "Jitters"

The second solution implies that the component structure is volatile in the presence of changing requirements... ...When cycles occur, they must be broken somehow. Sometimes this will mean creating new components, making the dependency structure grow.

### Top-Down Design

The component structure cannot be designed from the top down. It is not one of the first things about the system that is designed, but rather evolves as the system grows and changes.

We have come to expect that large-grained decompositions, like components, will also be high- level _functional_ decompositions... ...we believe that the components ought to somehow represent the functions of the system. Yet this does not seem to be an attribute of component dependency diagrams.

Component dependency diagrams have very little do to with describing the function of the application. Instead, they are a map to the _buildability_ and _maintainability_ of the application... ...they aren’t designed at the beginning of the project. There is no software to build or maintain, so there is no need for a build and maintenance map.

As more and more modules accumulate in the early stages of implementation and design, there is a growing need to manage the dependencies so that the project can be developed without the "morning after syndrome."

So we start paying attention to the SRP and CCP and collocate classes that are likely to change together.

One of the overriding concerns with this dependency structure is the isolation of volatility. We don’t want components that change frequently and for capricious reasons to affect components that otherwise ought to be stable... ...Consequently, the component dependency graph is created and molded by architects to protect stable high- value components from volatile components.

As the application continues to grow, we start to become concerned about creating reusable elements... ...the CRP begins to influence the composition of the components. Finally, as cycles appear, the ADP is applied and the component dependency graph jitters and grows.

If we tried to design the component dependency structure before we designed any classes, we would likely fail rather badly. We would not know much about common closure, we would be unaware of any reusable elements, and we would almost certainly create components that produced dependency cycles.

The component dependency structure grows and evolves with the logical design of the system.

### The Stable Dependencies Principle

_Depend in the direction of stability._

Designs cannot be completely static. Some volatility is necessary if the design is to be maintained.

By conforming to the Common Closure Principle (CCP), we create components that... ...are _designed_ to be volatile. We _expect_ them to change.

Any component... ...volatile should not be depended on by a component that is difficult to change. Otherwise... ...will also be difficult to change.

By conforming to the Stable Dependencies Principle (SDP), we ensure that modules that are intended to be easy to change are not depended on by modules that are harder to change.

#### Stability

What is meant by "stability"? Stand a penny on its side. Is it stable in that position? You would likely say "no." However, unless disturbed, it will remain in that position for a very long time.

Stability has nothing directly to do with frequency of change.

Stability is related to the amount of work required to make a change.

One sure way to make a software component difficult to change, is to make lots of other software components depend on it.

in Figure 14.5 `X` is a stable component. Three components depend on `X`, so it has three good reasons not to change... ...`X` is _responsible_ to those three components. Conversely, `X` depends on nothing, so it has no external influence to make it change. We say it is _independent._

![Figure 14.5 X: a stable component](./assets/figure14.5.jpg)

Figure 14.5 `X`: a stable component

Figure 14.6 `Y` is a very unstable component. No other components depend on Y, so we say that it is irresponsible. Y also has three components that it depends on, so changes may come from three external sources. We say that Y is dependent.

![Figure 14.6 Y: a very unstable component](./assets/figure14.6.jpg)

Figure 14.6 `Y`: a very unstable component

#### Stability Metrics

Stability of a component... ...number of dependencies that enter and leave that component... ...to calculate the `positional` stability of the component.

- _Fan-in:_ Incoming dependencies... ...number of classes outside this component that depend on classes within the component.
- _Fan-out:_ Outgoing depenencies... ...number of classes inside this component that depend on classes outside the component.
- _I: Instability: I = Fan-out , (Fan-in + Fan-out)_... ...range [0, 1]. _I_ = 0... ...maximally stable. _I_ = 1 indicates a maximally unstable.

![Figure 14.7 Our example](./assets/figure14.7.jpg)

Figure 14.7 Our example

Example in Figure 14.7... ...stability of the component `Cc`... ...three classes... ...depend on classes in `Cc`. Thus, _Fan-in_ = 3... ...one class outside _Cc_ that classes in `Cc` depend on. Thus, _Fan-out_ = 1 and _I_ = 1/4.

The _I_ metric is easiest to calculate when you have organized your source code such that there is one class in each source file.

When the _I_ is equal to 1... ...and this component depends on other components (_Fan-out_ > 0)

When the _I_ is equal to 1... ...and this component depends on other components (Fan-out > 0)... ...This... ...component... ...is irresponsible and dependent. Its lack of dependents gives the component no reason not to change, and the components that it depends on may give it ample reason to change. In contrast, when the _I_ is equal to 0... ...is _responsible_ and _independent._ It is as stable as it can get. Its dependents make it hard to change the component, and its has no dependencies that might force it to change.

The SDP says that the _I_ metric of a component should be larger than the _I_ metrics of the components that it depends on. That is, _I_ metrics should _decrease_ in the direction of dependency.

#### Not All Components Should Be Stable

If all the components in a system were maximally stable, the system would be unchangeable.

We want... ...our component structure so that some components are unstable and some are stable.

Putting the unstable components at the top... ...is a useful convention because any arrow that points _up_ is violating the SDP (and, as we shall see later, the ADP).

![Figure 14.8 An ideal configuration for a system with three components](./assets/figure14.8.jpg)

Figure 14.8 An ideal configuration for a system with three components

![Figure 14.9 SDP violation](./assets/figure14.9.jpg)

Figure 14.9 SDP violation

The diagram in Figure 14.9 shows how the SDP can be violated. `Flexible`is... ...designed to be easy to change. We want `Flexible` to be unstable... ...a dependency on `Flexible`... ...violates the SDP because the _I_ metric for `Stable` is much smaller than the _I_ metric for `Flexible`... ...A change to `Flexible` will force us to deal with `Stable` and all its dependents.

![Figure 14.10 U within Stable uses C within Flexible](./assets/figure14.10.jpg)

Figure 14.10 `U` within `Stable` uses `C` within `Flexible`

Let’s assume... ...(Figure 14.10)... ...We can fix this by employing the DIP... ...in Figure 14.11. This breaks the dependency of `Stable` on `Flexible`, and forces both components to depend on `UServer`. `UServer` is very stable (_I_ = 0), and `Flexible` retains its necessary instability (_I_ = 1). All the dependencies now flow in the direction of _decreasing_ I.

![Figure 14.11 C implements the interface class US](./assets/figure14.11.jpg)

Figure 14.11 `C` implements the interface class `US`

#### Abstract Components

Create a component... ...that contains nothing but an interface... ...is a very common, and necessary, tactic when using statically typed languages... ...These abstract components are very stable and, therefore, are ideal targets for less stable components to depend on.

Dynamically typed languages... ...abstract components don’t exist at all, nor do the dependencies that would have targeted them... ...dependency inversion does not require either the declaration or the inheritance of interfaces.

### The Stable Abstractions Principle

_A component should be as abstract as it is stable._

#### Where Do We Put the High-Level Policy?

The software that encapsulates the high-level policies of the system should be placed into stable components (_I_ = 0). Unstable components (_I_ = 1) should contain only the software that is volatile... ...However, if the high-level policies are placed into stable components, then the source code that represents those policies will be difficult to change. This could make the overall architecture inflexible. How can a component that is maximally stable (_I_ = 0) be flexible enough to withstand change?... ...OCP tells us that it is possible and desirable to create classes that are flexible enough to be extended without requiring modification... ..._Abstract classes._

#### Introducing the Stable Abstractions Principle

The Stable Abstractions Principle (SAP) sets up a relationship between stability and abstractness. On the one hand, it says that a stable component should also be abstract so that its stability does not prevent it from being extended. On the other hand, it says that an unstable component should
be concrete since it its instability allows the concrete code within it to be easily changed.

If a component is to be stable... ...consist of interfaces and abstract classes so that it can be extended.

Stable components that are extensible are flexible and do not overly constrain the architecture.

The SDP says that dependencies should run in the direction of stability, and the SAP says that stability implies abstraction. Thus _dependencies run in the direction of abstraction._

The DIP... ...deals with classes... ...Either a class is abstract or it is not. The combination of the SDP and the SAP deals with components, and... ...a component can be partially abstract and partially stable.

#### Measuring Abstraction

The _A_ metric is a measure of the abstractness of a component... ...ratio of interfaces and abstract classes... ...to the total number of classes in the component.
- _Nc:_ The number of classes in the component.
- _Na:_ The number of abstract classes and interfaces in the component.
- _A:_ Abstractness. _A = Na ÷ Nc._

The _A_ metric ranges from 0 to 1... ...0 no abstract classes... ...1 nothing but abstract classes.

#### The Main Sequence

Relationship between stability _(I)_ and abstractness _(A)_... ...(Figure 14.12)... ...components that are maximally stable and abstract at the upper left at (0, 1). Components that are maximally unstable and concrete are at the lower right at (1, 0).

![Figure 14.12 The I/A graph](./assets/figure14.12.jpg)

Figure 14.12 The I/A graph

There is a locus of points on the _A/I_ graph that defines reasonable positions for components... ...by finding the areas where components should _not_ be... ...determining the zones of _exclusion_ (Figure 11.13).

![Figure 14.13 Zones of exclusion](./assets/figure14.13.jpg)

Figure 14.13 Zones of exclusion

#### The Zone of Pain

A component is not desirable because it is rigid. It cannot be extended because it is not abstract, and it is very difficult to change because of its stability.

Within the Zone of Pain. An example... ...Database schemas are notoriously volatile, extremely concrete, and highly depended on... ...the interface between OO applications and databases is so difficult to manage... ...schema updates are generally painful.

Although a library has an _I_ metric of 1, it may actually be nonvolatile... ...Nonvolatile components are harmless in the (0, 0) zone since they are not likely to be changed... ...only volatile components are problematic in the Zone of Pain.

The more volatile a component in the Zone of Pain, the more "painful" it is. Indeed, we might consider volatility to be a third axis of the graph... ...Figure 14.13 shows only the most painful plane, where volatility = 1.

#### The Zone of Uselessness

A component near (1, 1)... ...is undesirable because it is maximally abstract, yet has no dependents.

Leftover abstract classes that no one ever implemented... ...sitting in the code base, unused. A component... ...deep within the Zone of Uselessness must contain a significant fraction of such entities... ...the presence of such useless entities is undesirable.

#### Avoiding the Zones of Exclusion

 our most volatile components should be kept as far from both zones of exclusion as possible. The locus of points that are maximally distant from each zone is the line that connects (1, 0) and (0, 1)... ...the _Main Sequence._
 
A component that sits on the Main Sequence is not "too abstract" for its stability, nor is it "too unstable" for its abstractness. It is neither useless nor particularly painful. It is depended on to the extent that it is abstract, and it depends on others to the extent that it is concrete.

The most desirable position for a component is at one of the two endpoints of the Main Sequence... ...However... ...some... ...components... ...are neither perfectly abstract nor perfectly stable... ...have the best characteristics if they are on, _or close,_ to the Main Sequence.

#### Distance from the Main Sequence

D^3: Distance. _D = |A+I-1|_ . The range is [0, 1]... ...0 the component is directly on the Main Sequence... ...1 the component is as far away as possible from the Main Sequence.

A design can be analyzed for its overall conformance to the Main Sequence... ...Any component that has a _D_ value that is not near zero can be reexamined and restructured.

We can calculate the mean and variance of all the _D_ metrics for the components within a design. We would expect... ...that are close to zero. The variance can be used to establish "control limits" so as to identify components that are "exceptional" in comparison to all the others.

Figure 14.14... ...the bulk... ...along the Main Sequence, but some are more than one standard deviation (Z = 1) away. These are worth examining more closely... ...they are either very abstract... ...or very concrete. 

![Figure 14.14 Scatterplot of the components](./assets/figure14.14.jpg)

Figure 14.14 Scatterplot of the components

Plot the _D_ metric of each component over time... ...Figure 14.15... ...plot shows a control threshold at _D_ = 0.1. The R2.1 point has exceeded this control limit, so it would be worth... ...to find out why this component is so far from the main sequence.

![Figure 14.15 Plot of D for a single component over time](./assets/figure14.15.jpg)

Figure 14.15 Plot of _D_ for a single component over time

### Conclusion

The _dependency management metrics_... ...are... ...not a god; it is merely a measurement against an arbitrary standard.

## PART V Architecture

## Chapter 15 What Is Architecture?

A software architect is a programmer; and continues to be a programmer... ...They do not! Software architects are the best programmers, and they continue to take programming tasks, while they also guide the rest of the team toward a design that maximizes productivity.

They cannot do their jobs properly if they are not experiencing the problems that they are creating for the rest.

The architecture of a software system is the shape given to that system by those who build it... ...to facilitate the development, deployment, operation, and maintenance of the software system contained within it. _The strategy behind that is to leave as many options open as possible, for as long as possible._

The architecture of a system has very little bearing on whether that system works... ...rather in their deployment, maintenance, and ongoing development.

Architecture... ...role is passive and cosmetic, not active or essential.

There are few, if any, _behavioral_ options that the architecture of a system can leave open.

The primary purpose of architecture is to support the life cycle of the system.

Good architecture makes the system easy to understand, easy to develop, easy to maintain, and easy to deploy.

The ultimate goal is to minimize the lifetime cost of the system and to maximize programmer productivity.

### Development

A software system that is hard to develop is not likely to have a long and healthy lifetime.

Architecture of a system should make that system easy to develop.

The reason why so many systems lack good architecture: They were begun with none, because the team was small and did not want the impediment of a superstructure.

A component-per-team architecture is not likely to be the best architecture for deployment, operation, and maintenance of the system. Nevertheless, it is the architecture that a group of teams will gravitate toward if they are driven solely by development schedule.

### Deployment

To be effective, a software system must be deployable.

The higher the cost of deployment, the less useful the system is.

A goal of a software architecture... ...to make a system that can be easily deployed _with a single action._

Deployment strategy is seldom considered during initial development. This leads to architectures that may make the system easy to develop, but leave it very difficult to deploy.

### Operation

The impact of architecture on system operation tends to be less dramatic than the impact of architecture on development, deployment, and maintenance.

Almost any operational difficulty can be resolved by throwing more hardware at the system without drastically impacting the software architecture.

The fact that hardware is cheap and people are expensive means that architectures that impede operation are not as costly as architectures that impede development, deployment, and maintenance.

A good software architecture communicates the operational needs of the system.

Architecture should reveal operation... ...elevate the use cases, the features, and the required behaviors of the system to first-class entities... ...This simplifies the understanding of the system and, therefore, greatly aids in development and maintenance.

### Maintenance

Of all the aspects of a software system, maintenance is the most costly.

The primary cost of maintenance is in _spelunking_ and risk. Spelunking is the cost of digging through the existing software, trying to determine the best place and the best strategy to add a new feature or to repair a defect. While making such changes, the likelihood of creating inadvertent defects is always there, adding to the cost of risk.

By separating the system into components, and isolating those components through stable interfaces, it is possible to illuminate the pathways for future features and greatly reduce the risk of inadvertent breakage.

### Keeping Options Open

Software has two types of value: the value of its behavior and the value of its structure. The second of these is the greater of the two because it is this value that makes software _soft._

Software was invented because we needed a way to quickly and easily change the behavior of machines.

The way you keep software soft is to leave as many options open as possible, for as long as possible.

The options that we need to leave open _are the details that don’t matter._

All software systems... ...two major elements: policy and details. The policy element embodies all the business rules and procedures... ...where the true value of the system lives. The details are those things that are necessary to enable humans, other systems, and programmers to communicate with the policy, but that do not impact the behavior of the policy at all. They include IO devices, databases, web systems, servers, frameworks, communication protocols, and so forth.

The goal... ...is to create a shape for the system that recognizes policy as the most essential element of the system while making the details _irrelevant_ to that policy. This allows decisions about those details to be _delayed_ and _deferred._

The high-level policy should not care which kind of database will be used.

It is not necessary to choose a web server early in development, because the high-level policy should not know that it is being delivered over the web... ...Indeed, _you don’t even have to decide if the system will be delivered over the web._

It is not necessary to adopt REST early in development, because the high- level policy should be agnostic about the interface to the outside world.

It is not necessary to adopt a dependency injection framework... ...because the high-level policy should not care how dependencies are resolved.

If you can develop the high-level policy without committing to the details that surround it, you can delay and defer decisions about those details for a long time. And the longer you wait to make those decisions, _the more information you have with which to make them properly._

This also leaves you the option to try different experiments. If you have a portion of the high-level policy working, and it is agnostic about the database, you could try connecting it to several different databases to check applicability and performance. 

The longer you leave options open... ...the more things you can try, and the more information you will have when you reach the point at which those decisions can no longer be deferred.

If the decisions have already been made by someone else... ..._A good architect pretends that the decision has not been made,_ and shapes the system such that those decisions can still be deferred or changed.

_A good architect maximizes the number of decisions not made._

### Device Independence

1960s... ...One mistake was to bind our code directly to the IO devices... ...Our code was _device dependent_... ...all our software was written to manipulate card readers and card punches. Those programs had to be rewritten to use magnetic tape. That was a big job. By the late 1960s, we had learned our lesson—and we invented _device independence._

Programs would invoke operating system services that dealt with abstract unit-record devices... ...the same program could read and write cards, or read and write tape, _without any change._ The Open–Closed Principle was born (but not yet named).

### Junk Mail

In the late 1960s, I worked for a company that printed junk mail for clients. The clients would send us magnetic tapes with unit records containing the names and addresses of their customers, and we would write programs that printed nice personalized advertisements... ...The value of device independence was enormous! We could write our programs without knowing or caring which device would be used. We could test those programs using the local line printer connected to the computer. Then we could tell the operating system to “print” to magnetic tape and run off hundreds of thousands of forms. Our programs had a shape. That shape disconnected policy from detail. The policy was the formatting of the name and address records. The detail was the device. We deferred the decision about which device we would use.

### Physical Addressing

We changed the high-level policy of the system to be agnostic about the physical structure of the disk. That allowed us to decouple the decision about disk drive structure from the application.

### Conclusion

Good architects carefully separate details from policy, and then decouple the policy from the details so thoroughly that the policy has no knowledge of the details and does not depend on the details in any way.

Good architects design the policy so that decisions about the details can be delayed and deferred for as long as possible.

## Chapter 16 Independence

A good architecture must support:
- The use cases and operation of the system.
- The maintenance of the system.
- The development of the system.
- The deployment of the system.

### Use Cases

Use cases—means that the architecture of the system must support the intent of the system.

The first concern of the architect, and the first priority of the architecture. The architecture must support the use cases.

Architecture does not wield much influence over the behavior of the system.

The most important thing a good architecture can do to support behavior is to clarify and expose that behavior so that the intent of the system is visible at the architectural level.

Behaviors will be first-class elements visible at the top level of the system... ...and they will have names that clearly describe their function.

### Operation

Architecture plays a more substantial, and less cosmetic, role in supporting the operation of the system

If the system must handle 100,000 customers per second, the architecture must support that kind of throughput and response time for each use case that demands it.

This decision is one of the options that a good architect leaves open.

Monolithic structure, cannot easily be upgraded to multiple processes... ...By comparison, an architecture that maintains the proper isolation of its components, and does not assume the means of communication between those components, will be much easier to transition... ...as the operational needs of the system change over time.

### Development

Architecture plays a significant role in supporting the development environment.

> Any organization that designs a system will produce a design whose structure is a copy of the organization’s communication structure.
> — Conway’s law.

A system that must be developed by an organization with many teams and many concerns must have an architecture that facilitates independent actions by those teams, so that the teams do not interfere with each other during development.

Partitioning the system into well-isolated, independently developable components... ...allocated to teams that can work independently of each other.

### Deployment

The goal is "immediate deployment."

A good architecture helps the system to be immediately deployable after build.

Achieved through the proper partitioning and isolation of the components of the system.

### Leaving Options Open

A good architecture balances all of these concerns with a component structure that mutually satisfies them all... ...The reality is that achieving this balance is pretty hard.

The problem is that most of the time we don’t know what all the use cases are, nor do we know the operational constraints, the team structure, or the deployment requirements. Worse, even if we did know them, they will inevitably change as the system moves through its life cycle. In short, the goals we must meet are indistinct and inconstant. Welcome to the real world.

Some principles of architecture are relatively inexpensive to implement and can help balance those concerns.

Partition our systems into well-isolated components that allow us to leave as many options open as possible, for as long as possible.

A good architecture makes the system easy to change, in all the ways that it must change, by leaving options open.

### Decoupling Layers

The architect wants the structure of the system to support all the necessary use cases, but does not know what all those use cases are. However, the architect _does_ know the basic intent of the system... ...So the architect can employ the Single Responsibility Principle and the Common Closure Principle to separate those things that change for different reasons, and to collect those things that change for the same reasons—given the context of the intent of the system.

Separate the UI portions of a use case from the business rule portions in such a way that they can be changed independently of each other, while keeping those use cases visible and clear.

The database, the query language, and even the schema are technical details that have nothing to do with the business rules or the UI. They will change at rates, and for reasons, that are independent of other aspects of the system. Consequently, the architecture should separate them from the rest of the system so that they can be independently changed.

System divided into decoupled horizontal layers—the UI, application-specific business rules, application-independent business rules, and the database, just to mention a few.

### Decoupling Use Cases

What else changes for different reasons? The use cases themselves!... ...Use cases are a very natural way to divide the system.

Use cases are narrow vertical slices that cut through the horizontal layers of the system. Each use case uses some UI, some application-specific business rules, some application-independent business rules, and some database functionality... ...dividing the system into thin vertical use cases that cut through those layers.

If you decouple the elements of the system that change for different reasons, then you can continue to add new use cases without interfering with old ones.

If each use case uses a different aspect of the UI and database, then adding new use cases will be unlikely to affect older ones.

### Decoupling Mode

If the different aspects of the use cases are separated, then those that must run at a high throughput are likely already separated from those that must run at a low throughput... ...Those that require higher bandwidth can be replicated in many servers.

The decoupling that we did for the sake of the use cases also helps with operations.

To take advantage of the operational benefit, the decoupling must have the appropriate mode... ...components cannot depend on being together in the same address space of a processor. They must be independent services, which communicate over a network.

An architecture based on services is often called a service-oriented architecture... ...sometimes we have to separate our components all the way to the service level.

I’m not going to tell you that SoA is the best possible architecture, or that micro- services are the wave of the future.

A good architecture leaves options open. _The decoupling mode is one of those options._

### Independent Develop-ability

When components are strongly decoupled, the interference between teams is mitigated.

If the business rules don’t know about the UI, then a team that focuses on the UI cannot much affect a team that focuses on the business rules. If the use cases themselves are decoupled from one another, then a team that focuses on the `addOrder` use case is not likely to interfere with a team that focuses on the `deleteOrder` use case.

So long as the layers and use cases are decoupled, the architecture of the system will support the organization of the teams

### Independent Deployability

The decoupling of the use cases and layers also affords a high degree of flexibility in deployment.

If the decoupling is done well, then it should be possible to hot-swap layers and use cases in running systems.

### Duplication

Duplication is generally a bad thing in software. We don’t like duplicated code. When code is truly duplicated, we are honor-bound as professionals to reduce and eliminate it.

There are different kinds of duplication. There is true duplication, in which every change to one instance necessitates the same change to every duplicate of that instance. Then there is false or accidental duplication. If two apparently duplicated sections of code evolve along different paths—if they change at different rates, and for different reasons—_then they are not true duplicates._

Imagine two use cases that have very similar screen structures. The architects will be tempted to share the code for that structure... ...Most likely it is accidental. As time goes by, the odds are that those two screens will diverge and eventually look very different. For this reason... ...avoid unifying them. Otherwise, separating them later will be a challenge.

When you are vertically separating use cases from one another... ...your temptation will be to couple the use cases because they have similar screen structures, or similar algorithms, or similar database queries and/or schemas. Be careful. Resist the temptation to commit the sin of knee-jerk elimination of duplication. Make sure the duplication is real.

### Decoupling Modes (Again)

Ways to decouple layers and use cases... ...at the source code level, at the binary code (deployment) level, and at the execution unit (service) level.

- **Source level.** We can control the dependencies between source code modules so that changes to one module do not force changes or recompilation of others... ...the components all execute in the same address space, and communicate with each other using simple function calls... ...monolithic structure.
- **Deployment level.** We can control the dependencies between deployable units... ...so that changes to the source code in one module do not force others to be rebuilt and redeployed.
- **Service level.** We can reduce the dependencies down to the level of data structures, and communicate solely through network packets such that every execution unit is entirely independent of source and binary changes to others... ...services or micro-services.

It’s hard to know which mode is best during the early phases of a project. Indeed, as the project matures, the optimal mode may change.

One solution... ...is to simply decouple at the service level by default. A problem... ...is that it is expensive and encourages coarse-grained decoupling. No matter how "micro" the micro-services get, the decoupling is not likely to be fine-grained enough.

Service-level decoupling is expensive, both in development time and in system resources. Dealing with service boundaries where none are needed is a waste of effort, memory, and cycles... ...the last two are cheap—but the first is not.

Push the decoupling to the point where a service _could_ be formed. should it become necessary; but then to leave the components in the same address space as long as possible. This leaves the option for a service open.

If deployment or development issues arise, driving some of the decoupling to a deployment level may be sufficient—at least for a while.

As the development, deployment, and operational issues increase, carefully choose which deployable units to turn into services, and gradually shift the system in that direction.

Over time, the operational needs of the system may decline. What once required decoupling at the service level may now require only deployment-level or even source-level decoupling.

A good architecture will allow a system to be born as a monolith, deployed in a single file, but then to grow into a set of independently deployable units, and then all the way to independent services and/or micro-services. Later, as things change, it should allow for reversing that progression and sliding all the way back down into a monolith.

A good architecture protects the majority of the source code from changes. It leaves the decoupling mode open as an option so that large deployments can use one mode, whereas small deployments can use another.

### Conclusion

The decoupling mode of a system is one of those things that is likely to change with time, and a good architect foresees and _appropriately_ facilitates those changes.

## Chapter 17 Boundaries: Drawing Lines

Software architecture is the art of drawing lines... ..._boundaries_... ...separate software elements from one another, and restrict those on one side from knowing about those on the other.

Those that are drawn early are drawn for the purposes of deferring decisions for as long as possible, and of keeping those decisions from polluting the core business logic.

The goal of an architect is to minimize the human resources required to build and maintain the required system.

What saps people-power? _Coupling_—and especially coupling to premature decisions.

Which kinds of decisions are premature? Decisions that have nothing to do with the business requirements—the use cases—of the system... ...frameworks, databases, web servers... ...and the like.

A good system architecture is one in which decisions like these are rendered ancillary and deferrable... ...does not depend on those decisions...allows those decisions to be made at the latest possible moment, without significant impact.

### A Couple of Sad Stories

The architects, by making a premature decision, multiplied the development effort enormously.

There’s nothing intrinsically wrong with a software system that is structured around services. The error at W was the premature adoption and enforcement of a suite of tools that promised SoA—that is, the premature adoption of a massive suite of domain object services. The cost of those errors was sheer person-hours—person-hours in droves—flushed down the SoA vortex.

### FitNesse

Anything produced should not require people to download more than one file. I called this rule, "Download and Go."

A bare-bones web server is a very simple piece of software to write and it allowed us to postpone any web framework decision until much later.

Early in the development of `FitNesse`, we drew a _boundary line_ between business rules and databases. That line prevented the business rules from knowing anything at all about the database, other than the simple data access methods. That decision allowed us to defer the choice and implementation of the database for well over a year. It allowed us to try the file system option, and it allowed us to change direction when we saw a better solution. Yet it did not prevent, or even impede, moving in the original direction (MySQL) when someone wanted it.

The fact that we did not have a database running for 18 months of development meant that, for 18 months, we did not have schema issues, query issues, database server issues, password issues, connection time issues, and all the other nasty issues that raise their ugly heads when you fire up a database. It also meant that all our tests ran fast, because there was no database to slow them down.

In short, drawing the boundary lines helped us delay and defer decisions, and it ultimately saved us an enormous amount of time and headaches. And that’s what a good architecture should do.

### Which Lines Do You Draw, and When Do You Draw Them?

You draw lines between things that matter and things that don’t.

The GUI doesn’t matter to the business rules, so there should be a line between them. The database doesn’t matter to the GUI, so there should be a line between them. The database doesn’t matter to the business rules, so there should be a line between them.

Many of us have been taught to believe that the database is inextricably connected to the business rules... ... but... ...this idea is misguided. The database is a tool that the business rules can use _indirectly._

All the business rules need to know is that there is a set of functions that can be used to fetch or save data. This allows us to put the database behind an interface.

![Figure 17.1 The database behind an interface](./assets/figure17.1.jpg)

Figure 17.1 The database behind an interface

The boundary is drawn across the inheritance relationship, just below the `DatabaseInterface` (Figure 17.2).

![Figure 17.2 The boundary line](./assets/figure17.2.jpg)

Figure 17.2 The boundary line

Note the two arrows leaving the `DatabaseAccess` class. Those two arrows point away from the `DatabaseAccess` class. That means that none of these classes knows that the `DatabaseAccess` class exists.

We’ll look at the component that contains many business rules, and the component that contains the database and all its access classes (Figure 17.3). Note the direction of the arrow. The `Database` knows about the `BusinessRules`. The `BusinessRules` do not know about the `Database`. This implies that the `DatabaseInterface` classes live in the `BusinessRules` component, while the `DatabaseAccess` classes live in the `Database` component.
The direction of this line is important. It shows that the `Database` does not matter to the `BusinessRules`, but the `Database` cannot exist without the `BusinessRules`.

![Figure 17.3 The business rules and database components](./assets/figure17.3.jpg)

Figure 17.3 The business rules and database components

The `Database` component contains the code that translates the calls made by the `BusinessRules` into the query language of the database. It is that translation code that knows about the `BusinessRules`.

Having drawn this boundary line... ...we can now see that the `BusinessRules` could use _any_ kind of database. The `Database` component could be replaced with many different implementations—the `BusinessRules` don’t care... ...database decision can be deferred and you can focus on getting the business rules written and tested before you have to make the database decision.

### What About Input and Output?

Developers and customers often get confused about what the system is. They... ...think that the GUI is the system. They define a system in terms of the GUI, so they believe that they should see the GUI start working immediately. They fail to realize a critically important principle: _The IO is irrelevant._

`GUI` and `BusinessRules` components separated by a boundary line (Figure 17.4)... ...the less relevant component depends on the more relevant component. The arrows show which component knows about the other... ...The `GUI` cares about the `BusinessRules`.

![Figure 17.4 The boundary between GUI and BusinessRules components](./assets/figure17.4.jpg)

Figure 17.4 The boundary between `GUI` and `BusinessRules` components

The `GUI` could be replaced with any other kind of interface—and the `BusinessRules` would not care.

### Plugin Architecture

The history of software development technology is the story of how to conveniently create plugins to establish a scalable and maintainable system architecture.

The core business rules are kept separate from, and independent of, those components that are either optional or that can be implemented in many different forms (Figure 17.5).

![Figure 17.5 Plugging in to the business rules](./assets/figure17.5.jpg)

Figure 17.5 Plugging in to the business rules

The database. Since we have chosen to treat it as a plugin, we can replace it with any... ...other kind of database technology we might deem necessary in the future.

By starting with the presumption of a plugin structure, we have at very least made such a change practical.

### The Plugin Argument

Relationship between ReSharper and Visual Studio... ...there is nothing that the ReSharper team can do to disturb the Visual Studio team. But the Visual Studio team could completely disable the ReSharper team if they so desired.

![Figure 17.6 ReSharper depends on Visual Studio](./assets/figure17.6.jpg)

Figure 17.6 ReSharper depends on Visual Studio

We want certain modules to be immune to others.

We don’t want the business rules to break when someone changes the format of a web page.

We don’t want changes in one part of the system to cause other unrelated parts of the system to break. We don’t want our systems to exhibit that kind of fragility.

Arranging our systems into a plugin architecture creates firewalls across which changes cannot propagate.

If the GUI plugs in to the business rules, then changes in the GUI cannot affect those business rules.

Boundaries are drawn where there is an _axis of change._ The components on one side of the boundary change at different rates, and for different reasons, than the components on the other side of the boundary.

GUIs change at different times and at different rates than business rules, so there should be a boundary between them.

This is simply the Single Responsibility Principle again. The SRP tells us where to draw our boundaries.

### Conclusion

To draw boundary lines in a software architecture, you first partition the system into components... ...Then you arrange the code in those components such that the arrows between them point in one direction—toward the core business.

Recognize this as an application of the Dependency Inversion Principle and the Stable Abstractions Principle. Dependency arrows are arranged to point from lower-level details to higher-level abstractions.

## Chapter 18 Boundary Anatomy

The architecture of a system is defined by a set of software components and the boundaries that separate them.

### Boundary Crossing

At runtime, a boundary crossing is nothing more than a function on one side of the boundary calling a function on the other side and passing along some data. The trick to creating an appropriate boundary crossing is to manage the source code dependencies... ...Because when one source code module changes, other source code modules may have to be changed or recompiled, and then redeployed. Managing and building firewalls against this change is what boundaries are all about.

### The Dreaded Monolith

The simplest and most common of the architectural boundaries has no strict physical representation.

The fact that the boundaries are not visible during the deployment of a monolith does not mean that they are not present and meaningful.

Even when statically linked into a single executable, the ability to independently develop and marshal the various components for final assembly is immensely valuable.

Dynamic polymorphism to manage their internal dependencies.

Static polymorphism (e.g., generics or templates) can sometimes be a viable means of dependency manage- ment in monolithic systems, especially in languages like C++. However, the decoupling afforded by generics cannot protect you from the need for recompilation and redeployment the way dynamic polymorphism can.

Without OO, or an equivalent form of polymorphism, architects must fall back on the dangerous practice of using pointers to functions to achieve the appropriate decoupling.

The simplest possible boundary crossing is a function call from a low-level client to a higher-level service. Both the runtime dependency and the compile-time dependency point in the same direction, toward the higher-level component.

In Figure 18.1, the flow of control crosses the boundary from left to right. The `Client` calls function `f()` on the `Service`. It passes along an instance of `Data`. The `<DS>` marker simply indicates a data structure. The `Data` may be passed as a function argument or by some other more elaborate means. Note that the definition of the `Data` is on the _called_ side of the boundary.

![Figure 18.1 Flow of control crosses the boundary from a lower level to a higher level](./assets/figure18.1.jpg)

Figure 18.1 Flow of control crosses the boundary from a lower level to a higher level

When a high-level client needs to invoke a lower-level service, dynamic polymorphism is used to invert the dependency against the flow of control. The runtime dependency opposes the compile-time dependency. In Figure 18.2, the flow of control crosses the boundary from left to right as before. The high-level `Client` calls the `f()` function of the lower-level `ServiceImpl` through the `Service` interface. Note, however, that all dependencies cross the boundary from right to left _toward the higher-level component._ Note, also, that the definition of the data structure is on the calling side of the boundary.

![Figure 18.2 Crossing the boundary against the flow of control](./assets/figure18.2.jpg)

Figure 18.2 Crossing the boundary against the flow of control

Even in a monolithic, statically linked executable, this kind of disciplined partitioning can greatly aid the job of developing, testing, and deploying the project.

High-level components remain independent of lower-level details.

Communications between components in a monolith are very fast and inexpensive.

Since the deployment of monoliths usually requires compilation and static linking, components in these systems are typically delivered as source code.

### Deployment Components

The simplest physical representation of an architectural boundary is a dynamically linked library.

Deployment does not involve compilation. Instead, the components are delivered in binary, or some equivalent deployable form. This is the deployment-level decoupling mode.

Deployment-level components are the same as monoliths. The functions generally all exist in the same processor and address space. The strategies for segregating the components and managing their dependencies are the same.

As with monoliths, communications across deployment component boundaries... ...are very inexpensive.

### Threads

Both monoliths and deployment components can make use of threads... ...a way to organize the schedule and order of execution. They may be wholly contained within a component, or spread across many components.

### Local Processes

A local process is typically created from the command line or an equivalent system call. Local processes run in the same processor, or in the same set of processors within a multicore, but run in separate address spaces.

Local processes communicate with each other using sockets... ...mailboxes or message queues.

Each local process may be a statically linked monolith, or it may be composed of dynamically linked deployment components. In the former case, several monolithic processes may have the same components compiled and linked into them. In the latter, they may share the same dynamically linked deployment components.

Local process as a kind of uber-component: The process consists of lower-level components that manage their dependencies through dynamic polymorphism.

Source code dependencies point in the same direction across the boundary, and always toward the higher-level component.

The source code of the higher-level processes must not contain the names, or physical addresses, or registry lookup keys of lower-level processes.

The architectural goal is for lower-level processes to be plugins to higher-level processes.

Communication across local process boundaries... ...moderately expensive. Chattiness should be carefully limited.

### Services

The strongest boundary is a service. A service is a process, generally started from the command line or through an equivalent system call. Services do not depend on their physical location. Two communicating services may, or may not, operate in the same physical processor or multicore. The services assume that all communications take place over the network.

Communications across service boundaries are very slow compared to function calls.

Lower-level services should "plug in" to higher-level services.

### Conclusion

Most systems, other than monoliths, use more than one boundary strategy. A system that makes use of service boundaries may also have some local process boundaries.

A service is often just a facade for a set of interacting local processes.

The boundaries in a system will often be a mixture of local chatty boundaries and boundaries that are more concerned with latency.

## Chapter 19 Policy and Level

Software systems are statements of policy.

A computer program is a detailed description of the policy by which inputs are transformed into outputs.

Policy can be broken down into many different smaller statements of policy. Some... ...will describe how particular business rules are to be calculated. Others... ...how certain reports are to be formatted. Still others...how input data are to be validated.

Part of the art of developing a software architecture is carefully separating those policies from one another, and regrouping them based on the ways that they change.

Policies that change for the same reasons, and at the same times, are at the same level and belong together in the same component. Policies that change for different reasons, or at different times, are at different levels and should be separated into different components.

The art of architecture involves forming the regrouped components into a directed acyclic graph. The nodes of the graph are the components that contain policies at the same level. The directed edges are the dependencies between those components.

In a good architecture... ...low-level components are designed so that they depend on high-level components.

### Level

"Level" is "the distance from the inputs and outputs." The farther a policy is from both the inputs and the outputs of the system, the higher its level.

The policies that manage input and output are the lowest- level policies in the system.

![Figure 19.1 A simple encryption program](./assets/figure19.1.jpg)

Figure 19.1 A simple encryption program

Data flow diagram in Figure 19.1 ... ...encryption program... ...The data flows are shown as curved solid arrows. The properly designed source code dependencies are shown as straight dashed lines. The Translate component is the highest-level component in this system because it is the component that is farthest from the inputs and outputs.

The data flows and the source code dependencies do not always point in the same direction... ...We want source code dependencies to be decoupled from data flow and _coupled to level._

```
function encrypt() {
  while(true)
    writeChar(translate(readChar()));
}
```

Incorrect architecture by writing the encryption program like this... ...because the high-level `encrypt` function depends on the lower-level `readChar` and `writeChar` functions.

![Figure 19.2 Class diagram showing a better architecture for the system](./assets/figure19.2.jpg)

Figure 19.2 Class diagram showing a better architecture for the system

`ConsoleReader` and `ConsoleWriter` are classes. They are low level because they are close to the inputs and outputs.

This structure... ...makes the encryption policy usable in a wide range of contexts... ...changes made to the input and output policies are not likely to affect the encryption policy.

Policies that change for the same reasons and at the same times are grouped together by the SRP and CCP.

Higher-level policies... ...tend to change less frequently, and for more important reasons, than lower-level policies... ...those that are closest to the inputs and outputs—tend to change frequently, and with more urgency, but for less important reasons.

Keeping... ...policies separate, with all source code dependencies pointing in the direction of the higher-level policies, reduces the impact of change.

Trivial... ...hanges at the lowest levels...have little or no impact on the higher.

![Figure 19.3 Lower-level components should plug in to higher-level components](./assets/figure19.3.jpg)

Figure 19.3 Lower-level components should plug in to higher-level components

The `Encryption` component knows nothing of the `IODevices` component; the `IODevices` component depends on the `Encryption` component.

### Conclusion

This discussion of policies has involved a mixture of the Single Responsibility Principle, the Open-Closed Principle, the Common Closure Principle, the Dependency Inversion Principle, the Stable Dependencies Principle, and the Stable Abstractions Principle.

## Chapter 20 Business Rules

Strictly speaking, business rules are rules or procedures that make or save the business money... ...whether they were implemented on a computer... ...or... ...executed manually.

_Critical Business Rules_... ...critical to the business itself, and would exist even if there were no system to automate them.

Critical Business Rules usually require some data to work with... ..._Critical Business Data_... ...data that would exist even if the system were not automated.

The critical rules and critical data are inextricably bound, so they are a good candidate for an object. We’ll call this kind of object an _Entity._

### Entities

An Entity is an object within our computer system that embodies a small set of critical business rules operating on Critical Business Data. The Entity object either contains the Critical Business Data or has very easy access to that data. The interface of the Entity consists of the functions that implement the Critical Business Rules that operate on that data.

![Figure 20.1 Loan entity as a class in UML](./assets/figure20.1.jpg)

Figure 20.1 Loan entity as a class in UML

When we create this kind of class, we are gathering together the software that implements a concept that is critical to the business, and separating it from every other concern in the automated system we are building. This class stands alone as a representative of the business... ...It could serve the business in any system, irrespective of how that system was presented, or how the data was stored... ...The Entity is pure business and _nothing else._

You don’t need to use an object-oriented language to create an Entity. All that is required is that you bind the Critical Business Data and the Critical Business Rules together in a single and separate software module.

### Use Cases

Not all business rules are as pure as Entities.

Some business rules make or save money for the business by defining and constraining the way that an _automated_ system operates. These rules would not be used in a manual environment, because they make sense only as part of an automated system.

A use case is a description of the way that an automated system is used. It specifies the input to be provided by the user, the output to be returned to the user, and the processing steps involved in producing that output. A use case describes _application-specific_ business rules as opposed to the Critical Business Rules within the Entities.

![Figure 20.2 Example use case](./assets/figure20.2.jpg)

Figure 20.2 Example use case

Figure 20.2 shows an example of a use case. Notice that in the last line it mentions the Customer. This is a reference to the Customer entity, which contains the Critical Business Rules that govern the relationship between the bank and its customers.

Use cases contain the rules that specify how and when the Critical Business Rules within the Entities are invoked.

Use cases control the dance of the Entities.

The use case does not describe the user interface other than to informally specify the data coming in from that interface, and the data going back out through that interface. From the use case, it is impossible to tell whether the application is delivered on the web, or on a thick client, or on a console, or is a pure service.

Use cases do not describe how the system appears to the user. Instead, they describe the application-specific rules that govern the interaction between the users and the Entities.

How the data gets in and out of the system is irrelevant to the use cases.

A use case is an object. It has one or more functions that implement the application-specific business rules. It also has data elements that include the input data, the output data, and the references to the appropriate Entities with which it interacts.

Entities have no knowledge of the use cases that control them.

High-level concepts, such as Entities, know nothing of lower-level concepts, such as use cases.

The lower-level use cases know about the higher-level Entities.

Use cases are specific to a single application and, therefore, are closer to the inputs and outputs of that system. Entities are generalizations that can be used in many different applications, so they are farther from the inputs and outputs of the system. Use cases depend on Entities; Entities do not depend on use cases.

### Request and Response Models

Use cases expect input data, and they produce output data. However, a well- formed use case object should have no inkling about the way that data is communicated to the user, or to any other component.

The use case class accepts simple request data structures for its input, and returns simple response data structures as its output. These data structures are not dependent on anything.

This lack of dependencies is critical. If the request and response models are not independent, then the use cases that depend on them will be indirectly bound to whatever dependencies the models carry with them.

### Conclusion

Business rules are the reason a software system exists. They are the core functionality. They carry the code that makes, or saves, money. They are the family jewels.

The business rules should remain pristine, unsullied by baser concerns such as the user interface or database used.

Ideally, the code that represents the business rules should be the heart of the system, with lesser concerns being plugged in to them.

The business rules should be the most independent and reusable code in the system.

## Chapter 21 Screaming Architecture

What does the architecture of your application scream? When you look at the top-level directory structure, and the source files in the highest-level package, do they scream "Health Care System," or "Accounting System," or "Inventory Management System"? Or do they scream "Rails," or "Spring/ Hibernate," or "ASP"?

### The Theme of an Architecture

Software architectures are structures that support the use cases of the system.

Just as the plans for a house or a library scream about the use cases of those buildings, so should the architecture of a software application scream about the use cases of the application.

Architectures are not (or should not be) about frameworks.

Architectures should not be supplied by frameworks. Frameworks are tools to be used, not architectures to be conformed to. If your architecture is based on frameworks, then it cannot be based on your use cases.

### The Purpose of an Architecture

Good architectures are centered on use cases so that architects can safely describe the structures that support those use cases without committing to frameworks, tools, and environments.

The first concern of the architect is to make sure that the house is usable— not to ensure that the house is made of bricks.

A good software architecture allows decisions about frameworks, databases, web servers, and other environmental issues and tools to be deferred and delayed.

_Frameworks are options to be left open._

A good architecture emphasizes the use cases and decouples them from peripheral concerns.

### But What About the Web?

The web is a delivery mechanism—an IO device—and your application architecture should treat it as such.

The fact that your application is delivered over the web is a detail and should not dominate your system structure.

Your system architecture should be as ignorant as possible about how it will be delivered.

### Frameworks Are Tools, Not Ways of Life

Frameworks can be very powerful and very useful. Framework authors often believe very deeply in their frameworks... ...Other authors... ...show you the way to use the framework. Often they assume an all-encompassing, all-pervading, let-the-framework-do-everything position. _This is not the position you want to take._

Look at each framework with a jaded eye... ...Ask yourself how you should use it, and how you should protect yourself from it... ...Develop a strategy that prevents the framework from taking over that architecture.

### Testable Architectures

If your system architecture is all about the use cases, and if you have kept your frameworks at arm’s length, then you should be able to unit-test all those use cases without any of the frameworks in place.

Your Entity objects should be plain old objects that have no dependencies on frameworks or databases or other complications. Your use case objects should coordinate your Entity objects. Finally, all of them together should be testable in situ, without any of the complications of frameworks.

### Conclusion

Your architecture should tell readers about the system, not about the frameworks you used in your system.

New programmers should be able to learn all the use cases of the system, yet still not know how the system is delivered. They may come to you and say: "We see some things that look like models—but where are the views and controllers?" And you should respond: "Oh, those are details that needn’t concern us at the moment. We’ll decide about them later."

## Chapter 22 The Clean Architecture

Over the last several decades... ...ideas regarding the architecture of systems: 
- Hexagonal Architecture (also known as Ports and Adapters), developed by Alistair Cockburn, and adopted by Steve Freeman and Nat Pryce in their wonderful book _Growing Object Oriented Software with Tests_
- DCI from James Coplien and Trygve Reenskaug
- BCE, introduced by Ivar Jacobson 
They all have the same objective, which is the separation of concerns... ...by dividing the software into layers. Each has at least one layer for business rules, and another layer for user and system interfaces.

Each of these architectures produces systems that have the following characteristics:
- _Independent of frameworks._ The architecture does not depend on the existence of some library of feature-laden software. This allows you to use such frameworks as tools, rather than forcing you to cram your system into their limited constraints.
- _Testable._ The business rules can be tested without the UI, database, web server, or any other external element.
- _Independent of the UI._ The UI can change easily, without changing the rest of the system.
- _Independent of the database_... ...Your business rules are not bound to the database.
- _Independent of any external agency._ In fact, your business rules don’t know anything at all about the interfaces to the outside world.

![Figure 22.1 The clean architecture](./assets/figure22.1.jpg)

Figure 22.1 The clean architecture

### The Dependency Rule

The concentric circles in Figure 22.1 represent different areas of software. In general, the further in you go, the higher level the software becomes. The outer circles are mechanisms. The inner circles are policies.

The overriding rule that makes this architecture work is the _Dependency Rule: Source code dependencies must point only inward, toward higher-level policies._

Nothing in an inner circle can know anything at all about something in an outer circle.

The name of something declared in an outer circle must not be mentioned by the code in an inner circle.

Data formats declared in an outer circle should not be used by an inner circle, especially if those formats are generated by a framework in an outer circle.

#### Entities

Entities encapsulate enterprise-wide Critical Business Rules... ...can be used by many different applications in the enterprise.

If you don’t have an enterprise and are writing just a single application, then these entities are the business objects of the application. They encapsulate the most general and high-level rules.

No operational change to any particular application should affect the entity layer.

#### Use Cases

The software in the use cases layer contains _application-specific_ business rules. It encapsulates and implements all of the use cases of the system.

Use cases orchestrate the flow of data to and from the entities, and direct those entities to use their Critical Business Rules to achieve the goals of the use case.

We do not expect changes in this layer to affect the entities. We also do not expect this layer to be affected by changes to externalities... ...The use cases layer is isolated from such concerns.

We expect that changes to the operation of the application will affect the use cases and, therefore, the software in this layer. If the details of a use case change, then some code in this layer will certainly be affected.

#### Interface Adapters

The software in the interface adapters layer is a set of adapters that convert data from the format most convenient for the use cases and entities, to the format most convenient for some external agency such as the database or the web.

The models are likely just data structures that are passed from the controllers to the use cases, and then back from the use cases to the presenters and views.

Data is converted, in this layer, from the form most convenient for entities and use cases, to the form most convenient for whatever persistence framework is being used.

No code inward of this circle should know anything at all about the database.

In this layer is any other adapter necessary to convert data from some external form, such as an external service, to the internal form used by the use cases and entities.

#### Frameworks and Drivers

The outermost layer of the model in Figure 22.1 is generally composed of frameworks and tools such as the database and the web framework... ...glue code that communicates to the next circle inward.

The frameworks and drivers layer is where all the details go.

#### Only Four Circles?

There’s no rule that says you must always have just these four. However, the Dependency Rule always applies. Source code dependencies always point inward. As you move inward, the level of abstraction and policy increases. The outermost circle consists of low-level concrete details. As you move inward, the software grows more abstract and encapsulates higher-level policies. The innermost circle is the most general and highest level.

#### Crossing Boundaries

At the lower right of the diagram in Figure 22.1 is an example of how we cross the circle boundaries... ...flow of control: It begins in the controller, moves through the use case, and then winds up executing in the presenter. Note also the source code dependencies: Each points inward toward the use cases.

We usually resolve this apparent contradiction by using the Dependency Inversion Principle... ...we would arrange interfaces and inheritance relationships such that the source code dependencies oppose the flow of control at just the right points across the boundary.

No name in an outer circle can be mentioned by an inner circle. So we have the use case call an interface (shown in Figure 22.1 as "use case output port") in the inner circle, and have the presenter in the outer circle implement it.

We take advantage of dynamic polymorphism to create source code dependencies that oppose the flow of control so that we can conform to the Dependency Rule, no matter which direction the flow of control travels.

#### Which Data Crosses the Boundaries

The data that crosses the boundaries consists of simple data structures.

Basic structs or simple data transfer objects... ...Or the data can simply be arguments in function calls... ...The important thing is that isolated, simple data structures are passed across the boundaries. We don’t want to cheat and pass Entity objects or database rows. We don’t want the data structures to have any kind of dependency that violates the Dependency Rule.

When we pass data across a boundary, it is always in the form that is most convenient for the inner circle.

### A Typical Scenario

![Figure 22.2 A typical scenario for a web-based Java system utilizing a database](./assets/figure22.2.jpg)

Figure 22.2 A typical scenario for a web-based Java system utilizing a database


Figure 22.2 shows a typical scenario for a web-based Java system using a database. The web server gathers input data from the user and hands it to the `Controller` on the upper left. The `Controller` packages that data into a plain old Java object and passes this object through the `InputBoundary` to the `UseCaseInteractor`. The `UseCaseInteractor` interprets that data and uses it to control the dance of the `Entities`. It also uses the `DataAccessInterface` to bring the data used by those `Entities` into memory from the `Database`. Upon completion, the `UseCaseInteractor` gathers data from the `Entities` and constructs the `OutputData` as another plain old Java object. The `OutputData` is then passed through the `OutputBoundary` interface to the `Presenter`. The job of the `Presenter` is to repackage the `OutputData` into viewable form as the `ViewModel`, which is yet another plain old Java object. The `ViewModel` contains mostly `Strings` and flags that the `View` uses to display the data. Whereas the `OutputData` may contain `Date` objects, the `Presenter` will load the `ViewModel` with corresponding `Strings` already formatted properly for the user. The same is true of `Currency` objects or any other business-related data. `Button` and `MenuItem` names are placed in the `ViewModel`, as are flags that tell the `View` whether those `Buttons` and `MenuItems` should be gray. This leaves the `View` with almost nothing to do other than to move the data from the `ViewModel` into the `HTML` page.

All dependencies cross the boundary lines pointing inward, following the Dependency Rule.

### Conclusion

By separating the software into layers and conforming to the Dependency Rule, you will create a system that is intrinsically testable, with all the benefits that implies.

When any of the external parts of the system become obsolete... ...you can replace those obsolete elements with a minimum of fuss.

## Chapter 23 Presenters and Humble Objects

Presenters are a form of the _Humble Object_ pattern, which helps us identify and protect architectural boundaries.

### The Humble Object Pattern

The _Humble Object_ pattern is a design pattern that was originally identified as a way to help unit testers to separate behaviors that are hard to test from behaviors that are easy to test.

Split the behaviors into two modules or classes. One... ...is humble; it contains all the hard-to-test behaviors stripped down to their barest essence. The other module contains all the testable behaviors that were stripped out of the humble object.

GUIs are hard to unit test... ...difficult to... ...check... ...elements displayed. However, most of the behavior of a GUI is, in fact, easy to test. Using the _Humble Object_ pattern, we can separate these two kinds of behaviors into two different classes called the Presenter and the View.

### Presenters and Views

The View is the humble object that is hard to test. The code in this object is kept as simple as possible. It moves data into the GUI but does not process that data.

The Presenter is the testable object. Its job is to accept data from the application and format it for presentation so that the View can simply move it to the screen.

If the application wants to display money on the screen, it might pass a _Currency_ object to the Presenter. The Presenter will format that object with the appropriate decimal places and currency markers, creating a string that it can place in the View Model.

The names for every radio button, check box, and text field are loaded, by the Presenter, into appropriate strings and booleans in the View model.

Anything and everything that appears on the screen, and that the application has some kind of control over, is represented in the View Model as a string, or a boolean, or an enum. Nothing is left for the View to do other than to load the data from the View Model into the screen. Thus the View is humble.

### Testing and Architecture

Testability is an attribute of good architectures.

The _Humble Object_ pattern... ...separation of the behaviors into testable and non-testable parts often defines an architectural boundary. The Presenter/View boundary is one of these boundaries.

### Database Gateways

Between the use case interactors and the database are the database gateways... ...polymorphic interfaces that contain methods for every create, read, update, or delete operation that can be performed by the application on the database.

We do not allow SQL in the use cases layer; instead, we use gateway interfaces that have appropriate methods. Those gateways are implemented by classes in the database layer. That implementation is the humble object. It simply uses SQL... ...to access the data required by each of the methods.

The interactors... ...are not humble because they encapsulate application-specific business rules... ...are _testable,_ because the gateways can be replaced with appropriate stubs and test-doubles.

### Data Mappers

There is no such thing as an object relational mapper (ORM). The reason is simple: Objects are not data structures. At least, they are not data structures from their users’ point of view. The users of an object cannot see the data, since it is all private. Those users see only the public methods of that object. So, from the user’s point of view, an object is simply a set of operations.

A data structure is a set of public data variables that have no implied behavior.

ORMs would be better named "data mappers," because they load data into data structures from relational database tables.

ORM reside In the database layer. ORMs form another kind of _Humble Object_ boundary between the gateway interfaces and the database.

### Service Listeners

If your application must communicate with other services, or if your application provides a set of services... ...The application will load data into simple data structures and then pass those structures across the boundary to modules that properly format the data and send it to external services. On the input side, the service listeners will receive data from the service interface and format it into a simple data structure that can be used by the application. That data structure is then passed across the service boundary.

### Conclusion

At each architectural boundary, we are likely to find the _Humble Object_ pattern... ...The communication across that boundary... ...involve... ...simple data structure, and the boundary will frequently divide something that is hard to test from something that is easy to test... ...increases the testability of the entire system.

## Chapter 24 Partial Boundaries

Full-fledged architectural boundaries are expensive. They require reciprocal polymorphic `Boundary` interfaces, `Input` and `Output` data structures, and all of the dependency management necessary to isolate the two sides into independently compilable and deployable components.

A good architect might judge that the expense of such a boundary is too high—but might still want to hold a place for such a boundary in case it is needed later... ...In that case, they may implement a partial boundary.

### Skip the Last Step

One way to construct a partial boundary is to do all the work necessary to create independently compilable and deployable components, and then simply keep them together in the same component. The reciprocal interfaces are there, the input/output data structures are there, and everything is all set up—but we compile and deploy all of them as a single component.

Partial boundary requires the same amount of code and preparatory design work as a full boundary. However, it does not require the administration of multiple components.

### One-Dimensional Boundaries

The full-fledged architectural boundary uses reciprocal boundary interfaces to maintain isolation in both directions. Maintaining separation in both directions is expensive both in initial setup and in ongoing maintenance.

![Figure 24.1 The Strategy pattern](./assets/figure24.1.jpg)

Figure 24.1 The Strategy pattern

A simpler structure that serves to hold the place for later extension to a full- fledged boundary... ...Figure 24.1.. ..._Strategy_ pattern. A `ServiceBoundary` interface is used by clients and implemented by `ServiceImpl` classes... ...this sets the stage for a future architectural boundary.

The separation can degrade pretty rapidly... ...Without reciprocal interfaces, nothing prevents this kind of backchannel other than the diligence and discipline of the developers and architects.

### Facades

_Facade_ pattern... ...even the dependency inversion is sacrificed. The boundary is simply defined by the Facade class, which lists all the services as methods, and deploys the service calls to classes that the client is not supposed to access.

![Figure 24.2 The Facade pattern](./assets/figure24.2.jpg)

Figure 24.2 The Facade pattern

`Client` has a transitive dependency on all those service classes. In static languages, a change to the source code in one of the `Service` classes will force the `Client` to recompile.

### Conclusion

Each of these approaches has its own set of costs and benefits. Each is appropriate, in certain contexts, as a placeholder for an eventual full-fledged boundary. Each can also be degraded if that boundary never materializes.

It is one of the functions of an architect to decide where an architectural boundary might one day exist, and whether to fully or partially implement that boundary.

## Chapter 25 Layers and Boundaries

UI, business rules, and database. For some simple systems, this is sufficient. For most systems, though, the number of components is larger than that.

### Hunt the Wumpus

In Figure 25.1 any number of UI components can reuse the same game rules. The game rules do not know, nor do they care, which human language is being used.

![Figure 25.1 Any number of UI components can reuse the game rules](./assets/figure25.1.jpg)

Figure 25.1 Any number of UI components can reuse the game rules

We don’t want the game rules to know anything about the different kinds of data storage, so the dependencies have to be properly directed following the Dependency Rule, as shown in Figure 25.2.

![Figure 25.2 Following the Dependency Rule](./assets/figure25.2.jpg)

Figure 25.2 Following the Dependency Rule

### Clean Architecture?

We could easily apply the clean architecture approach in this context, with all the use cases, boundaries, entities, and corresponding data structures.

We also might want to vary the mechanism by which we communicate the text... ...That means that there is a potential architectural boundary defined by this axis of change. Perhaps we should construct an API that crosses that boundary and isolates the language from the communications mechanism; that idea is illustrated in Figure 25.3.

![Figure 25.3 The revised diagram](./assets/figure25.3.jpg)

Figure 25.3 The revised diagram

In Figure 25.3... ...the dashed outlines indicate abstract components that define an API that is implemented by the components above or below them... ...The API is defined and owned by the user, rather than by the implementer.

Inside `GameRules`, we would find polymorphic `Boundary` interfaces used by the code inside `GameRules` and implemented by the code inside the Language component. We would also find polymorphic Boundary interfaces used by Language and implemented by code inside GameRules.

The variations, such as `English`, `SMS`, and `CloudData`, are provided by polymorphic interfaces defined in the abstract API component, and implemented by the concrete components that serve them. For example, we would expect polymorphic interfaces defined in `Language` to be implemented by `English` and `Spanish`.

We can simplify this diagram by eliminating all the variations and focusing on just the API components. Figure 25.4 shows this diagram... ...This orientation makes sense because GameRules is the component that contains the highest-level policies.

![Figure 25.4 Simplified diagram](./assets/figure25.4.jpg)

Figure 25.4 Simplified diagram

This organization effectively divides the flow of data into two streams. The stream on the left is concerned with communicating with the user, and the stream on the right is concerned with data persistence. Both streams meet at the top3 at `GameRules`, which is the ultimate processor of the data that goes through both streams.

### Crossing the Streams

To play Hunt the Wumpus on the net with multiple players we would need a network component... ...in Figure 25.5. This organization divides the data flow into three streams, all controlled by the `GameRules`.

![Figure 25.5 Adding a network component](./assets/figure25.5.jpg)

Figure 25.5 Adding a network component

As systems become more complex, the component structure may split into many such streams.

### Splitting the Streams

You may be thinking that all the streams eventually meet at the top in a single component. If only life were so simple! The reality, of course, is much more complex.

Another set of policies at an even higher level—policies that know the health of the player, and the cost or benefit of a particular event... ...The lower-level mechanics policy would declare events to this higher-level policy... ...The higher-level policy would then manage the state of the player (as shown in Figure 25.6). Eventually that policy would decide whether the player wins or loses.

![Figure 25.6 The higher-level policy manages the player](./assets/figure25.6.jpg)

Figure 25.6 The higher-level policy manages the player

Is this an architectural boundary? Do we need an API that separates `MoveManagement` from `PlayerManagement`? Well, let’s... ...add micro-services... ...multiplayer version of Hunt the Wumpus... ...Figure 25.7... ...The `Network` elements are a bit more complex than depicted... ...A full-fledged architectural boundary exists between `MoveManagement` and `PlayerManagement` in this case.

![Figure 25.7 Adding a micro-service API](./assets/figure25.7.jpg)

Figure 25.7 Adding a micro-service API

### Conclusion

Architectural boundaries exist everywhere. Architects, must be careful to recognize when they are needed... ...be aware that such boundaries, when fully implemented, are expensive.

When boundaries are ignored, they are very expensive to add in later—even in the presence of comprehensive test-suites and refactoring discipline.

So what do we do, we architects? The answer is dissatisfying. On the one hand, some very smart people have told us, over the years, that we should not anticipate the need for abstraction. This is the philosophy of YAGNI: "You aren’t going to need it." There is wisdom in this message, since over-engineering is often much worse than under-engineering. On the other hand, when you discover that you truly do need an architectural boundary where none exists, the costs and risks can be very high to add such a boundary. So there you have it. O Software Architect, you must see the future. You must guess—intelligently. You must weigh the costs and determine where the architectural boundaries lie, and which should be fully implemented, and which should be partially implemented, and which should be ignored.

You don’t simply decide at the start of a project which boundaries to implement and which to ignore. Rather, you _watch._ You pay attention as the system evolves.

You note where boundaries may be required, and then carefully watch for the first inkling of friction because those boundaries don’t exist. At that point, you weigh the costs of implementing those boundaries versus the cost of ignoring them.

Your goal is to implement the boundaries right at the inflection point where the cost of implementing becomes less than the cost of ignoring. It takes a watchful eye.

## Chapter 26 The Main Component

In every system, there is at least one component that creates, coordinates, and oversees the others. I call this component `Main`.

### The Ultimate Detail

The `Main` component is the ultimate detail—the lowest-level policy. It is the initial entry point of the system... ...Its job is to create all the Factories, Strategies, and other global facilities, and then hand control over to the high-level abstract portions of the system.

In this `Main` component that dependencies should be injected by a Dependency Injection framework. Once they are injected into `Main`, `Main` should distribute those dependencies normally, without using the framework.

Think of `Main` as the dirtiest of all the dirty components.

The following `Main` component from Hunt the Wumpus... ...loads up all the strings that we don’t want the main body of the code to know about.

```java
public class Main implements HtwMessageReceiver {
  private static HuntTheWumpus game;
  private static int hitPoints = 10;
  private static final List<String> caverns = new ArrayList<>();
  private static final String[] environments = new String[]{ 
    "bright",
    "humid",
    "dry",
    "creepy",
    "ugly",
    "foggy",
    "hot",
    "cold",
    "drafty",
    "dreadful"
  };
  
  private static final String[] shapes = new String[] { 
    "round",
    "square",
    "oval",
    "irregular",
    "long",
    "craggy",
    "rough",
    "tall",
    "narrow"
  };

  private static final String[] cavernTypes = new String[] { 
    "cavern",
    "room",
    "chamber",
    "catacomb",
    "crevasse",
    "cell",
    "tunnel",
    "passageway",
    "hall",
    "expanse"
  };

  private static final String[] adornments = new String[] {
    "smelling of sulfur",
    "with engravings on the walls",
    "with a bumpy floor",
    "",
    "littered with garbage",
    "spattered with guano",
    "with piles of Wumpus droppings",
    "with bones scattered around",
    "with a corpse on the floor",
    "that seems to vibrate",
    "that feels stuffy",
    "that fills you with dread"
};   
```

The `main` function... ...uses the `HtwFactory` to create the game. It passes in the name of the class, `htw.game.HuntTheWumpusFacade`, because that class is even dirtier than `Main`. This prevents changes in that class from causing `Main` to recompile/redeploy... ...also the `main` creates the input stream and contains the main loop of the game, interpreting the simple input commands, but then defers all processing to other, higher-level components... ...`main` creates the map.

```java
public static void main(String[] args) throws IOException { 
  game = HtwFactory.makeGame("htw.game.HuntTheWumpusFacade", new Main());

  createMap(); 
  BufferedReader br = new BufferedReader(new InputStreamReader(System.in)); 
  game.makeRestCommand().execute();
  while (true) {
    System.out.println(game.getPlayerCavern()); 
    System.out.println("Health: " + hitPoints + " arrows: " + game.getQuiver()); 
    HuntTheWumpus.Command c = game.makeRestCommand();
    System.out.println(">");
    String command = br.readLine();
    if (command.equalsIgnoreCase("e"))
      c = game.makeMoveCommand(EAST);
    else if (command.equalsIgnoreCase("w"))
      c = game.makeMoveCommand(WEST);
    else if (command.equalsIgnoreCase("n"))
      c = game.makeMoveCommand(NORTH);
    else if (command.equalsIgnoreCase("s"))
      c = game.makeMoveCommand(SOUTH);
    else if (command.equalsIgnoreCase("r"))
      c = game.makeRestCommand();
    else if (command.equalsIgnoreCase("sw"))
      c = game.makeShootCommand(WEST);
    else if (command.equalsIgnoreCase("se"))
      c = game.makeShootCommand(EAST);
    else if (command.equalsIgnoreCase("sn"))
      c = game.makeShootCommand(NORTH);
    else if (command.equalsIgnoreCase("ss"))
      c = game.makeShootCommand(SOUTH); 
    else if (command.equalsIgnoreCase("q"))
      return;
    
    c.execute();
  }
}
```

```java
private static void createMap() {
  int nCaverns = (int) (Math.random() * 30.0 + 10.0); 
  while (nCaverns-- > 0)
    caverns.add(makeName());
  
  for (String cavern : caverns) {
    maybeConnectCavern(cavern, NORTH);
    maybeConnectCavern(cavern, SOUTH);
    maybeConnectCavern(cavern, EAST);
    maybeConnectCavern(cavern, WEST);
  }

  String playerCavern = anyCavern();
  game.setPlayerCavern(playerCavern); 
  game.setWumpusCavern(anyOther(playerCavern)); 
  game.addBatCavern(anyOther(playerCavern));
  game.addBatCavern(anyOther(playerCavern)); 
  game.addBatCavern(anyOther(playerCavern));
  
  game.addPitCavern(anyOther(playerCavern));
  game.addPitCavern(anyOther(playerCavern)); 
  game.addPitCavern(anyOther(playerCavern));
  
  game.setQuiver(5); 
}

// much code removed... 
}
```

The point is that `Main` is a dirty low-level module in the outermost circle of the clean architecture. It loads everything up for the high level system, and then hands control over to it.

### Conclusion

Think of `Main` as a plugin to the application that sets up the initial conditions and configurations, gathers all the outside resources, and then hands control over to the high-level policy of the application.

Since it is a plugin, it is possible to have many `Main` components, one for each configuration of your application... ...you could have a `Main` plugin for _Dev,_ another for _Test,_ and yet another for _Production_... ...also... ...for each country you deploy to, or each jurisdiction, or each customer.

When you think about `Main` as a plugin component, sitting behind an architectural boundary, the problem of configuration becomes a lot easier to solve.

## Chapter 27 Services: Great and Small

Service-oriented “architectures” and micro-service “architectures”... ...popularity include the following:
- Services seem to be strongly decoupled from each other... ...this is only partially true.
- Services appear to support independence of development and deployment... ...this is only partially true.

### Service Architecture?

The notion that using services, by their nature, is an architecture. This is patently untrue. The architecture of a system is defined by boundaries that separate high-level policy from low-level detail and follow the Dependency Rule. Services that simply separate application behaviors are little more than expensive function calls, and are not necessarily architecturally significant.

Not all services _should_ be architecturally significant. There are... ...benefits creating services that separate functionality across processes and platforms—whether they obey the Dependency Rule or not. It’s just that services, in and of themselves, do not define an architecture.

The architecture of a monolithic or component-based system is defined by certain function calls that cross architectural boundaries and follow the Dependency Rule. Many other functions in those systems, however, simply separate one behavior from another and are not architecturally significant.

Services are, after all, just function calls across process and/or platform boundaries. Some of those services are architecturally significant, and some aren’t.

### Service Benefits?

#### The Decoupling Fallacy

One of the big supposed benefits... ...is that services are strongly decoupled from each other... ...each service runs in a different process... ...therefore those services do not have access to each other’s variables. What’s more, the interface of each service must be well defined... ...certainly... ...but not very much truth. Yes, services are decoupled at the level of individual variables. However, they can still be coupled by shared resources within a processor, or on the network. What’s more, they are strongly coupled by the data they share.

Services are strongly coupled by the data they share.

If a new field is added to a data record that is passed between services, then every service that operates on the new field must be changed... ...Thus those services are strongly coupled to the data record and, therefore, indirectly coupled to each other.

Service interfaces are no more formal, no more rigorous, and no better defined than function interfaces. Clearly, then, this benefit is something of an illusion.

#### The Fallacy of Independent Development and Deployment

Another of the supposed benefits of services is that can be owned and operated by a dedicated team... ...responsible for writing, maintaining, and operating the service as part of a dev-ops strategy... ...presumed to be _scalable_... ...There is some truth to this belief. First... ...large enterprise systems can be built from monoliths and component- based systems as well as service-based systems. Thus services are not the only option for building scalable systems.
Second, the decoupling fallacy means that services cannot always be independently developed, deployed, and operated. To the extent that they are coupled by data or behavior, the development, deployment, and operation must be coordinated.

### The Kitty Problem

Taxi aggregator system... ...build it out of lots of little micro-services... ...The diagram in Figure 27.1 shows how our fictitious architects arranged services to implement this application. The `TaxiUI` service deals with the customers, who use mobile devices to order taxis. The `TaxiFinder` service examines the inventories of the various `TaxiSuppliers` and determines which taxies are possible candidates for the user. It deposits these into a short-term data record attached to that user. The `TaxiSelector` service takes the user’s criteria of cost, time, luxury, and so forth, and chooses an appropriate taxi from among the candidates. It hands that taxi off to the `TaxiDispatcher` service, which orders the appropriate taxi.

![Figure 27.1 Services arranged to implement the taxi aggregator system](./assets/figure27.1.jpg)

Figure 27.1 Services arranged to implement the taxi aggregator system

Marketing department... ...announce their plans to offer a kitten delivery service to the city... ...When a kitten order is placed, a nearby taxi will be selected to collect a kitten from one of those collection points, and then deliver it to the appropriate address... ...Of course, some drivers may be allergic to cats, so those drivers should never be selected for this service. Also, some customers will undoubtedly have similar allergies, so a vehicle that has been used to deliver kittens within the last 3 days should not be selected for customers who declare such allergies... ...How many of those services will have to change to implement this feature? _All of them_... ...In other words, the services are all coupled, and cannot be independently developed, deployed, and maintained. This is the problem with cross-cutting concerns. Every software system must face this problem, whether service oriented or not.

Functional decompositions, of the kind depicted in the service diagram in Figure 27.1, are very vulnerable to new features that cut across all those functional behaviors.

### Objects to the Rescue

This problem in a component-based architecture?... ...SOLID design principles... ...create a set of classes that could be polymorphically extended to handle new features.

Figure 27.2 shows the strategy. The classes in this diagram roughly correspond to the services shown in Figure 27.1. However, note the boundaries. Note also that the dependencies follow the Dependency Rule.

Much of the logic... ...preserved within the base classes of the object model. However... ...logic specific to _rides_ has been extracted into a `Rides` component. The new feature for kittens has been placed into a `Kittens` component. These two components override the abstract base classes in the original components using a pattern such as _Template Method or Strategy._

New components, `Rides` and `Kittens`, follow the Dependency Rule... ...classes that implement those features are created by factories under the control of the UI.

When the Kitty feature is implemented, the `TaxiUI` must change. But nothing else needs to be changed... ...Thus the Kitty feature is decoupled, and independently developable and deployable.

![Figure 27.2 Using an object-oriented approach to deal with cross-cutting concerns](./assets/figure27.2.jpg)

Figure 27.2 Using an object-oriented approach to deal with cross-cutting concerns

### Component-Based Services

Services do not need to be little monoliths. Services can, instead, be designed using the SOLID principles, and given a component structure so that new components can be added to them without changing the existing components within the service.

Each new feature... ...as another jar file that contains classes that extend the abstract classes in the first jar files. Deploying a new feature then becomes not a matter of redeploying the services, but... ...simply _adding_ the new jar files to the load paths of those services... ...adding new features conforms to the Open-Closed Principle.

Figure 27.3 shows the structure. The services still exist as before, but each has its own internal component design, allowing new features to be added as new derivative classes. Those derivative classes live within their own components.

![Figure 27.3 Each service has its own internal component design, enabling new features to be added as new derivative classes](./assets/figure27.3.jpg)

Figure 27.3 Each service has its own internal component design, enabling new features to be added as new derivative classes

### Cross-Cutting Concerns

Architectural boundaries do not fall _between_ services. Rather, those boundaries run _through_ the services, dividing them into components.

To deal with the cross-cutting concerns that all significant systems face, services must be designed with internal component architectures that follow the Dependency Rule.

Services do not define the architectural boundaries of the system; instead, the components within the services do.

![Figure 27.4 Services must be designed with internal component architectures that follow the Dependency Rule](./assets/figure27.4.jpg)

Figure 27.4 Services must be designed with internal component architectures that follow the Dependency Rule

### Conclusion

As useful as services are to the scalability and develop-ability of a system, they are not, in and of themselves, architecturally significant elements.

The architecture of a system is defined by the boundaries drawn within that system, and by the dependencies that cross those boundaries.

Architecture is not defined by the physical mechanisms by which elements communicate and execute.

A service might be a single component, completely surrounded by an architectural boundary. Alternatively, a service might be composed of several components separated by architectural boundaries. In rare2 cases, clients and services may be so coupled as to have no architectural significance whatever.

## Chapter 28 The Test Boundary

_The tests are part of the system,_ and they participate in the architecture just like every other part of the system does.

### Tests as System Components

From an architectural point of view, all tests are the same. Whether they are the tiny little tests created by TDD, or large... ...tests, they are architecturally equivalent.

Tests, by their very nature, follow the Dependency Rule; they are very detailed and concrete; and they always depend inward toward the code being tested.

Tests as the outermost circle in the architecture. Nothing within the system depends on the tests, and the tests always depend inward on the components of the system.

Tests are also independently deployable. In fact, most of the time they are deployed in test systems, rather than in production systems. So, even in systems where independent deployment is not otherwise necessary, the tests will still be independently deployed.

Tests are the most isolated system component. They are not necessary for system operation. No user depends on them. Their role is to support development, not operation.

They are no less a system component than any other. In fact, in many ways they represent the model that all other system components should follow.

### Design for Testability

The extreme isolation of the tests, combined with the fact that they are not usually deployed, often causes developers to think that tests fall outside of the design of the system. This is a catastrophic point of view.

Tests that are not well integrated into the design of the system tend to be fragile, and they make the system rigid and difficult to change.

The issue... ...is coupling. Tests that are strongly coupled to the system must change along with the system.

Changes to common system components can cause hundreds, or even thousands, of tests to break. This is known as the _Fragile Tests Problem._

Fragile tests often have the perverse effect of making the system rigid. When developers realize that simple changes to the system can cause massive test failures, they may resist making those changes.

The solution is to design for testability. The first rule of software design— whether for testability or for any other reason—is always the same: _Don’t depend on volatile things._

GUIs are volatile. Test suites that operate the system through the GUI _must be fragile._ Therefore design the system, and the tests, so that business rules can be tested without using the GUI.

### The Testing API

Create a specific API that the tests can use to verify all the business rules. This API should... ...allow the tests to avoid security constraints... ...and force the system into particular testable states... ...will be a superset of the suite of _interactors_ and _interface adapters_ that are used by the user interface.

The purpose of the testing API is to decouple the tests from the application... ...The goal is to decouple the _structure_ of the tests from the _structure_ of the application.

#### Structural Coupling

Structural coupling is one of the strongest, and most insidious, forms of test coupling.

A test suite that has a test class for every production class, and a set of test methods for every production method... ...When one of those production methods or classes changes, a large number of tests must change as well... ...they make the production code rigid.

The role of the testing API is to hide the structure of the application from the tests.

Production code to be refactored and evolved in ways that don’t affect the tests. It also allows the tests to be refactored and evolved in ways that don’t affect the production code.

This separation of evolution is necessary because as time passes, the tests tend to become increasingly more concrete and specific. In contrast, the production code tends to become increasingly more abstract and general.

Strong structural coupling prevents—or at least impedes—this necessary evolution, and prevents the production code from being as general, and flexible, as it could be.

#### Security

The superpowers of the testing API could be dangerous if they were deployed in production systems... ...then the testing API, and the dangerous parts of its implementation, should be kept in a separate, independently deployable component.

### Conclusion

Tests are not outside the system; rather, they are parts of the system that must be well designed if they are to provide the desired benefits of stability and regression.

Tests that are not designed as part of the system tend to be fragile and difficult to maintain.

## Chapter 29 Clean Embedded Architecture

> Although software does not wear out, firmware and hardware become obsolete, thereby requiring software modifications.
> — Doug Schmidt.

_Software_ is this thing that can have a long useful life, but _firmware_ will become obsolete as hardware evolves.

I’d like to add to Doug’s statement:

> Although software does not wear out, it can be destroyed from within by unman- aged dependencies on firmware and hardware.

It is not uncommon for embedded software to be denied a potentially long life due to being infected with dependencies on hardware.

Firmware does not mean code lives in ROM. It’s not firmware because of where it is stored; rather, it is firmware because of what it depends on and how hard it is to change as hardware evolves.

Hardware does evolve... ...so we should structure our embedded code with that reality in mind.

What we really need is less firmware and more software.

Non-embedded engineers also write firmware!... ...whenever you bury SQL in your code or when you spread platform dependencies throughout your code.

Stop writing so much firmware and give your code a chance at a long useful life.

## App-titude Test

Most of the emphasis is on getting the embedded code to work, and not so much emphasis is placed on structuring it for a long useful life.

Kent Beck describes... ...building software (the quoted text is Kent’s words and the italics are my commentary):
1. “First make it work.” _You are out of business if it doesn’t work._ 
2. “Then make it right.” _Refactor the code so that you and others can understand it and evolve it as needs change or are better understood._ 
3. “Then make it fast.” _Refactor the code for “needed” performance._

In _The Mythical Man-Month,_ Fred Brooks suggests we “plan to throw one away.” Kent and Fred are giving virtually the same advice: Learn what works, then make a better solution.

Most non-embedded apps are built just to work, with little regard to making the code right for a long useful life.

Getting an app to work is what I call the _App-titude_ test for a programmer.

Programmers... ...who just concern themselves with getting their app to work are doing their products and employers a disservice. There is much more to programming than just getting an app to work.

Application works: The engineer passed the App-titude test. But the application can’t be said to have a clean embedded architecture.

### The Target-Hardware Bottleneck

Most of the time the hardware is concurrently developed with the software and firmware. As an engineer developing code for this kind of system, you may have no place to run the code.

Yes, embedded is special. Embedded engineers are special. But embedded development is not _so_ special that the principles in this book are not applicable to embedded systems.

_The target-hardware bottleneck._ When embedded code is structured without applying clean architecture principles and practices, you will often face the scenario in which you can test your code only on the target. If the target is the only place where testing is possible, the target-hardware bottleneck will slow you down.

#### A Clean Embedded Architecture Is a Testable Embedded Architecture

Apply some of the architectural principles to embedded software and firmware to help you eliminate the target-hardware bottleneck.

##### Layers

![Figure 29.1 Three layers](./assets/figure29.1.jpg)

Figure 29.1 Three layers

If you are not careful about where you put things and what one module is allowed to know about another module, the code will be very hard to change... ...not just... ...when the hardware changes, but when the user asks for a change, or when a bug needs to be fixed.

![Figure 29.2 Hardware must be separated from the rest of the system](./assets/figure29.2.jpg)

Figure 29.2 Hardware must be separated from the rest of the system

Software and firmware intermingling is an anti-pattern. Code... ...will resist changes. In addition, changes will be dangerous, often leading to unintended consequences. Full regression tests of the whole system will be needed for minor changes.

The line between software and firmware is typically not so well defined as the line between code and hardware.

![Figure 29.3 The line between software and firmware is a bit fuzzier than the line between code and hardware](./assets/figure29.3.jpg)

Figure 29.3 The line between software and firmware is a bit fuzzier than the line between code and hardware

As an embedded software developer... ...firm up that line. The name of the boundary between the software and the firmware is the hardware abstraction layer (HAL) (Figure 29.4)

![Figure 29.4 The hardware abstraction layer](./assets/figure29.4.jpg)

Figure 29.4 The hardware abstraction layer

The HAL exists for the software that sits on top of it, and its API should be tailored to that software’s needs.

The HAL expressing services needed by the application.

Layers may contain layers. It is more of a repeating fractal pattern than a limited set of predefined layers.

#### Don’t Reveal Hardware Details to the User of the HAL

A clean embedded architecture’s software is testable _off_ the target hardware.

A successful HAL provides that seam or set of substitution points that facilitate off-target testing.

##### The Processor Is a Detail

When your embedded application uses a specialized tool chain, it will often provide header files to `<i>`help you`</i>`. These compilers often take liberties with the C language, adding new keywords to access their processor features. The code will look like C, but it is no longer C... ...it’s up to you to use that help in a way that does not hurt in the future. You will have to limit which files are allowed to know about the C extensions.

All of the _software_ should be processor independent, but not all of the _firmware_ can be.

A clean embedded architecture would use device access registers directly in very few places and confine them totally to the _firmware._ Anything that knows about these registers becomes _firmware_ and is consequently bound to the silicon.

If you use a micro-controller... ...your firmware could isolate these low- level functions with some form of a _processor abstraction layer_ (PAL). Firmware above the PAL could be tested off-target, making it a little less firm.

##### The Operating System Is a Detail

To give your embedded code a good chance at a long life, you have to treat the operating system as a detail and protect against OS dependencies.

The software accesses the services of the operating environment through the OS. The OS is a layer separating the software from firmware (Figure 29.5). Using an OS directly can cause problems.

![Figure 29.5 Adding in an operating system](./assets/figure29.5.jpg)

Figure 29.5 Adding in an operating system

A clean embedded architecture isolates software from the operating system, through an _operating system abstraction layer_ (OSAL) (Figure 29.6).

![Figure 29.6 The operating system abstraction layer](./assets/figure29.6.jpg)

Figure 29.6 The operating system abstraction layer

If your software depended on an OSAL instead of the OS directly, you would largely be writing a new OSAL that is compatible with the old OSAL. Which would you rather do: modify a bunch of complex existing code, or write new code to a defined interface and behavior? This is not a trick question. I choose the latter.

The layer becomes the place where much of the duplication around using an OS is isolated. This duplication does not have to impose a big overhead. If you define an OSAL, you can also encourage your applications to have a common structure. You might provide message passing mechanisms, rather than having every thread handcraft its concurrency model.

A clean embedded architecture’s software is testable off the target operating system.

OSAL provides that seam or set of substitution points that facilitate off-target testing.

#### Programming to Interfaces and Substitutability

The idea of a layered architecture is built on the idea of programming to interfaces.

When one module interacts with another though an interface, you can substitute one service provider for another.

Don’t clutter the interface header files with data structures, constants, and typedefs that are needed by only the implementation... ...That clutter will lead to unwanted dependencies.

Limit the visibility of the implementation details... ...The fewer places where code knows the details, the fewer places where code will have to be tracked down and modified.

A clean embedded architecture is testable within the layers because modules interact through interfaces. Each interface provides that seam or substitution point that facilitates off-target testing.

#### DRY Conditional Compilation Directives

There is a tendency to use conditional compilation to turn on and off segments of code... ...This repetition of code violates the Don’t Repeat Yourself (DRY) principle.

### Conclusion

Letting all code become firmware... ...Being able to test only in the target hardware is not good for your product’s long-term health. A clean embedded architecture is good for your product’s long-term health.

## PART VI Details

## Chapter 30 The Database Is a Detail

From an architectural point of view, the database is a non-entity—it is a detail that does not rise to the level of an architectural element.

The structure you give to the data within your application is highly significant to the architecture of your system. But the database is not the data model.

The database is a utility that provides access to the data... ...it’s a low-level detail—a mechanism. And a good architect does not allow low-level mechanisms to pollute the system architecture.

### Relational Databases

Edgar Codd defined the principles of relational databases in 1970.

There is nothing architecturally significant about arranging data into rows within tables. The use cases of your application should neither know nor care about such matters.

Knowledge of the tabular structure of the data should be restricted to the lowest-level utility functions in the outer circles of the architecture.

Many data access frameworks allow database rows and tables to be passed around the system as objects. Allowing this is an architectural error. It couples the use cases, business rules, and in some cases even the UI to the relational structure of the data.

### Why Are Database Systems So Prevalent?

The rotating magnetic disk was the mainstay of data storage for five decades... ...On a disk, data is stored within circular tracks. Those tracks are divided into sectors that hold a convenient number of bytes, often 4K. Each platter may have hundreds of tracks, and there can be a dozen or so platters. If you want to read a particular byte off the disk, you have to move the head to the proper track, wait for the disk to rotate to the proper sector, read all 4K of that sector into RAM, and then index into that RAM buffer to get the byte you want. And all that takes milliseconds.

To mitigate the time delay imposed by disks... ...you need a data access and management system... ...two distinct kinds: file systems and relational database management systems (RDBMS). File systems are document based. They provide a natural and convenient way to store whole documents. They work well when you need to save and retrieve a set of documents by name, but they don’t offer a lot of help when you’re searching the content of those documents... ...Database systems are content based. They provide a natural and convenient way to find records based on their content. They are very good at associating multiple records based on some bit of content that they all share. Unfortunately, they are rather poor at storing and retrieving opaque documents.

### What If There Were No Disk?

Disks... ...are being replaced by RAM... ...how will you organize that data?... ...into linked lists, trees, hash tables, stacks, queues, or any of the other myriad data structures, and you’ll access it using pointers or references—because _that’s what programmers do._

### Details

The database is a detail. It’s just a mechanism we use to move the data back and forth between the surface of the disk and RAM.

From an architectural viewpoint, we should not care about the form that the data takes while it is on the... ...disk. Indeed, we should not acknowledge that the disk exists at all.

### But What about Performance?

Isn’t performance an architectural concern?... ...when it comes to data storage, it’s a concern that can be entirely encapsulated and separated from the business rules.

### Anecdote

The database vendors at the time... ...had managed to convince high-level executives that their corporate “data assets” needed protection, and that the database systems they offered were the ideal means of providing that protection.

The word “enterprise” and the notion of “Service-Oriented Architecture” have much more to do with marketing than with reality.

### Conclusion

The organizational structure of data, the data model, is architecturally significant. The technologies and systems that move data on and off a rotating magnetic surface are not.

The data is significant. The database is a detail.

## Chapter 31 The Web Is a Detail

The...series of oscillations that our industry has gone through since the 1960s... ...move back and forth between putting all the computer power in central servers and putting all computer power out at the terminals.

Oscillations... ...since the web became prominent. At first we thought all the computer power would be in server farms, and the browsers would be stupid. Then we started putting applets in the browsers. But we didn’t like that, so we moved dynamic content back to the servers. But then we didn’t like that, so we invented Web 2.0 and moved lots of processing back into the browser with Ajax and JavaScript. We went so far as to create whole huge applications written to execute in the browsers. And now we’re all excited about pulling that JavaScript back into the server with Node. (Sigh.)

### The Endless Pendulum

We can’t seem to figure out where we want the computer power. We go back and forth between centralizing it and distributing it. And, I imagine, those oscillations will continue for some time to come.

The web was simply one of many oscillations in a struggle that began before most of us were born and will continue well after most of us have retired.

As architects, though, we have to look at the long term. Those oscillations are just short-term issues that we want to push away from the central core of our business rules.

I certainly would have lobbied very hard to isolate the business rules from the GUI, because you never know what the marketing geniuses will do next.

I do hope the architects at A, and the architects of the apps, keep their UI and business rules isolated from each other, because there are always marketing geniuses out there just waiting to pounce on the next little bit of coupling you create.

### The Upshot

The GUI is a detail. The web is a GUI. So the web is a detail.

Put details... ...behind boundaries that keep them separate from your core business logic.

_The WEB is an IO device._ In the 1960s, we learned the value of writing applications that were device independent... ...The web is not an exception to that rule. Or is it? The argument can be made that a GUI, like the web, is so unique and rich that it is absurd to pursue a device-independent architecture. When you think about the intricacies of JavaScript... ...or any of the plethora of widgets and gadgets you can put on a web page, it’s easy to argue that device independence is impractical. To some extent, this is true. The interaction between the application and the GUI is “chatty” in ways that are quite specific to the kind of GUI you have.

The interaction between the application and the GUI is “chatty” in ways that are quite specific to the kind of GUI you have.

The dance between a browser and a web application is different from the dance between a desktop GUI and its application.

Each use case can be described based on the input data, the processing preformed, and the output data.

At some point in the dance between the UI and the application, the input data can be said to be complete, allowing the use case to be executed. Upon completion, the resultant data can be fed back into the dance between the UI and the application.

The complete input data and the resultant output data can be placed into data structures and used as the input values and output values for a process that executes the use case. With this approach, we can consider each use case to be operating the IO device of the UI in a device-independent manner.

### Conclusion

This kind of abstraction is not easy,... ...But it is possible... ...But it is possible. And since the world is full of marketing geniuses, it’s not hard to make the case that it’s often very necessary.

## Chapter 32 Frameworks Are Details

Frameworks are not architectures—though some try to be.

### Framework Authors

Framework authors know their own problems, and the problems of their coworkers and friends. And they write their frameworks to solve _those_ problems—not yours.

Your problems will likely overlap with those other problems quite a bit. If this were not the case, frameworks would not be so popular. To the extent that such overlap exists, frameworks can be very useful indeed.

### Asymmetric Marriage

The relationship between you and the framework author is extraordinarily asymmetric. You must make a huge commitment to the framework, but the framework author makes no commitment to you whatsoever.

When you use a framework,... ...Typically, this means wrapping your architecture around that framework... ...The author urges you to _couple_ your application to the framework as tightly as possible.

The author wants you to couple to the framework, because once coupled in this way, it is very hard to break away.

The author is asking you to marry the framework—to make a huge, long-term commitment to that framework. And yet, under no circumstances will the author make a corresponding commitment to you. It’s a one- directional marriage. You take on all the risk and burden; the framework author takes on nothing at all.

### The Risks

The architecture of the framework is often not very clean. Frameworks tend to violate he Dependency Rule.

The framework may help you with some early features... ...However, as your product matures,... ...you’ll find the framework fighting you more and more.

The framework may evolve in a direction that you don’t find helpful... ...upgrading to new versions that don’t help you.

A new and better framework may come along that you wish you could switch to.

### The Solution

_Don’t marry the framework!_

You can _use_ the framework—just don’t couple to it.

If the framework wants you to derive your business objects from its base classes, say no! Derive proxies instead, and keep those proxies in components that are _plugins_ to your business rules.

Integrate them into components that plug in to your core code, following the Dependency Rule.

### I Now Pronounce You …

There are some frameworks that you simply must marry... ...That’s normal—but it should still be a _decision._

When you marry a framework to your application, you will be stuck with that framework for the rest of the life cycle of that application.

### Conclusion

When faced with a framework, try not to marry it right away. See if there aren’t ways to date it for a while before you take the plunge.

Keep the framework behind an architectural boundary if at all possible, for as long as possible.

Find a way to get the milk without buying the cow.

## Chapter 33 Case Study: Video Sales

Put these rules and thoughts about architecture together into a case study... ...short and simple... ...the process a good architect uses and the decisions that such an architect makes.

### The Product

For this case study,... ...the software for a website that sells videos... ...on the web, to both individuals and businesses. Individuals can pay one price to stream the videos, and another, higher price to download those videos and own them permanently. Business licenses are streaming only, and are purchased in batches that allow quantity discounts.

Individuals typically act as both the viewers and the purchasers. Businesses, in contrast, often have people who buy the videos that other people will watch. Video authors need to supply their video files,... ...and other materials. Administrators need to add new video series, add and delete videos to and from the series, and establish prices for various licenses.

### Use Case Analysis

![Figure 33.1 A typical use-case analysis](./assets/figure33.1.jpg)

Figure 33.1 A typical use-case analysis

According to the Single Responsibility Principle, these four actors will be the four primary sources of change for the system. Every time some new feature is added, or... ...changed, that step will be taken to serve one of these actors. Therefore we want to partition the system such that a change to one actor does not affect any of the other actors.

In Figure 33.1... ...you won’t find log-in or log-out use cases... ...to manage the size of the problem in this book. If I were to include all the different use cases, then this chapter would have to turn into a book in its own right.

The dashed use cases... ... are _abstract_ use cases......that sets a general policy that another use case will flesh out. As you can see, the _View Catalog as Viewer_ and _View Catalog as Purchaser_ use cases both inherit from the _View Catalog_ abstract use case.

It was not strictly necessary... ...to create that abstraction. I could have left the abstract use case out... ...without compromising any of the features... ...On the other hand, these two use cases are _so similar_ that I thought it wise to recognize the similarity and find a way to unify it early in the analysis.

### Component Architecture

Now that we know the actors and use cases, we can create a preliminary component architecture (Figure 33.2).

The double lines... ...represent architectural boundaries... ...You can see the typical partitioning of views, presenters, interactors, and controllers. You can also see that I’ve broken each of those categories up by their corresponding actors.

Each of those components will contain the views, presenters, interactors, and controllers that have been allocated to it.

Note the special components for the `Catalog View` and the `Catalog Presenter`. This is how I dealt with the abstract _View Catalog_ use case... ...those views and presenters will be coded into abstract classes within those components, and the inheriting components will contain view and presenter classes that will inherit from those abstract classes.

![Figure 33.2 A preliminary component architecture](./assets/figure33.2.jpg)

Figure 33.2 A preliminary component architecture

Would I really break the system up into all these components, and deliver them as `.jar` or `.dll` files? Yes and no. I would certainly break the compile and build environment up this way, so that I _could_ build independent deliverables like that. I would also reserve the right to combine all those deliverables into a smaller number of deliverables if necessary. 

Given the partitioning in Figure 33.2, it would be easy to combine them into five `.jar` files—one for views, presenters, interactors, controllers, and utilities, respectively. I could then independently deploy the components that are most likely to change independently of each other.

Another possible grouping... ...views and presenters together into the same `.jar` file, and... ...interactors, controllers, and utilities in their own `.jar` file. Still another... ...more primitive... ...two `.jar` files, with views and presenters in one file, and everything else in the other.

Keeping these options open will allow us to adapt the way we deploy the system based on how the system changes over time.

### Dependency Management

The flow of control in Figure 33.2 proceeds from right to left. Input occurs at the controllers, and that input is processed into a result by the interactors. The presenters then format the results, and the views display those presentations.

The arrows do not all flow from the right to the left... ...most of them point from left to right. This is because the architecture is following the _Dependency Rule._ All dependencies cross the boundary lines in one direction, and they always point toward the components containing the higher-level policy.

The _using_ relationships (open arrows) point _with_ the flow of control, and that the _inheritance_ relationships (closed arrows) point _against_ the flow of control. This depicts our use of the Open–Closed Principle to make sure that the dependencies flow in the right direction, and that changes to low-level details do not ripple upward to affect high-level policies.

### Conclusion

The architecture diagram in Figure 33.2 includes two dimensions of separation. The first is the separation of actors based on the Single Responsibility Principle; the second is the Dependency Rule. The goal of both is to separate components that change for different reasons, and at different rates. The different reasons correspond to the actors; the different rates correspond to the different levels of policy.

Once you have structured the code this way, you can mix and match how you want to actually deploy the system. You can group the components into deployable deliverables in any way that makes sense, and easily change that grouping when conditions change.

## Chapter 34 The Missing Chapter

The devil is in the implementation details, and it’s really easy to fall at the last hurdle if you don’t give that some thought.

Imagine... ...an online book store,... ...customers being able to view the status of their orders... ...Let’s put the Clean Architecture to one side for a moment and look at a number of approaches to design and code organization.

### Package by Layer

Traditional horizontal layered architecture, where we separate our code based on what it does from a technical perspective.

Typical layered architecture,... ...one layer for the web code, one layer for our “business logic,” and one layer for persistence.

In Figure 34.1, all of the dependencies between layers (packages) point downward.

- `OrdersController`: A web controller,
- `OrdersService`: An interface that defines the “business logic” related to orders.
- `OrdersServiceImpl`: The implementation of the orders service.
- `OrdersRepository`: An interface that defines how we get access to persistent order information.
- `dbcOrdersRepository`: An implementation of the repository interface.

![Figure 34.1 Package by layer](./assets/figure34.1.jpg)

Figure 34.1 Package by layer

In “Presentation Domain Data Layering,” Martin Fowler says that adopting such a layered architecture is a good way to get started. He’s not alone.

The problem, as Martin points out, is that once your software grows in scale and complexity, you will quickly find that having three large buckets of code isn’t sufficient, and you will need to think about modularizing further.

Another problem is that, as Uncle Bob has already said, a layered architecture doesn’t scream anything about the business domain.

### Package by Feature

Vertical slicing, based on related features, domain concepts, or aggregate roots.

With this approach, as shown in Figure 34.2, we have the same interfaces and classes as before, but they are all placed into a single Java package rather than being split among three packages.

This is a very simple refactoring from the “package by layer” style, but the top-level organization of the code now screams something about the business domain. We can now see that this code base has something to do with orders rather than the web, services, and repositories.

Another benefit is that it’s potentially easier to find all of the code that you need to modify... ...It’s all sitting in a single package rather than being spread out.

![Figure 34.2 Package by feature](./assets/figure34.2.jpg)

Figure 34.2 Package by feature

### Ports and Adapters

Approaches such as “ports and adapters,” the “hexagonal architecture,” “boundaries, controllers, entities,” and so on aim to create architectures where business/domain-focused code is independent and separate from the technical implementation details such as frameworks and databases.

Such code bases being composed of an “inside” (domain) and an “outside” (infrastructure), as suggested in Figure 34.3.

![Figure 34.3 A code base with an inside and an outside](./assets/figure34.3.jpg)

Figure 34.3 A code base with an inside and an outside

The “inside” region contains all of the domain concepts, whereas the “outside” region contains the interactions with the outside world.

The “outside” depends on the “inside”—never the other way around.

Figure 34.4... ...how the “view orders” use case might be implemented. The `com.mycompany.myapp.domain` package here is the “inside,” and the other packages are the “outside.”... ...the dependencies flow toward the “inside.”.

The `OrdersRepository` from previous diagrams has been renamed to simply be `Orders`. This comes from the world of domain-driven design, where the advice is that the naming of everything on the “inside” should be stated in terms of the “ubiquitous domain language.”... ...we talk about “orders” when we’re having a discussion about the domain, not the “orders repository.”

![Figure 34.4 View orders use case](./assets/figure34.4.jpg)

Figure 34.4 View orders use case

### Package by Component

Although I agree wholeheartedly with the discussions about SOLID, REP, CCP, and CRP and most of the advice in this book, I come to a slightly different conclusion about how to organize code. So I’m going to present another option here, which I call “package by component.”... ...I’ve spent most of my career building enterprise software,... ...Although the technologies differed, the common theme was that the architecture for most of these software systems was based on a traditional layered architecture... ...to separate code that has the same sort of function. Web stuff is separated from business logic, which is in turn separated from data access... ...From a code accessibility perspective, for the `OrdersController` to be able to have a dependency on the `OrdersService` interface, the `OrdersService` interface needs to be marked as `public`, because they are in different packages. Likewise, the `OrdersRepository` interface needs to be marked as `public` so that it can be seen outside of the repository package, by the `OrdersServiceImpl` class.

 In a strict layered architecture, the dependency arrows should always point downward, with layers depending only on the next adjacent lower layer... ...creating a nice, clean, acyclic dependency graph, which is achieved by introducing some rules about how elements in a code base should depend on each other. The big problem here is that we can cheat by introducing some undesirable dependencies, yet still create a nice, acyclic dependency graph.

Figure 34.5. The dependency arrows still point downward, but the `OrdersController` is now additionally bypassing the `OrdersService` for some use cases. This organization is often called a _relaxed layered architecture,_ as layers are allowed to skip around their adjacent neighbor(s). 

In some situations, this is the intended outcome—if you’re trying to follow the CQRS pattern, for example.

In many other cases, bypassing the business logic layer is undesirable, especially if that business logic is responsible for ensuring authorized access to individual records, for example.

![Figure 34.5 Relaxed layered architecture](./assets/figure34.5.jpg)

Figure 34.5 Relaxed layered architecture

We need here a guideline—an architectural principle—that says something like, “Web controllers should never access repositories directly.”

Many teams I’ve met... ...enforce this principle through good discipline and code reviews,... ...but we all know what happens when budgets and deadlines start looming ever closer.

If left unchecked, this practice can turn a code base into a “big ball of mud.”

Use the compiler to enforce my architecture if at all possible.

The “package by component” It’s a hybrid approach to everything we’ve seen so far, with the goal of bundling all of the responsibilities related to a single coarse-grained component into a single Java package.

Taking a service-centric view of a software system, which is something we’re seeing with micro-service architectures as well. In the same way that ports and adapters treat the web as just another delivery mechanism, “package by component” keeps the user interface separate from these coarse- grained components.

This approach bundles up the “business logic” and persistence code into a single thing, which I’m calling a “component.”

> Components are the units of deployment. They are the smallest entities that can be deployed as part of a system. In Java, they are jar files.
> — Robert C. Martin

![Figure 34.6 View orders use case](./assets/figure34.6.jpg)

Figure 34.6 View orders use case

My definition of a component is slightly different: “A grouping of related functionality behind a nice clean interface, which resides inside an execution environment like an application.”

“C4 software architecture model,"... ...a simple hierarchical way to think about the static structures of a software system in terms of containers, components, and classes (or code).

A key benefit of the “package by component” approach is that if you’re writing code that needs to do something with `orders`, there’s just one place to go—the `OrdersComponent`. Inside the component, the separation of concerns is still maintained, so the business logic is separate from data persistence, but that’s a component implementation detail that consumers don’t need to know about.

You can think of well-defined components in a monolithic application as being a stepping stone to a micro- services architecture.

### The Devil Is in the Implementation Details

The four approaches... ...look like different ways to organize code and could be considered different architectural styles. This perception starts to unravel very quickly if you get the implementation details wrong.

Something I see on a regular basis is an overly liberal use of the `public` access modifier in languages such as Java... ...developers, instinctively use the `public` keyword without thinking... ...regardless of which architectural style a code base is aiming to adopt.

Marking all of your types as `public` means you’re not taking advantage of the facilities that your programming language provides with regard to encapsulation.

### Organization versus Encapsulation

If you make all types in your Java application `public`, the packages are simply an organization mechanism (a grouping, like folders), rather than being used for encapsulation... ...the Java packages become an irrelevant detail if all of the types are marked as `public`... ...all four architectural approaches presented earlier in this chapter are exactly the same when we overuse this designation (Figure 34.7).

The arrows between each of the types in Figure 34.7:... ...identical regardless of which architectural approach you’re trying to adopt.

When you make all of the types `public`, what you really have are just four ways to describe a traditional horizontally layered architecture.

Nobody would ever make all of their Java types `public`. Except when they do. And I’ve seen it.

The access modifiers in Java are not perfect, but ignoring them is just asking for trouble. The way Java types are placed into packages can actually make a huge difference to how accessible (or inaccessible) those types can be when Java’s access modifiers are applied appropriately.

If I bring the packages back and mark... ...those types where the access modifier can be made more restrictive,... ...(Figure 34.8).

![Figure 34.7 All four architectural approaches are the same](./assets/figure34.7.jpg)

Figure 34.7 All four architectural approaches are the same

In the “package by layer” approach, the `OrdersService` and `OrdersRepository` interfaces need to be `public`, because they have inbound dependencies from classes outside of their defining package. In contrast, the implementation classes (`OrdersServiceImpl` and `JdbcOrdersRepository`) can be made more restrictive (package protected). Nobody needs to know about them; they are an implementation detail.

In the “package by feature” approach, the `OrdersController` provides the sole entry point into the package, so everything else can be made package protected.

Nothing else in the code base,... ...can access information related to orders unless they go through the controller. This may or may not be desirable.

In the ports and adapters approach, the `OrdersService` and `Orders` interfaces have inbound dependencies from other packages, so they need to be made `public`.

![Figure 34.8 Grayed-out types are where the access modifier can be made more restrictive](./assets/figure34.8.jpg)

Figure 34.8 Grayed-out types are where the access modifier can be made more restrictive

In the “package by component” approach, the `OrdersComponent` interface has an inbound dependency from the controller, but everything else can be made package protected.

The fewer `public` types you have, the smaller the number of potential dependencies.

To be absolutely clear, what I’ve described here relates to a monolithic application, where all of the code resides in a single source code tree. If you are building such an application... ...I would certainly encourage you to lean on the compiler to enforce your architectural principles, rather than relying on self-discipline and post-compilation tooling.

### Other Decoupling Modes

Other ways that you can decouple your source code dependencies... ...module frameworks like OSGi and the new Java 9 module system... ...you can make a distinction between types that are `public` and types that are _published._

You could create an `Orders` module where all of the types are marked as `public`, but publish only a small subset of those types for external consumption.

Another option is to decouple your dependencies at the source code level, by splitting code across _different source code trees._

Ports and adapters example,... ...three source code trees:
- The source code for the business and domain (i.e., everything that is independent of technology and framework choices): `OrdersService`, `OrdersServiceImpl`, and `Orders`
- The source code for the web: `OrdersController`
- The source code for the data persistence: `JdbcOrdersRepository`

The latter two source code trees have a compile-time dependency on the business and domain code, which itself doesn’t know anything about the web or the data persistence code. From an implementation perspective, you can do this by configuring separate modules or projects in your build tool.

This is very much an idealistic solution, though, because there are real-world performance, complexity, and maintenance issues associated with breaking up your source code in this way.

A simpler approach... ...for ports and adapters code is to have just two source code trees:
- Domain code (the “inside”)
- Infrastructure code (the “outside”)
This maps on nicely to the diagram (Figure 34.9) that many people use to summarize the ports and adapters architecture, and there is a compile-time dependency from the infrastructure to the domain.

![Figure 34.9 Domain and infrastructure code](./assets/figure34.9.jpg)

Figure 34.9 Domain and infrastructure code

The “Périphérique anti-pattern of ports and adapters.”... ...Having all of your infrastructure code in a single source code tree means that it’s potentially possible for infrastructure code in one area of your application (e.g., a web controller) to directly call code in another area of your application (e.g., a database repository), without navigating through the domain. This is especially true if you’ve forgotten to apply appropriate access modifiers to that code.

### Conclusion: The Missing Advice

Your best design intentions can be destroyed in a flash if you don’t consider the intricacies of the implementation strategy.

Think about how to map your desired design on to code structures, how to organize that code, and which decoupling modes to apply during runtime and compile-time. 

Leave options open where applicable, but be pragmatic, and take into consideration the size of your team, their skill level, and the complexity of the solution in conjunction with your time and budgetary constraints.

The devil is in the implementation details.

## Afterword

My professional career as a software developer began in the 1990s,... ...To get ahead, you had to learn about objects and components, about design patterns, and about the Unified Modeling Language (and its precursors).

Projects... ...started with long design phases, where detailed blueprints for our systems were laid out by “senior” programmers for more “junior” programmers to follow. Which, of course, they didn’t. Ever.

Every line of code contains at least one design decision, and therefore anyone who writes code has a much greater impact on the quality of the software than a PowerPoint jockey like me ever could.

I’m a programmer. I like programming. And the best way I’ve found to have a positive impact on code is to write it.

The dinosaurs of Big Architecture... ...were wiped out by the asteroid of Extreme Programming... ...and small, nimble Just-Enough-Design-Up-Front-with-Plenty-of-Refactoring mammals replaced us. Software architecture became responsive. Well, that was the theory, anyway.

The problem with leaving architecture to programmers is that programmers have to be able to think like architects.

The way that software is structured can have a profound impact on our ability to keep adapting and evolving it, even in the short term.

Every design decision needs to leave the door open for future changes.

Like playing pool, each shot isn’t just about sinking that ball; it’s also about lining up the next shot.

Writing working code that doesn’t block future code is a non-trivial skillset. It takes years to master.

New era of Fragile Architecture: designs that grew quickly to deliver value sooner, but that made sustaining that pace of innovation very difficult.

It’s all very well talking about “embracing change,” but if it costs $500 to change a line of code, change ain’t happening.

You’ve seen how it’s possible to write code that delivers value today without blocking future value tomorrow; the onus is on you to put in the practice so you can apply these principles to your own code.

To get the best from a book like this, you need to get practical.

Analyze your code and look for the kinds of problems Bob highlights, then practice refactoring the code to fix these problems.

Incorporate design principles and Clean Architecture into your development processes, so that new code is less likely to cause pain.

If you’re doing TDD, make a point of having a little design review after passing each test, and clean up as you go. (It’s way cheaper than fixing bad designs later.)

Talk about Clean Architecture... ...with your team... ...with the wider developer community. Quality is everybody’s business, and it’s important to reach a consensus about the difference between good and bad architecture.

Be mindful that most software developers are not very architecture-aware,... ...Once you’ve wrapped your head around Clean Architecture, take the time to wrap someone else’s head around it. Pay it forward.

While the technology landscape for developers evolves continuously, foundational principles like the ones described here rarely change.

The real journey starts here.

## PART VII Appendix

## Appendix A Architecture Archaeology

45-year journey through some of the projects I have worked on since 1970. Some... ...are interesting from an architectural point of view. Others... ...because of the lessons learned and because of how they fed into subsequent projects.

### Union Accounting System

These computers did not come with operating systems. They didn’t even come with file systems. What you got was an assembler. If you needed to store data on the disk, you stored data on the disk. Not in a file. Not in a directory. You figured out which track, platter, and sector to put the data into, and then you operated the disk to put the data there. Yes, that means we wrote our own disk driver.

We created an overlay system. Applications would be loaded from disk into a block of memory dedicated to overlays... ...Of course, when your UI runs at 30 characters per second, your programs spend a lot of time waiting. We had plenty of time to swap the programs in and off the disk to keep all of the terminals running as fast as they could go... ...We wrote a preemptive supervisor that managed the interrupts and IO. We wrote the applications; we wrote the disk drivers, the terminal drivers, the tape drivers, and everything else in that system. There was not a single bit in that system that we did not write. Though it was a struggle involving far too many 80-hour weeks, we got the beast up and running in a matter of 8 or 9 months.

### Laser Trim

Our product was a system that used relatively high-powered lasers to trim electronic components to very fine tolerances... ...The system would measure the resistance of the resistors, and then use a laser to burn off parts of the resistor, making it thinner and thinner until it reached the desired resistance value within a tenth of a percent or so.

The computer was an M365. This was in the days when many companies built their own computers: Teradyne built the M365 and supplied it to all its divisions. The M365 was an enhanced version of a PDP-8—a popular minicomputer of the day.

The operating system would prompt the user for the name of a program to run. Those programs were stored on the tape, just after the operating system.

The console was an ASCII CRT with green phosphors, 72 characters wide5 by 24 lines. The characters were all uppercase.

To edit a program, you would load the ED-402 Editor, and then insert the tape that held your source code. You would read one tape block of that source code into memory, and it would be displayed on the screen. The tape block might hold 50 lines of code. You would make your edits by moving the cursor around on the screen and typing in a manner similar to `vi`. When you were done, you would write that block onto a different tape, and read the next block from the source tape. You kept on doing this until you were done.

We printed our programs out on paper, marked all the edits by hand in red ink, and then edited our programs block by block by consulting our markups on the listing.

Our program was approximately 20,000 lines of code, and took nearly 30 minutes to compile.

The architecture of the program was typical for those days. There was a Master Operating Program, appropriately called “the MOP." Its job was to manage basic IO functions and provide the rudiments of a console "shell."

A special-purpose utility layer controlled the measurement hardware... ...The boundary between this layer and the MOP was muddled at best... ...To us, it was just some code that we added to the MOP in a highly coupled way.

Next came the isolation layer. This layer provided a virtual machine interface for the application programs, which were written in a completely different domain-specific data-driven language (DSL)... ...Our customers would write their laser trimming application programs in this language, and the isolation layer would execute them.

The boundaries in this application were soft at best... ...There were couplings everywhere. But that was typical of software in the early 1970s.

### Aluminum Die-Cast Monitoring

I began working at Outboard Marine Corporation (OMC)... ...OMC maintained a huge facility in Waukegan, Illinois, for creating die-cast aluminum parts for all of the company’s motors and products... ...OMC had purchased an IBM System/7—which was IBM’s answer to the minicomputer. They tied this computer to all the die-cast machines on the floor, so that we could count, and time, the cycles of each machine. Our role was to gather all that information and present it on 3270 green-screen displays.

The language was assembler. And, again, every bit of code that executed in this computer was code that we wrote. There was no operating system, no subroutine libraries, and no framework. It was just raw code.

From an architectural point of view, there’s not a lot to learn here except for one thing. The System/7 had a very interesting instruction called _set program interrupt_ (`SPI`). This allowed you to trigger an interrupt of the processor, allowing it to handle any other queued lower-priority interrupts. Nowadays, in Java we call this `Thread.yield()`.

### 4-TEL

In October 1976, having been fired from OMC, I returned to a different division of Teradyne—a division I would stay with for 12 years. The product I worked on was named 4-TEL. Its purpose was to test every telephone line in a telephone service area, every night, and produce a report of all lines requiring repair.

At first, the COLT computers did everything, including all the console communication, menus, and reports. The SAC was just a simple multiplexor that took the output from the COLTs and put it on a screen. The problem with this setup was that 30 cps is really slow. The testers didn’t like watching the characters trickle across the screen, especially since they were only interested in a few key bits of data. Also, in those days, the core memory in the M365 was expensive, and the program was big. The solution was to separate the part of the software that dialed and measured lines from the part that analyzed the results and printed the reports. The latter would be moved into the SAC, and the former would remain behind in the COLTs. This would allow the COLT to be a smaller machine, with much less memory, and would greatly speed up the response at the terminal, since the reports would be generated in the SAC.

So we embarked upon a project to replace the M365 with a microcomputer based on an 8085 μprocessor... ...My buddy CK and I translated the M365 assembly language program for the COLT into 8085 assembly language. This translation was done by hand and took us about 6 months. The end result was approximately 30K of 8085 code.

The 30K program was a single binary, 30K long. To burn the chips, we simply divided that binary image into 30 different 1K segments, and burned each segment onto the appropriately labeled chip. This worked very well, and we began to mass-produce the hardware and deploy the system into the field. But software is soft. Features needed to be added. Bugs needed to be fixed. And as the installed base grew, the logistics of updating the software by burning 30 chips per installation, and having field service people replace all 30 chips at each site became a nightmare.

We needed a way to make a change to the firmware without replacing all 30 chips every time. We brainstormed this issue for a while, and then embarked upon the “Vectorization” project. It took me three months. The idea was beautifully simple. We divided the 30K program into 32 independently compilable source files, each less than 1K. At the beginning of each source file, we told the compiler in which address to load the resulting program... ...Also at the beginning of each source file, we created a simple, fixed-size data structure that contained all the addresses of all the subroutines on that chip... ...Next, we created a special area in RAM known as the vectors. It contained 32 tables of 40 bytes—exactly enough RAM to hold the pointers at the start of each chip. Finally, we changed every call to every subroutine on every chip into an indirect call through the appropriate RAM vector. When our processor booted, it would scan each chip and load the vector table at the start of each chip into the RAM vectors. Then it would jump into the main program. This worked very well. Now, when we fixed a bug, or added a feature, we could simply recompile one or two chips, and send just those chips to the field service engineers. We had made the chips _independently deployable._ We had invented polymorphic dispatch. We had invented objects. This was a plugin architecture, quite literally. We plugged those chips in.

One unexpected side benefit of the approach was that we could patch the firmware over a dial-up connection... ...This was a great boon to our field service operation, and to our customers. If they had a problem, they didn’t need us to ship new chips and schedule an urgent field service call. The system could be patched, and a new chip could be installed at the next regularly scheduled maintenance visit.

### The Service Area Computer

#### Dispatch Determination

One of the economic foundations for this system was based on the correct allocation of repair craftsmen... ...When a customer complained about a problem, our system could diagnose that problem and determine which kind of craftsman to dispatch. This saved the phone companies lots of money because incorrect dispatches meant delays for the customer and wasted trips for the craftsmen.

The code that made this dispatch determination was designed and written by someone who was very bright, but a terrible communicator. The process of writing the code has been described as “Three weeks of staring at the ceiling and two days of code pouring out of every orifice of his body—after which he quit."

In the end, our management simply told us to lock that code down and never modify it. That code became _officially rigid._ This experience impressed upon me the value of good, clean code.

#### Architecture

There was no isolation of device control logic, or UI logic, from the business rules of the system. For example, modem control code could be found smeared throughout the bulk of the business rules and UI code. There was no attempt to gather it into a module or abstract the interface. The modems were controlled, at the bit level, by code that was scattered everywhere around the system. The same was true for the terminal UI. Messages and formatting control code were not isolated. They ranged far and wide throughout the 60,000-line code base.

When we got the new modem, the control structured was entirely different... ...we were mixing old and new modems in our systems. The software needed to be able to handle both kinds of modems at the same time. Were we doomed to surround every place in the code that manipulated the modems with flags and special cases? There were hundreds of such places! In the end, we opted for an even worse solution. One particular subroutine wrote data to the serial communication bus that was used to control all our devices, including our modems. We modified that subroutine to recognize the bit patterns that were specific to the old modem, and translate them into the bit patterns needed by the new modem.

It was because of this fiasco that I learned the value of isolating hardware from business rules, and of abstracting interfaces.

#### The Grand Redesign in the Sky

The goal was the total and complete redesign of the SAC in C and UNIX on our own,... ...It took years, then more years, and then even more years... ...I believe I had left the company by then (1988). Indeed, I’m not at all sure it ever was deployed... ...it is very difficult for a redesign team to catch up with a large staff of programmers who are actively maintaining the old system.

#### Europe

At about the same time that the SAC was being redesigned in C, the company started to expand sales into Europe. They could not wait for the redesigned software to be finished, so of course, they deployed the old M365 systems into Europe... ...So one of our best programmers was sent to the United Kingdom to lead a team of U.K. developers to modify the SAC software to deal with all these European issues... ...These U.K. developers simply forked the U.S.-based code and modified it as needed... ...Bugs were found on both sides of the Atlantic that needed repair on the other side. But the modules had changed significantly, so it was very difficult to determine whether the fix made in the United States would work in the United Kingdom... ...a serious attempt was made to integrate these two forks back together again, making the differences a matter of configuration. This effort failed... ...The two code bases, though remarkably similar, were still too different to reintegrate—especially in the rapidly changing market environment that existed at that time.

#### SAC Conclusion

Many of the hard lessons of my software life were learned while immersed in the horrible assembler code of the SAC.

### C Language

Our lead _hardware_ engineer convinced our CEO that we needed a _real_ computer... ...When the manuals arrived, many months before the delivery of the machine, I took them home and devoured them... ...I helped to write the purchase order... ...When the machine arrived, I spent several days setting it up, wiring all the terminals, and getting everything to work. It was a joy—a labor of love... ...We built a cross- compilation system that allowed us to download compiled binaries from the PDP-11 to our 8085 development environments, and ROM burners. And—Bob’s your Uncle—it all worked like a champ.

#### C

The problem of still using 8085 assembler... ...I had heard that there was this “new” language that was heavily used at Bell Labs. They called it “C.” So I purchased a copy of _The C Programming Language_ by Kernighan and Ritchie... ...I _inhaled_ this book... ...It sacrificed none of the power of assembly language, and provided access to that power with a much more convenient syntax. I was sold... ...Now the only problem was convincing a group of embedded assembly language programmers that they should be using C.

### BOSS

we needed a simple task switcher for the 8085. So I conceived of BOSS: Basic Operating System and Scheduler. The vast majority of BOSS was written in C. It provided the ability to create concurrent tasks.

It was a simple, nonpreemptive task switcher. This software became the basis for a vast number of projects over the following years.

### pCCU

The late 1970s and early 1980s were a tumultuous time for telephone companies. One of the sources of that tumult was the digital revolution... ...the phone companies embarked upon the process of replacing their old analog central switching equipment with modern digital switches... ...We promised the phone companies that we would have this new architecture working in time for their transition. We knew they were months, if not years away, so we did not feel rushed.

#### The Schedule Trap

As time went on, we found that there were always urgent matters that required us to postpone development of the CCU/CMU architecture. We felt safe about this decision because the phone companies were consistently delaying the deployment of digital switches... ...Then came the day that my boss called me into his office and said: _“One of our customers is deploying a digital switch next month. We have to have a working CCU/CMU by then.”_... ...as my boss explained to me, we did not actually need a CCU/CMU. What we needed was a simple computer at the central office connected by modem lines to two standard COLTs at the distribution points... ...Thus was born the pCCU. This was the first product written in C and using BOSS that was deployed to a customer. It took me about a week to develop. There is no deep architectural significance to this tale, but it makes a nice preface to the next project.

### DLU/DRU

We had remote terminal capability, but it was based on modems, and in the early 1980s modems were generally limited to 300 bits per second. Our customers were not happy with that slow speed. High-speed modems were available, but they were very expensive... ...Our customers demanded a solution. Our response was DLU/DRU. DLU/DRU stood for “Display Local Unit” and “Display Remote Unit.” The DLU was a computer board that plugged into the SAC computer chassis and pretended to be a terminal manager board... ...We even had to invent our own communications protocol because, in those days, standard communications protocols were not open source shareware. Indeed, this was long before we had any kind of Internet connection.

#### Architecture

The architecture of this system was very simple, but there are some interesting quirks I want to highlight. First, both units used our 8085 technology, and both were written in C and used BOSS. But that’s where the similarity ended... ...The architecture of the DLU was based on a dataflow model. Each task did a small and focused job, and then passed its output to the next task in line, using a queue. Think of a pipes and filters model in UNIX. The architecture was intricate. One task might feed a queue that many others would service. Other tasks would feed a queue that just one task would service. Think of an assembly line. Each position on the assembly line has a single, simple, highly focused job to perform. Then the product moves to the next position in line. Sometimes the assembly line splits into many lines. Sometimes those lines merge back into a single line. That was the DLU... ...DRU used a remarkably different scheme. He created one task per terminal, and simply did the entire job for that terminal in that task. No queues. No data flow. Just many identical large tasks, each managing its own terminal.This is the opposite of an assembly line. In this case the analogy is many expert builders, each of whom builds an entire product... ...In the end, of course, both worked quite well. And I was left with the realization that software architectures can be wildly different, yet equally effective.

### VRS

As the 1980s progressed, newer and newer technologies appeared. One of those technologies was the computer control of _voice._ One of the features of the 4-Tel system was the ability of the craftsman to locate a fault in a cable. The procedure was as follows:
- The tester, in the central office, would use our system to determine the approximate distance, in feet, to the fault.
- The cable repair craftsman, upon arrival, would call the tester and ask to begin the fault location process.
- The tester would tell the craftsman which operations the system wanted, and the craftsman would tell the tester when the operation was complete.
- After two or three such interactions, the system would calculate a new distance to the fault. The cable craftsman would then drive to that location and begin the process again.
Imagine how much better that would be if the cable craftsmen, up on the pole or standing at a pedestal, could operate the system themselves. And that is exactly what the new voice technologies allowed us to do. The cable craftsmen could call directly into our system, direct the system with touch tones, and listen to the results being read back to them in a pleasant voice.

#### The Name

The company held a little contest to select a name for the new system. One of the most creative of the names suggested was SAM CARP... ...“Still Another Manifestation of Capitalist Avarice Repressing the Proletariat.”... ...Another was the Teradyne Interactive Test System... ...Still another was Service Area Test Access Network... ...The winner, in the end, was VRS: Voice Response System.

#### Architecture

These were the heady days of microcomputers, UNIX operating systems, C, and SQL databases. We were determined to use them all. From the many database vendors out there, we eventually chose UNIFY... ...supported a new technology called _Embedded SQL._ This technology allowed us to embed SQL commands, as strings, right into our C code. And so we did—everywhere.

In those days SQL was hardly a solid standard... ...So the special SQL and special UNIFY API calls were also smeared throughout the code. This worked great! The system was a success. The craftsmen used it, and the telephone companies loved it. Life was all smiles. Then the UNIFY product we were using was cancelled. Oh. Oh. So we decided to switch... ...we had to search through all that C code, find all the embedded SQL and special API calls, and replace them with corresponding gestures for the new vendor. After three months of effort or so, we gave up. We couldn’t make it work. We were so coupled to UNIFY that there was no serious hope of restructuring the code at any practical expense. So, we hired a third party to maintain UNIFY for us, based on a maintenance contract. And, of course, the maintenance rates went up year after year after year.

#### VRS Conclusion

Databases are details that should be isolated from the overall business purpose of the system.

I don’t like strongly coupling to third-party software systems.

### The Electronic Receptionist

When you called a company, ER would answer and ask you who you wanted to speak with. You would use touch tones to spell the name of that person, and ER would then connect you. The users of ER could dial in and, by using simple touch-tone commands, tell it which phone number the desired person could be reached at, anywhere in the world. In fact, the system could list several alternate numbers.

When you called ER and dialed RMART (my code), ER would call the first number on my list. If I failed to answer and identify myself, it would call the next number, and the next. If I still wasn’t reached, ER would record a message from the caller. ER would then, periodically, try to find me to deliver that message, and any other message left for me by anyone else. This was the first voice mail system ever, and we held the patent to it. We built all the hardware for this system—the computer board, the memory board, the voice/telecom boards, everything. The main computer board was _Deep Thought,_ the Intel 80286 processor that I mentioned earlier.

The architecture of this system would today be called _service oriented._ Each telephone line was monitored by a listener process running under MP/M. When a call came in, an initial handler process was started and the call was passed to it. As the call proceeded from state to state, the appropriate handler process would be started and take control. Messages were passed between these services through disk files. The currently running service would determine what the next service should be; would write the necessary state information into a disk file; would issue the command line to start that service; and then would exit.

This was the first time I had built a system like this... ...Everything having to do with software was mine—and it worked like a champ... ...The services were independently deployable, and lived within their own domain of responsibility. There were high-level processes and low-level processes, and many of the dependencies ran in the right direction.

#### ER Demise

Unfortunately, the marketing of this product did not go very well. Teradyne was a company that sold test equipment. We did not understand how to break into the office equipment market. After repeated attempts over two years, our CEO gave up.

### Craft Dispatch System

ER had failed as a product, but we still had all this hardware and software that we could use to enhance our existing product lines... ...we should offer a voice response system for interacting with telephone craftsmen that did not depend on our test systems. Thus was born CDS, the Craft Dispatch System... ...When a problem was discovered in a phone line, a trouble ticket was created in the service center. Trouble tickets were kept in an automated system. When a repairman in the field finished a job, he would call the service center for the next assignment. The service center operator would pull up the next trouble ticket and read it off to the repairman. We set about to automate that process. Our goal was for the repairman in the field to call into CDS and ask for the next assignment. CDS would consult the trouble ticket system, and read off the results. CDS would keep track of which repairman was assigned to which trouble ticket, and would inform the trouble ticket system of the status of the repair.

I set about to create what would now be called a _micro-service architecture._ Every state transition of any call, no matter how insignificant, caused the system to start up a new service. Indeed, the state machine was externalized into a text file that the system read. Each event coming into the system from a phone line turned into a transition in that finite state machine. The existing process would start a new process dictated by the state machine to handle that event; then the existing process would either exit or wait on a queue. This externalized state machine allowed us to change the flow of the application without changing any code (the Open-Closed Principle). We could easily add a new service, independently of any of the others, and wire it into the flow by modifying the text file that contained the state machine. We could even do this while the system was running. In other words we had _hot-swapping_ and an effective BPEL (Business Process Execution Language).

On an airplane, flying between customer visits, I invented a scheme that I called FLD: _Field Labeled Data._ Nowadays we would call this XML or JSON. The format was different, but the idea was the same. FLDs were binary trees that associated names with data in a recursive hierarchy. FLDs could be queried by a simple API, and could be translated to and from a convenient string format... ...So, micro-services communicating through shared memory analog of sockets using an XML analog—in 1985. There is nothing new under the Sun.

### Clear Communications

In 1988... ...Our mission was to build the software for a system that would monitor the communications quality of T1 lines—the digital lines that carried long- distance communications across the country. The vision was a huge monitor with a map of the United States crisscrossed by T1 lines flashing red if they were degrading.

Graphical user interfaces were brand new in 1988. The Apple Macintosh was only five years old. Windows was a joke back then. But Sun Microsystems was building Sparcstations that had credible X-Windows GUIs. So we went with Sun—and therefore with C and UNIX.

This was a startup. We worked 70 to 80 hours per week. We had the vision. We had the motivation. We had the will. We had the energy. We had the expertise. We had equity. We had dreams of being millionaires. We were full of shit.

Architecture? Are you joking? This was a startup. We didn’t have time for _architecture._ Just code, dammit! _Code for your very lives!_ So we coded. And we coded. And we coded. But, after three years, what we failed to do was sell. Oh, we had an installation or two. But the market was not particularly interested in our grand vision, and our venture capital financiers were getting pretty fed up. I hated my life at this point.

#### The Setup

Sun released a C++ compiler... ...I left the 3000-line C functions behind, and started to write C++ code at Clear. And I learned ... I read books... ...But perhaps most significantly of all, I read Object Oriented Design with Applications by Grady Booch... ...As I learned, I also began debating on Netnews, the way people now debate on Facebook. My debates were about C++ and OO... ...It was in one of those debates that the foundations of the SOLID principles were laid.
And all that debating, and perhaps even some of the sense, got me noticed ...

#### Uncle Bob

One of the engineers at Clear... ...gave nicknames to everyone. He called me Uncle Bob... ...he was making an offhand reference to [J. R. “Bob” Dobbs](https://en.wikipedia.org/wiki/J._R._%22Bob%22_Dobbs)

#### The Phone Call

It was a recruiter. He had gotten my name as someone who knew C++ and object-oriented design... ...He said he had an opportunity in Silicon Valley, at a company named Rational. They were looking for help building a CASE tool... ...This was _Grady Booch’s_ company. I saw before me the opportunity to join forces with _Grady Booch!_

### ROSE

A tool that allowed programmers to draw Booch diagrams—the diagrams that Grady had written about in _Object-Oriented Analysis and Design with Applications_ (Figure A.9 shows an example).

![Figure A.9 A Booch diagram](./assets/figureA.9.jpg)

Figure A.9 A Booch diagram

The Booch notation was very powerful. It presaged notations like UML.

We also fell for one of the most unfortunate fads of the day—we used a so-called object-oriented database.

This was one of the most intellectually stimulating experiences of my professional life.

#### The Debates Continued

With Grady’s help, I started working on my first book: _Designing Object-Oriented C++ Applications Using the Booch Method._

No one was calling me “Uncle Bob.”... ...So I made the mistake of putting “Uncle Bob” in my email and Netnews signatures. And the name stuck. Eventually I realized that it was a pretty good brand.

#### ... By Any Other Name

ROSE... ...enforced dependency rule... ...is not the rule that I have described in this book. We did _not_ point our dependencies toward high-level policies. Rather, we pointed our dependencies in the more traditional direction of flow control. The GUI pointed at the representation, which pointed at the manipulation rules, which pointed at the database. In the end, it was this failure to direct our dependencies toward policy that aided the eventual demise of the product.

Object-oriented databases were a relatively new idea, and the OO world was all abuzz with the implications. Every object-oriented programmer wanted to have an object-oriented database in his or her system. The idea was relatively simple, and deeply idealistic. The database stores objects, not tables.

That database was probably our biggest practical mistake. We wanted the magic, but what we got was a big, slow, intrusive, expensive third-party framework that made our lives hell by impeding our progress on just about every level.

Great architectures sometimes lead to great failures. Architecture must be flexible enough to adapt to the size of the problem. Architecting for the enterprise, when all you really need is a cute little desktop tool, is a recipe for failure.

### Architects Registry Exam

In the early 1990s, I became a true consultant... ...My consulting was focused strongly on the design and architecture of object-oriented systems.
One of my first consulting clients was Educational Testing Service (ETS)... ...to conduct the registration exams for new architect candidates... ...The candidate might be given a set of requirements for a public library, or a restaurant, or a church, and then asked to draw the appropriate architectural diagrams. The results would be collected and saved until such time as a group of senior architects could be gathered together as jurors, to score the submissions. These gatherings were big, expensive events and were the source of much ambiguity and delay.

ETS had broken the problem down into 18 individual test vignettes. Each would require a CAD-like GUI application that the candidate would use to express his or her solution. A separate scoring application would take in the solutions and produce scores.

My partner, Jim Newkirk, and I realized that these 36 applications had vast amounts of similarity... ...were determined to develop a reusable framework... ...Indeed, we sold this idea to ETS by saying that we’d spend a long time working on the first application, but then the rest would just pop out every few weeks. At this point you should be face-palming or banging your head on this book. Those of you who are old enough may remember the “reuse” promise of OO. We were all convinced, back then, that if you just wrote good clean object-oriented C++ code, you would just naturally produce lots and lots of reusable code.

The first application... ...was called Vignette Grande... ...It took us a year... ...We delivered this product to ETS, and they contracted with us to write the other 17 applications post-haste... ...But something went wrong. We found that the reusable framework we had created was not particularly reusable. It did not fit well into the new applications being written... ...We went to ETS and told them that there would be a delay... ...So we began again. We set the old framework aside and began writing four new vignettes simultaneously. We would borrow ideas and code from the old framework but rework them so that they fit into all four without modification. This effort took another year. It produced another 45,000-line framework, plus four vignettes that were on the order of 3000 to 6000 lines each.

The relationship between the GUI applications and the framework followed the Dependency Rule. The vignettes were plugins to the framework. All the high-level GUI policy was in the framework. The vignette code was just glue. The relationship between the scoring applications and the framework was a bit more complex. The high-level scoring policy was in the vignette. The scoring framework plugged into the scoring vignette.

We met our dates and our commitments. Our customer was happy. We were happy. Life was good. But we learned a good lesson: You can’t make a reusable framework until you first make a usable framework. Reusable frameworks require that you build them in concert with _several_ reusing applications.

You can’t make a reusable framework until you first make a usable framework. Reusable frameworks require that you build them in concert with _several_ reusing applications.

### Conclusion

this appendix is somewhat autobiographical... ...I mentioned a few episodes that were not exactly relevant to the technical content of this book, but were significant nonetheless. Of course, this was a partial history. There were many other projects that I worked on over the decades... ...My hope is that you enjoyed this little trip down my memory lane; and that you were able to learn some things along the way.<hr/><br/>[Read:](Read/index.md) [2020](Read/2020.md)<br/>[Genre:](Genre/index.md) [Good Practices](Genre/Good%20Practices.md) [Software Development](Genre/Software%20Development.md)