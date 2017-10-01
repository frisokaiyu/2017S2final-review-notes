## Mid-Term Review – W1,2
### 1. What is software architecture? Why is it important?
The software architecture of a system is the set of structures needed to reason about the system, which comprise--包含 software element, relations among them, and properties of both. (Clements, Bass, Kazman 2012)

#### The architecture is a carrier of the earliest design decisions.
- An architecture will inhibit a system’s driving quality attributes and the early prediction.
- Provides reasoning about managing changes.
- An architecture will improve cost and schedule estimates.
- Architecture-based development focuses on the assembly of components
- A documented architecture enhances communication among stakeholders.
- An architecture is a transferable and reusable model.

### 2. In what phases of software development does architecture play a crucial role?

#### During inception and design
- Facilitates system consistency and simplifies design
- Helps predict key system qualities.
- Helps identify requirements!
#### During implementation
- Helps identification and allocation of development work
- Guides finer-grained design decisions
#### During maintenance and system evolution
- Reduces likelihood of architectural decay during fine-grained maintenance
- Identifies feasibility and potential cost of potential evolution alternatives 

### 3. What is meant by “architectural decay” and what causes it?

The gradual corruption of architectural design decisions through seemingly minor fixes and modifications.

#### Architectural decay is due to two principal factors:
- The difficulty of comprehending an architecture by observing details
- The difficulty of enforcing architectural design decisions in the process of implementation 

### 4. What is a model? What is a software model?
**A Model**：
- is a representation of a part of function, structure, behaviour of a system
- is a simplification of a system
- information, abstraction, specification
- can answer question in place of actual system
- inference, prediction
- is used for a purpose planning, design, risk analysis, testing 

#### Software model: An engineering model (specified using a modeling language) of some software that represents:
- Design-time views of the software: The structure and content of the software specification
- Run-time views of the software: the structure and behavior of the software in execution 

### 5. What are the primary reasons for constructing models in engineering?
- To understand the interesting characteristics of an existing or desired (complex) system and its environment
- To predict the interesting characteristics of the system by analysing its model(s)
- To communicate their understanding and design intent (to others and to oneself)
- To specify the implementation of the system (models as blueprints) 

### 6. What is the unique feature of software model?
Software has the unique property that it allows us to directly evolve models into implementations without fundamental discontinuities in the expertise, tools, or methods! 

### 7. What is meant by the term “platform independence”?
A highly desirable objective
- Separation of concerns: focus on the functionality and behaviour of a system
- Enables portability 

## Mid-Term Review – W3

### 1. What is software requirements engineering?
The process of discovering **the purpose** of a **software system** by identifying stakeholders and their needs and documenting these in a form that is amenable to analysis, communication, and subsequent implementation.
- Eliciting requirements
- Modelling and analysing requirements
- Communicating requirements
- Agreeing requirements
- Evolving requirements 

### 2. What are the common issues in requirement statement?
- Ambiguity
- Incompleteness
- Conflict
- Difference in priority
- Perceived stakeholders urgency to realise. 

### 3. What are the common approaches to specify requirements?

#### “Ad hoc” analysis
- Mixture of different kinds of requirements (what, how, how well, etc.);
- Unsystematic, informal, and error prone (omissions, conflicts, inconsistencies, ambiguities);
- However, usually, the most common starting point.
### Feature analysis
- System viewed as a collection of desired properties (features);
- A capability-based view of a system.
#### Use case analysis
- System viewed as a set of functional capabilities that realize desired stakeholder goals;
- An operational view of a system;
- A pragmatic combination of all three is often the best approach.

### 4. Why informal software requirement specification is not sufficient?
#### The informal nature of the text makes it difficult:
- To identify potential conflicts and inconsistencies between requirements
- To determine any interdependencies between individual requirements
- To ensure all requirements are covered
- To understand precisely what needs to be implemented
- To trace requirements to implementation and vice verse
- To provide a basis for comprehensive testing
- Need a more systematic and more precise approach to requirements specification
- Also, need requirements in electronic form for easier manipulation (searching, linking, tracing)

### 5. What are the differences between functional and nonfunctional requirements?
It is common practice to categorize requirements as being either **functional** or **non-functional**:

