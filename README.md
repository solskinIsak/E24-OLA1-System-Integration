# OLA 2: Distributed Architecture – Modern Enterprise Architecture
 - Group: **TofuBytes**
 - Members: **Isak, Jamie & Helena**
## Objective
This assignment is focused on exploring the concepts of Enterprise and Solution Architecture as well as understanding the role of teams, integration patterns, and modern architectural practices. It also aims to provide a foundation for the exam project by allowing students to research relevant tools and technologies for building scalable, service-based enterprise applications.

---

## Table of Contents
1. [Overview](#overview)
2. [Study Materials](#study-materials)
3. [Assignment Questions](#assignment-questions)
   - [Q1: Enterprise vs Solution Architecture](#q1-enterprise-vs-solution-architecture)
   - [Q2: Role of Teams in Modern Architecture](#q2-role-of-teams-in-modern-architecture)
   - [Q3: Centralization in Architecture](#q3-centralization-in-architecture)
   - [Q4: ABCDE of Modern Architecture](#q4-abcde-of-modern-architecture)
   - [Q5: Continuous Conversation and DevOps](#q5-continuous-conversation-and-devops)
   - [Q6: Messaging Integration Patterns](#q6-messaging-integration-patterns)
   - [Q7: Messaging vs Conversation Architectures](#q7-messaging-vs-conversation-architectures)
   - [Q8: Pattern Languages](#q8-pattern-languages)
   - [Q9: Strangler Pattern](#q9-strangler-pattern)
   - [Q10: Core Architecture Diagrams](#q10-core-architecture-diagrams)
4. [Submission Guidelines](#submission-guidelines)
5. [Resources](#resources)

---

## Overview
This assignment focuses on the different aspects of modern enterprise architecture, including comparisons between enterprise and solution architectures, the role of teams, architectural centralization, and key integration patterns. The answers to the questions will provide a deep understanding of how to build and scale enterprise systems in distributed environments.

---

## Study Materials
Before answering the questions, ensure you have gone through the following resources:
- Moodle videos on Enterprise Architecture
- PowerPoint slides on Enterprise Architecture and Integration Patterns
- Suggested readings: *Team Topologies* by Matthew Skelton, *Enterprise Integration Patterns* by Gregor Hohpe, and the article by Simon Rohrer on modern enterprise architecture.

---

## Assignment Questions

### Q1: Enterprise vs Solution Architecture

So, from watching the video [Enterprise Architecture vs Solution Architecture](https://www.youtube.com/watch?v=v6xBGN2A0hM) he mentions that there are quite a few differences between **Enterprise Architecture (EA)** and **Solution Architecture (SA)** as far as we’ve been able to pick up. In frameworks he also mentions like TOGAF, architecture is split into four key levels. Three of these levels function within Enterprise Architecture:

1. **Strategic Architecture**
2. **Segment Architecture**
3. **Capability Architecture**

And then there’s the 4th level, which is **Solution Architecture**. Before diving into Solution Architecture, let’s go over the differences between these roles.

Enterprise Architecture, especially within the first three levels, is all about strategy, long-term planning, and ensuring that the technology systems align with the business’s overall objectives. Think of **Strategic Architecture** as the top-level vision, defining where the organization wants to go. Then, **Segment Architecture** breaks this down into different parts or "segments" of the business, each with its own needs but all aligned with that top-level strategy. Finally, **Capability Architecture** focuses on what the organization *can* do, identifying the core competencies it needs to develop to meet those strategic goals.

Now, when we get to **Solution Architecture**, the focus shifts from high-level planning to actual products and solutions. This is the stage where we specify the detailed implementation of the capabilities defined earlier in the enterprise architecture. Unlike the **Capability Architecture**, which defines what the organization needs to be capable of, **Solution Architecture** deals with the actual "how." It's where we start talking about the real-world systems and applications needed to deliver those capabilities.

For example, in **Enterprise Architecture**, you wouldn’t necessarily discuss the specific details of an application. You’d instead focus on ensuring the right capabilities are in place, like moving towards cloud computing or building strong data management systems. However, when we step into **Solution Architecture**, we’re no longer just talking strategy—we’re specifying which technologies, platforms, or applications are required to bring those capabilities to life. This is where the **Solution Architect** comes in, designing systems that align with the broader goals laid out by the enterprise architects.

In simple terms, **Enterprise Architecture** is about laying the roadmap, while **Solution Architecture** is about building the car that drives on that roadmap. EA operates at a higher, long-term strategic level, whereas SA gets into the nitty-gritty of delivering specific projects or products.

 ### When designing large-scale systems, Enterprise Architecture (EA) and Solution Architecture (SA) contribute at different levels but are both essential.
#### Enterprise Architecture (EA):
EA focuses on the strategic, long-term vision, ensuring that all technology systems align with business objectives. It defines company-wide principles, such as system integration, technology standards, and security requirements. In large-scale systems, EA sets the architectural framework, ensuring that the system will integrate seamlessly into the organization’s broader ecosystem.

#### Solution Architecture (SA):
SA operates on a project-specific level, designing the technical solutions for individual systems within the framework set by EA. It specifies the technology stack, APIs, and detailed functional requirements, ensuring the system meets the business needs while adhering to enterprise guidelines.

#### Collaboration:
EA provides the roadmap, while SA delivers the detailed solutions that fit within that roadmap. Together, they ensure systems are scalable, aligned with - business goals, and technically sound.

So to sum it up, **Enterprise Architecture** ensures the organization is heading in the right direction from a technology perspective. It defines the capabilities and frameworks that guide everything. **Solution Architecture**, on the other hand, takes those ideas and turns them into actionable solutions, detailing how specific technologies and systems will be implemented to meet the organization’s needs.



### Q2: Role of Teams in Modern Architecture
Stefan mentions in regard to role of teams in modern architecture he highlights the crucial role of team **organization** in modern architecture. 
Tilkov argues that successful architecture goes beyond technical solutions and emphasizes the importance of how teams are structured and how they collaborate. 
Essentially what he says is that he Values Explicit **Team-first approach** which is when you have larger teams of 50 or 25 people this Team-first idea enables the teams to do something that makes sense, that has purpose is the most motivating thing he continues.
He also Values that the book is completely **technology agnostic** meaning no need micro services to do and the ability to choose any other techonology choice. the Book doesn't try to sell you anything in that regard.
**Long-Lived teams instead of project thinking** is essentlially a shift form companies wherea project is something that is looked upon as an expection thats supposed to end as quickly as possible so you can get to the "state" of having no projects running. The shift he mentions is how the focus now is more on how "we" always can improve and always add new thing or features because the buisness is essentially depending on innovation within the services they support.
And finally how **the book focuses on actual experiences, research and collaboration** is a key point he values.

Stefan mentioned the book **Team Topologies.**
now, **what Team topologies does the book describe and do we agree with from our own experience that the team is a core part of a successfull project?**
Well, to build on that,the book describes four key team types:

1. **Stream-aligned Teams**: These teams are responsible for a specific stream of work, such as a particular product or service.
2. **Enabling Teams**: They focus on helping other teams gain skills and improve their capabilities without directly delivering software themselves.
3. **Complicated Subsystem Teams**: These handle complex or specialized subsystems that require deep technical expertise.
4. **Platform Teams**: They provide internal services and support, creating and maintaining the platforms used for software delivery.

The book also introduces three key interaction modes between teams:

1. **Collaboration**: Teams work closely together for short periods to achieve specific goals.
2. **X-as-a-Service**: One team provides a service to another, often with a formal service contract.
3. **Facilitation**: One team helps another improve its capabilities by offering guidance and support.

**From our own experience**, we can confirm that these concepts are somwhat spot on. Effective team organization and interactions are indeed central to project success and for the team chemistry. When teams are well-structured and collaborate effectively, they can address challenges more efficiently, share and leverage specialized knowledge, and deliver better outcomes. So, aligning team roles and interactions with the principles described in **Team Topologies** **can** greatly enhance the success of a project. That being said. Its not as easy as just saying we agree or disagree. Yes this is true to a degree that allows and enables such teams to develop and prosper but this also depends on the members of the team themselves. all these points can collapse if the team doesn't know how to synchronize or collaborate and grow as a team. Our experiences do infact lean on the agreeable side, as when speaking of school projects and exam projects Teams obviously (meaning us the students delivering the projects) is a core part of the successfull project if not integral.




### Q3: Centralization in Architecture 
***Stefan Tilkov explains why some things are best done centrally (for example at 23 min 30 seconds). Why do you think he is saying this? What does he claim are the benefits?***

From what we could gather from his [presentation](https://www.youtube.com/watch?v=BNTt2aLB1tg&t=7s), is what he means by this is that some things are best done centrally. He suggests that doing so helps address challenges in complex, large-scale systems and organizations. The key benefits he outlines were:

- **Consistency**: Ensuring uniform quality and standards across the organization.
- **Efficiency**: Reducing duplication and costs by managing resources centrally.
- **Specialization and Expertise**: Centralizing knowledge and skills to handle complex tasks.
- **Coordination**: Improving alignment and integration of complex systems.

Stefan also highlights how centralization can enable individuals or small teams to act independently and make quick, efficient decisions. This decentralized decision-making is possible because the core functions are centralized, allowing for more focused, consistent guidance across the organization.

Essentially, he advocates for centralizing specific areas to achieve consistency, efficiency, and specialization, ultimately improving quality, reducing costs, and enhancing security and coordination.

In summary, he thinks centralization is important because it ensures uniform quality and compliance with standards, enables more efficient use of resources, pools specialized expertise, and enhances coordination across different parts of the organization. This leads to better collaboration and smoother functioning within large systems and a happy Stefan (rip bless his soul).

### Q4: ABCDE of Modern Architecture
Do you find his arguments persuasive and if so why?

- A) **Aligning values, people, and technology.** This makes sense—if the whole team is aligned, it leads to better cooperation within the team and across areas of expertise, ensuring that all team members are on the same page.

- B) **Better, value, sooner, safer, happier.** "Better" means delivering the best possible quality of the product. In the video, he explains "value" as what makes you special. "Sooner" refers to learn faster and delivering value faster. "Safer" obviously refers to security and privacy. "Happier" means making everyone involved with the product happier, not just the customer, but also the employees and even the environment/climate.

- C) **Continuous Conversational Governance.** This is about having ongoing conversations about the architecture and involving every member in the discussion. This approach allows for a more agile design of the architecture.

- D) **DevOps at enterprise scale.** This refers to implementing DevOps on a large, enterprise-wide scale.

- E) **Evolutionary enterprise architecture.** This focuses on continuous improvement over time.

His arguments are persuasive, and even without having used them, they make a lot of sense. They focus heavily on community within the team and on CI/CD (continuous integration and continuous delivery/deployment).

### Q5: Continuous Conversation and DevOps
what ways does he say it benefits Saxo Bank? How does he connect the Continuous Conversation to the Devops Infinity Loop.

He says it helps to talk about what makes a better design, less complex, and more simple design. He says this works well in the DevOps loop because of it is a continuous conversation, the conversation will follow around the DevOps loop. He also says it works well at large scale, where you have teams of teams (teams within larger teams).


### Q6: Messaging Integration Patterns
- **Objective**: Identify and describe five messaging integration patterns, including the *Pipes and Filters* and *Request-Reply* patterns.
  - Use the PowerPoint slides on integration patterns as your reference.
  - Provide real-world use cases and, optionally, code examples for these patterns.

### Q7: Messaging vs Conversation Architectures
- **Objective**: Discuss the difference between messaging and conversation architectures as explained by Gregor Hohpe.
  - Focus on challenges like pub-sub vs. subscribe-notify models (starting at 18 minutes in *Enterprise Integration Patterns 2*).

### Q8: Pattern Languages
- **Objective**: Summarize the core concepts of pattern languages as described by Gregor Hohpe.

  - For patterns to be truly useful, they need to be clear and understandable, allowing practitioners to easily grasp and communicate the ideas they represent. They must be proven solutions, drawn from real-world experiences, demonstrating their effectiveness in addressing recurring problems. It’s crucial that patterns are context-aware, clearly defining the situations where they are most applicable, so they are used appropriately. Additionally, useful patterns should document both their benefits and potential trade-offs, helping practitioners make informed decisions. Reusability is also key—patterns should be general enough to apply across different scenarios while still providing specific, actionable guidance. Finally, patterns are most effective when they are part of a larger pattern language, connecting with other patterns to provide a comprehensive roadmap for solving complex problems.

### Q9: Strangler Pattern
he goes in to more detail about the ABCDE of modern EA he discusses the ‘strangler’ pattern for moving away from legacy systems – why is this seen as a complex problem and what does the 
strangler pattern do to help?

Going from a legacy system to modern enterprise architecture is complex because you often want the system to work while transitioning, and it takes time transitioning. However, the Strangler Pattern, in combination with refactoring and anti-corruption layers, helps to upgrade a legacy system to modern enterprise architecture. This is done in small pieces at a time to reduce complexity, all while the legacy system still runs the functionalities that have not been upgraded yet.
 

### Q10: Core Architecture Diagrams
- **Objective**: List and explain the three core architecture diagrams described by Jesper Lowgren.
  - Provide examples of each diagram and explain their roles in solution architecture.


### Due Date:
- **Submission Deadline**: 16 September 2024

---

## Resources
- Moodle videos on Enterprise and Solution Architecture.
- PowerPoint slides on Enterprise Architecture and Integration Patterns.
- Books:
  - *Team Topologies* by Matthew Skelton
  - *Enterprise Integration Patterns* by Gregor Hohpe
- Additional reading:
  - Simon Rohrer’s article on [Modern Enterprise Architecture](https://modernenterprisearchitecture.substack.com/p/modern-enterprisearchitecture-a)
  - [Strangler pattern wikipedia](https://en.wikipedia.org/wiki/Strangler_fig_pattern)

---