#### Common rationale: functional => what ::: non-functional = how well.
- A functional requirement describes what a software system should do, while non-functional requirements place constraints on how the system will do so.
- functional requirements related to the system functionalities.
- non-functional requirements related to the system’s performance characteristics, such as accessibility, reliability.
- But, for very many systems, these are not always separable concerns. E.g., “Compute the optimal route for a data packet” and “Compute the optimal route for a data packet in 4 sec” can be two very different. 

### 6. What is Use Case?
**Use case**: a collection of possible interactions between actors and a system relating to one or more goals:
- Give context of requirements
- Facilitate agreement
- Being a collection of possible scenarios, a use case is similar to a class 

### 7. What are the key elements in "Cockburn’s Use Case" Approach?
#### Use cases are motivated by (and defined around) actor goals:
- Use cases start with an action by an actor (trigger)
- Use cases always terminate with a clear result: the desired goal has or has not been achieved
- Success scenarios (usually one “main”success scenario)
- Failure scenarios: complications
- In general, each step in a scenario can succeed or fail
- The condition that led to a step heads the corresponding failure scenario
- Failure scenarios branch off from the point of failure 

## Mid-Term Review – W4
### 1. What is architecture of a system?
The fundamental concepts or properties of a system in its environment embodied in its elements, relationships, and in the principles of its design and evolution.
 
### 2. What are the viewpoints used in "Kruchten’s" “4+1” approach? Which of these viewpoints are independent of the underlying implementation technology?
**4 views that capture the system + 1 that captures the requirements**
- Each view describes different aspects of the system
- Full system specification is obtained by a union of the individual views
- **Logical Viewpoint:**
What the system does specified by an abstract design model (e.g., classes and associations, subsystems, etc.)
- **Process Viewpoint:**
Concurrency aspects of the system (tasks, threads, processes) and related system interactions
- **Implementation Viewpoint:**
The organization of the implementation artifacts (packages, executable, etc.) in the development environment
- **Deployment Viewpoint:**
Mapping of run-time implementation artifacts to the underlying platforms or computing nodes.
- **Use-Case View(point):**
Key use cases that drive the architecture 

### 3. What are the viewpoints used in "Seimens approach"?
- **Conceptual Viewpoint:**
Application-oriented specification of a system’s components, their functionality and interconnections
- **Module Viewpoint:**
Grouping of conceptual view components into development environment entities (e.g., modules and subsystems)
- **Execution Viewpoint:**
Mapping of modules to platform specific runtime entities (threads, processes, etc.) and the hardware
- **Code Viewpoint:**
The allocation and deployment of module view entities to actual platform entities.

### 4. Which of these viewpoints are design-time viewpoints and runtime viewpoints?
- Design-time view:
The static organization of the system specification in a design repository 
- Run-time view:
The dynamic organization of instances created by an executing computer program (a specification)

### 5. What is control behaviour in architecture? What are the main design principles?

**Control behavior** is often treated in an ad-hoc manner, since it is not part of the primary system functionality, typically retrofitted into the framework optimized for the functional behavior.

**Separate control from function:**
- separate control components from functional components
- separate control from functional interfaces

**Centralize control (decision making):**
- if possible, focus control in one component place control policies in the control components and control mechanisms inside the controlled components 

### 6. Why are architectural design patterns important?
Defines types of elements and relationships that work together in order to solve a particular problem from some perspective (viewpoints).
- Recurring common situation – the context
- The problem that arises in the given context.
- Reused solution to a recurring design problem 
- General solution to common problem (importance)
**Abstraction**+ **Minimal changes**+ **General structure**.

### 7. Name four architectural design patterns?
- Data-flow
- Shared-data
- Layering
- Service-oriented
- Model-View-Controller 

## Mid-Term Review – W5,6

### 1. What does structure modeling deal with?
Structure modeling deals with the representation of entities that take up space (ultimately, physical) and, which have state and may have behaviour：
- Specifically, modeling of Run-time instances (e.g., objects) and their relationships (e.g., links) and 
- Specifications of those run-time entities (e.g., classes, collaborations) and relationships (e.g., associations)
- In UML: two categories of structural entities
1) Elementary
2) Structured (for modeling architectures) 

### 2. What is classifier in UML?
A **classifier** is a specification of a collection of entities (things, concepts, etc.) that Share a set of characteristics (features) and which Can be classified (divided) into sub-collections according to the nature of some of their characteristics. E.g., people can be classified based on their gender into men and women or, they may be classified according to their age into adults and children.

#### Kinds of Classifiers in UML:
Classes, Associations, AssociationClasses, DataTypes, Enumerations, Interfaces, Behaviors (Activities, Interactions, StateMachines), Signals, UseCases, Collaborations, Components, Nodes, etc. 

### 3. What does collaboration represent in structure modeling?
Describes a set of collaborating roles communicating via connectors (representing communication links) 

### 4. What is the difference between Active Object and Passive Object?
**Passive objects** respond whenever an operation (or reception) of theirs is invoked;
NB: invocations may be concurrent ⇒ conflicts possible!
**Active objects** run concurrently and respond only when they execute a “receive” action

### 5. What is the difference between Action and Activity in UML?

**Action** is a named element which represents a single atomic step within activity, i.e. that is not further decomposed within the activity.
**Activity** represents a behavior that is composed of individual elements that are actions.
Actions are denoted by round cornered rectangles.
Name of the action is usually action verb or noun for the action with some explanation. 

### 6. What are the often used diagrams for modeling behaviors?
- Sequence diagram
- Communication diagram
- Interaction overview diagram 

## Mid-Term Review – W7,8
### 1. What is Namespace?
A namespace is a collection of owned model elements that may be identified by their names
- The features (attributes, operations, etc.) of a Class;
- Many different manifestations of the namespace concept in UML: Package, Class, State, Behaviour, etc. 

### 2. What is Meta model?
A model that specifies the abstract syntax of that modeling language and defines the rules for well-formed models independently of the concrete syntax. 

### 3. What is Meta Modeling Language?
#### Meta model and Meta Modeling Language:
![metamodel01.png](https://github.com/frisokaiyu/2017S2final-review-notes/blob/master/metamodel01.png)
![metamodel02.png](https://github.com/frisokaiyu/2017S2final-review-notes/blob/master/metamodel02.png)
![metamodel03.png](https://github.com/frisokaiyu/2017S2final-review-notes/blob/master/metamodel03.png)
![metamodel04.png](https://github.com/frisokaiyu/2017S2final-review-notes/blob/master/metamodel04.png)
![metamodel05.png](https://github.com/frisokaiyu/2017S2final-review-notes/blob/master/metamodel05.png)
![metamodel06.png](https://github.com/frisokaiyu/2017S2final-review-notes/blob/master/metamodel06.png)

### 4. What is Abstract Syntax and Concrete Syntax in UML?
**(1) Abstract Syntax**
- Concepts, their features, and mutual relationships
- Described by a MOF metamodel + additional constraints
**(2) Concrete Syntax**
- Notation (diagrams, text, tables, graphical representation)
- UML concrete syntax definition is incomplete and informally defined
**(3) Language Semantics**
- The meaning of UML models and the concepts used to express them
- English (+ UML model + mathematical model) 

### 5. How to specialize UML?
UML has a built-in language specialization kit: the **profile mechanism**. It allows domain-specific interpretations of UML models which are compatible with general (standard) UML, which implies the ability to reuse UML tools, expertise, etc.
 
### 6. What is UML profile? How is it defined?
(1) A profile in UML provides a generic extension mechanism for customizing UML models for particular domains and platforms.<br \>
(2) Profiles are defined using stereotypes, tag definitions and constraints.<br \>
(3) Profiles can be used for two different purposes:
- To define a domain-specific modeling language;
- To define a domain-specific viewpoint that can be overlaid onto an existing model = a way of reinterpreting the original model.<br \>
(4) A profile customizes UML for a particular domain.
- SysML: system engineering application;
- MARTE: real-time and embeded applications.

### 7. What is a stereotype in UML?
A stereotype allows designers to extend the vocabulary of UML in order to create new model elements, derived from existing one.
- Have specific properties suitable for a particular problem domain.
- Properties of a stereotype are referred to as tag definitions. 
