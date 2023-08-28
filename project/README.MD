# SWE 3313 Project Introduction

This course has a large team project that starts immediately after Exam 1. You should start thinking about it now and considering who to add to your team.

This project attempts to simulate the software development process a small team might follow to produce a software solution for a client (me). The project has seven graded components, one of which is graded by your teammates. The entire project is 50% of your semester grade.

- [Project Plan](#project-plan)
   15 points, 5% of total
- [Requirements](#requirements)
   30 points, 10% of total
- [User Interface Design](#user-interface-design)
   30 points, 10% of total
- [Technical Design](#technical-design)
   30 points, 10% of total
- [Implementation](#implementation)
   105 points, 35% of total
- [Final Presentation](#final-presentation)
   60 points, 20% of total
- [Peer Evaluation](#peer-evaluation)
   30 points, 10% of total

---

## What Will You Make?

Your customer (me) wants a shopping cart/sales system that meets very specific architectural requirements. 

The system will manage no less than three related data tables:
- Inventory
   Each item in this table will be unique (you will not choose a quantity). Items have at least one related image, plus a description, and price. Each item has a unique ID that will never repeat. If you want to show multiple images, you must add another table to your design.
- Users
   Users have a unique username and a role that sets their access level. Each user has a unique ID that will never repeat.
   - Customer: Can browse inventory and purchase items. Customers can self-register (create their own account).
   - Administrator: In addition to all Customer rights (except self-registration), Administrators can create, update, and remove inventory, plus run a sales report showing all sales.
- Sales
   A sale record relates an inventory item to a user. A sale record also includes the date/time the item was sold and payment details such as sales tax, shipping fees, and the total. Once an inventory item is related to a sales record, it is no longer available for purchase. Each sale record has a unique ID that will never repeat.

Your team will decide what industry/product to target. You will pick something that sells *unique* items, similar to Etsy or a pet rescue. In other words, you will not create inventory items with a quantity greater than 1, so pick something that sells unique goods. Once an inventory item is in the Sales table, it is "sold" and no longer available for sale. Some ideas you might consider are:

- Artwork
- Pet Rescue (don't sell rescued pets - charge fees for adoption overhead and veterinary care)
- Automobiles
- Handmade Jewelry
- European Castles
- Pokemon (gotta catch 'em all)
- Video Game Items (players, gold, etc.)
- Asteroids (they are quite valuable, and each is very unique, for example, [Oumuamua](https://www.npr.org/2023/03/22/1164814086/scientists-think-they-know-why-interstellar-object-oumuamua-moved-so-strangely))

Each team will produce a sales system tailored to your selected product/industry implemented using my architectural requirements. This is like each team making a car with four wheels and two doors and an engine, but every car is uniquely styled, has a different color, is electric or gas, etc. Every team's "car" will be unique in this way, but share the architectural characteristics I specify.

Be creative (engineering is a very creative profession) and put some thought into this. Pick something that will make a great looking presentation and keep your teammates, classmates, and me interested. Produce something that you will be proud to show a future client/employer when they ask you for an example of your work.

---

## What Will You Need?

This project covers many disciplines and you will use a variety of tools. Fortunately, none of them will cost you anything.

1. Teammates
   Far and away the most important bit.
2. A Team Name
   Completely unnecessary, but you cannot have a team without a name. Pick something cool.
3. A free Github account
   You will check in some of your submissions and all of your presentations to a team Github account. Your team can either create a dedicated Github account or choose one team member to house the team's work in their  account.
4. An IDE for development
   I will provide everyone a full JetBrains license. They have IDEs for every major language and operating system. You can use something else for development, but I recommend these, particularly if you have never used a professional-grade tool. JetBrains IDEs work on Windows, MacOS, and Linux.
5. A YouTrack account
   I will provide these to each of you. Your project plan, requirements, and technical design will be housed here. Your technical design will use YouTrack's Knowledge Base feature and will be written in [Markdown](https://markdown-it.github.io/). Your project plan will use YouTrack's excellent [Gantt Chart creator](https://www.jetbrains.com/youtrack/features/gantt_chart.html).
6. A free Marvel account
   Your UI design will be made in Marvel, a friendly high-fidelity design tool.
7. Software to record video presentations
   Windows and MacOS both include recording software. You can use whatever you like as long as the results are high resolution and the audio is clear. If your presentations are too large to check in to Github, you can use [VLC to compress your presentation to a more reasonable size](https://multimedia.easeus.com/video-converter-tips/compress-video-vlc.html).
8. D2L
   Everyone will post a link to their team's work in the D2L assignment folder. This is necessary for the grade book. Your actual work will either be in YouTrack or Github. Every member of the team will post in D2L the same links. To avoid late penalties, do not assume your teammates are handling this for you.
9. Diagramming tools
   I will introduce you to a few. I am partial to [PlantUML](https://www.plantuml.com/plantuml/umla/jSxBQW8n6CNnVPxYuAPGK9pBgeYuQJTz28cJKoSqbo7vh1NjktTguw98SL6w2l_am2-hB3h9pZjrXzuQGdeY3r4ktTdKEQenzLkq1aEA6qUViRVIGuUjeq6NuZxZXHILNsqOTD8UpWRAOI1YaZugnI1M3fWydizvDO7EuBp2KG7thDRMu05XvpTCM2os34nQQ9PB1KodNwEWFSUDy5t6DCnTieFO62wN7rTCNPYwCFLjvlelJy_droWzqzfGj7NvTx8fP5F8vZRvHx4jObl4zX_4UONJQJQBnz6flpEMR7vcgrOCPkVT9m00) and [Mermaid]((https://mermaid.live/edit#pako:eNp1Uk1vwjAM_StWdtkk-AHtreJDmhgFFdhh6w5ea9qINqmcsIkB_30p7bSVjlziOM_2e7aPItEpCV8QjyVmjGWswJ1REMHpNBzqI4TBfDIejqPH50kEPmBR6E_zizo2Zn2MZakyYMqkM9FKrcJ9-U4My1kPVeKO-k5Hprj2vr5BhWzbmufmWk6i1SK8wVGaDqhPMWX5QWyeZELKkKMHsVjnBEXruIvFdcy95z3AVrKxIZbk8AtVHMDzIMmRMbEuHSBT0x9K-wmgwCa291HlWhFs_vRIKguYUUdxR2NfUoIc_df4AUxnN_Rf5CfUAbXF5kG4mQaj9SZyxXSttKZoNXwRa9DsJuW01vP3L5M0YiBK4hJl6pbpwi4WNienVvjOTJF3dUvODod7q1cHlQjf8p4GYl-laKldP-FvsTDOW6F60frnff4G-kLSMQ)) because I hate drawing. You can also use Dia (I think it stinks, but it is free and cross-platform and many courses here require it) or any professional grade diagramming tool such as LucidChart, yEd, etc, You cannot use PowerPoint (which is not a professional grade diagramming tool) or hand drawn diagrams. Try a few and pick the one you like.

---

## I Just Finished FYE. I am REALLY Nervous. Can I Do This?

Yes!

Some of you are not confident in your abilities yet. This course and this project will help you build the confidence you need to succeed in this profession.

I will help you get there. You will surprise yourself this semester. I hear it every time I teach 3313. 

This field requires a lifetime of learning new things. If you come out of here with one thing, it's the confidence that you can learn new things and apply what you have learned to the latest problem you have to solve.

Google and YouTube are your friends. Computer science has never been more accessible than it is today thanks to the massive number of training videos, blogs, and examples you can find online.

You have probably noticed I stay after class every night. You will find that I am almost always available at that time. Take advantage of that if you and your team are struggling. 

Most importantly, do not wait until the last minute to ask for help and manage your time well.

------

## After Each Component Is Graded

After each part of the project except the Final Presentation, I will pick an outstanding submission and share that team's presentation with the class.

I encourage you to watch these shared presentations. We have much to learn from one another.

------

## Crashing and Burning on One Part

Almost every semester I see an outstanding team deliver a bad component, even getting a D or F on that part. Most of these teams go on to make excellent grades on the overall project.

Why does this happen? This project covers multiple disciplines - writing, design, coding, presenting, etc. It is hard to do all of them well unless everyone is contributing their combined expertise.

Also, team members let you down sometimes, even in excellent teams. Sometimes people just get overwhelmed or have problems in their personal life that temporarily crush their ability to execute. Your team has to manage this. All of you must have the attitude that you succeed or fail together. Support one another. Learn from failure to avoid failing again.

Whatever the reason, if your team fails on one piece, do not let it demoralize you. There are many pieces in this project and a single bad grade will not hurt your team overly much. I know grades are important, but in the long run, learning from failure is even more valuable.

--------

## Team Selection

`Complete by September 21, 2023`

As of August 26, there are 38 students in this course. Therefore, there will be 8 teams of 4 and 2 teams of 3. The teams with 3 students will get a bit of flexibility in grading (but not deadlines) since they have 25% less brainpower to complete the project (also remember that fewer teammates can be good since it's less to coordinate - I personally do not think a smaller team is any disadvantage).

Choose your teammates wisely. I recommend thinking about the various competencies necessary to perform each component of the project with high quality. Each of you needs to contribute to each piece, so do not let your teammates do the work simply because they might have a bit more skill in a particular area. In fact, you should probably participate *more* in pieces where you have less expertise to get the practice you need to improve. Here are some of the competencies necessary to execute the various phases of the project.

- Leadership
   Someone needs to coordinate the team. Some teams do fine without this, but they are the exception. Most teams need someone who coordinates the group's activities and occasionally has to push one or more people to do their part. This can be a thankless job. I recommend learning a bit about [Servant Leadership](https://www.forbes.com/sites/forbescoachescouncil/2020/03/11/traditional-leadership-vs-servant-leadership/?sh=493498c6451e).
- Written Communication
   This project has several large written deliverables. Your components must be professional-grade and exhibit outstanding grammar. Your work must effectively communicate very complex ideas. This includes the [Project Plan](#project-plan), [Requirements](#requirements), and [Technical Design](#technical-design).
- Visual Design
   This project has a significant user interface design effort. This includes the User Interface Design component. Being a good visual designer means being able to see the world through the eyes and experience of your target audience.
- Technical Design
   Every phase of this project requires you to understand what you can (and cannot) produce within the timeframe. You have requirements from me to execute. This is not simply expertise in coding... this involves deciding how to build something that meets the requirement with high quality in the allotted timeframe. 
- Implementation / Coding / Packaging
   There is one coding phase. Being a good coder is not enough to ace this part. You have to execute the requirements, technical design, and visual design. In other words, you have to convert the artifacts produced earlier in the project into a working system.
- Presentation
   Every component (Project Plan, Requirements, etc.) includes a video presentation. This is where you will take the finished work you are delivering and produce a short 5 minute video describing what was done. This is where you are convincing your customer (me) that the work you are doing is high quality, meets or exceeds expectations, and that I can be confident you are on the right path.

After considering these notes, put together your teams. You will tell me your teammates after Exam 1. On that day, I will provide you access to YouTrack, the system we will use to build your project plan, requirements, and technical design. Professional engineers typically use online tracking systems like YouTrack to manage large projects instead of Word, Excel, etc. We will do the same.

Once your team is ready, post your team information on this [Google Spreadsheet](https://docs.google.com/spreadsheets/d/1HAYA4j73sbCi0KeXlEjSr-4Po-mB3QXsVpAHA1ZZQbQ/edit?usp=sharing). Read the Instructions tab, then select an unused team sheet and complete the required information. Do not modify the spreadsheet or change another team's information. 

![image-20230828092225481](/Users/jeff/projects/swe-3313-fall-2023/project/README.assets/image-20230828092225481.png)

NOTE: Anyone not on a team by selection day will be assigned to one by me. If you are uncomfortable finding teammates, it will not be a problem.

-----

## Project Plan

`5%, 15 of 300  points`

In this component, you will use YouTrack to develop your project plan. This will include the milestones and various tasks to execute. This will be presented in Gantt chart format using YouTrack's Gantt chart creator. I will give you the milestone dates. You will decompose the milestones into tasks that do not exceed 3 days, assign each a priority and team member(s), and order them in a Gantt chart.

Your recorded presentation will present your plan within 5 minutes. I want you to think of every presentation in this project as a mechanism to build confidence in your client that the project is heading toward success, demonstrate technical proficiency, and help your client understand the decisions your team is making. Your client (me) wants reassurance your team is on the right path. I recommend putting some thought into your presentations. You will do this for real customers in your career, so do not write this off as just something to appease your professor. Carefully organize your presentations. I do not recommend submitting the first one you produce any more than you would submit the first draft of an essay as a final report.

You will check your video presentation into your team's Github repository. Your submission on D2L will include the link to the presentation and a link to your YouTrack Gantt chart (not a screenshot).

Since every team will have the same milestone dates, most of these will look similar at the macro level, but will vary significantly in the task breakdown. That is fine... there are many ways to perform this project.

### Why Is The Project Plan Only 5% of the Grade?

1. This is your first submission and I will grade it rigorously. You will see my expectations without losing a lot of points on the project. I expect excellent spelling and grammar, well-organized work, and a polished presentation.
2. This part is pretty easy. I give you the dates and milestones. If you were creating a real plan from scratch, it would be a much larger effort trying to figure out how long things actually take.

### Detailed Component Requirements and Grading Rubric

*Coming soon.*

-----

## Requirements

`10%, 30 of 300 points`

This component has three sections:

- Requirements Elicitation
- Technology Selection
- Requirements Writing and Presentation

### Requirements Elicitation

This component will begin with a Requirements Elicitation interview between everyone in our course and your client (me). Everyone can ask questions to better understand the project. This is your opportunity to better understand what I consider success, what requirements are most important to me, etc. We will record the session in case anyone wants to refer to it later.

### Technology Selection

After Requirements Elicitation, each team will decide and report to me the following:

- What language you will use to build your system
   Your choices are limited to Java, C#, Python, and Node+Javascript/Typescript
- Is your solution web-based or uses a desktop framework such as Swing, JavaFx, Winforms, MAUI, TKinter, QT, etc.
- What user interface framework you will use to create the screens for your system
   Your choices here will be constrained by the language your team chooses and whether the solution is web-based or desktop-based. Examples include:
   - Java + Web : Grails, Spring, Struts (note I recommend avoiding JSP - it's too old-school IMO)
   - Java + Desktop : Swing, JavaFX
   - C# + Web : ASPNET Core (note I recommend avoiding WinForms - it's too old-school IMO)
   - C# + Desktop : MAUI, Winforms (MAUI is much newer and cross-platform, but still a bit immature)
   - Python + Web : Django, Flask
   - Python + Desktop : PyQT, TKinter
   - Node + Web : Many options here, but Sails.js is a good one to consider for MVC
   - Node + Desktop : Electron (warning - this can get complex fast, but is a great framework regardless)
   - Web API + Javascript SPA UI
      In this configuration, the web API is made in Java, C#, Python, or on a Node server and the UI is built using a web framework such as Angular, React, Vue, or Svelte
- IF you selected a web framework, you *must* select a popular CSS framework such as Bootstrap, Tailwind, Bulma, etc. Do not plan on writing your own (not a good use of your limited time, less maintainable, and does not add to your resume).

Some things to consider when choosing:

- Everyone on your team must agree. 
- Pick something you believe has economic value to your resume. Technologies such as JavaFX and Winforms are losing value in the market because they are old and being replaced by newer technologies. You can use them and it *will not* count against you, but consider something newer first.
- Though not required, picking something cross-platform has a lot of market value and is excellent experience as well. The only platform listed above that is *not* cross-platform is Winforms.
- Do not select something outside of your ability to deliver. If you pick something with a large learning effort, be prepared to make time for that. Remember - it's critical to ship working software... it's less critical (in this case) to write it on the coolest, latest, greatest thing.
- Do your research. You might even consider looking at job boards such as Indeed to see what has good economic value to you and your teammates for future career opportunities.
- Read the [User Interface Design](#user-interface-design) section of the project, then ask yourself "can I build a good looking application that matches my UI design with the language/framework I am selecting?" Your UI Design helps your client understand how the final implementation will look. Do not pick something that will look awful compared to your UI design (JavaFX and Winforms are not easy to make look great IMO). Note that this is where web frameworks shine in my opinion.
- Your client (me) must agree. If you pick something I think is too challenging, too esoteric, too old, too new, not in the allowed list, etc., I will ask you to try again. Ultimately, your client is "paying" you to do the project, so the client has the final decision here.

Often your client will tell you what language and frameworks to use and you have to learn them. They might want you to use something their other teams already know and support. In this case, you are choosing which is great, but it also means I may not have much (or any) expertise to help you if your implementation failing. *Choose wisely.* 

**IMPORTANT NOTE:** Start thinking about *how* your system will retrieve and store data. Your choices include CSV, JSON, and SQL. Your data must be written storage - it will not only live in memory - and be available after restarting the application. You do not have to select this mechanism until [Technical Design](#technical-design), but you need to start thinking about it and doing some research. Many of the frameworks I listed include libraries to help with this requirement. I always give an *optional* JSON lecture for those of you who want to use this valuable technique. If you choose SQL, I recommend considering something embedded like [SQLite](https://www.sqlite.org/index.html) that does not require a server installation. If you do require a server for storage, consider something cloud-based or that runs in a Docker container to simplify installation (Postgres is a great solution, for example for both Docker and free/almost free cloud solutions).

### Requirements + Presentation

Following Technology Selection, each team will produce a detailed set of requirements broken into Epics and Stories with each Epic assigned to a specific Milestone in your Project Plan. You will also estimate the effort for each Story. Note that we will cover Epics and Stories when we study Agile methods.

Your requirements will be detailed, precise, grammatically correct and correctly spelled, and well-organized. Your requirements will strive to be complete and have no errors of omission (missing requirements) or errors of inclusion (unnecessarily adding to the scope of the project). Each requirement will be assigned a priority, an estimate of effort (no more than 3 days, no less than .25 days), and one or more team members.

After your requirements are complete and available in YouTrack, you will once again produce a 5 minute video presentation to your client (me) to give a high level review of your project focusing on requirements you consider highest priority, most interesting, highest risk, etc. Do not just spend five minutes reading requirements. Once again, the presentation is to simulate convincing your client that you are on the path to success, that you have carefully considered and are working to managing risk, and that your project is organized and carefully planned. I should feel happy and confident after watching your presentation that your team understands the project, is not missing anything and furthermore, is not adding anything that will increase the risk of failure. Like before, carefully plan your presentation and make it professional quality.

### Writing Center Bonus

Do not forget that you can get up to two extra points on your final grade visiting the Writing Center (1 visit = 1 point, 2 visits = 2 points).

### Detailed Component Requirements and Grading Rubric

*Coming soon.*

-----

## User Interface Design

`10%, 30 of 300 points`

In this component, you will combine your knowledge of the project, the requirements, and your technology choice's UI capabilities to produce a high-fidelity mockup of your application using the free edition of [Marvel](https://marvelapp.com).

In this component, you are designing how users will move through your application. After reviewing your mockup, your client (me) will have a good understanding how each screen will look and how each screen relates to one another.

In reality, it is unlikely a real client/stakeholder will completely read and understand your requirements. It is easier for most users to map their expectations onto the final visual controls of a software solution than to imagine how it all fits together reading tables of requirements. Thus, we do User Interface Design to help our client envision the final project. During this part of a project, it's common for clients to say "OMG, I didn't think about that" or "This reminds me... I forgot to tell you" or "The colors you picked do not match our brand" or "This does not match my expectation" or "You can do this operation in 2 steps rather than 3 if you..."

Your mockup will demonstrate every screen in your future implementation, including:

- Login (as a Customer and an Administrator)
- Self-Registration (creating your Customer account)
- Inventory List including Search
- Product View
- Shopping Cart including Remove
- Checkout including payment acceptance and on-screen receipt
- Sales Report (Administrators only)

Marvel is used by Professor Sandra Jones for her design and interaction classes that all SWE students take, so this will give you valuable experience going into those courses.

Marvel supports both [desktop design](https://marvelapp.com/examples/recruitment-website) and [web design](https://marvelapp.com/examples/hotel-app), so your mockup will work for whatever technology selections your team has made.

Other design tools, such as PowerPoint, or hand drawn screens will not be accepted.

Make *sure* you are designing something that you are capable of producing in your selected language and framework. You will compare your UI design to your final implementation during your [Final Presentation](#final-presentation), so you want the expectation you set here to generally match the reality of what you produce. Do not draw a Ferrari and deliver a PT Cruiser. This can be particularly challenging with some UI frameworks such as JavaFX and Winforms, so you need to know what your team is capable of here before getting your client excited about his new Ferrari.

As always, you will produce a 5 minute video presentation showing your UI design. Like before, it will be professional-grade, well-organized, and highlight the features your client (me) will find most interesting or high priority.

### Detailed Component Requirements and Grading Rubric

*Coming soon.*

----

## Technical Design

`10% = 30 of 300 points`

At this point, you have spent significant time thinking about and working on your project. You should have very good ideas how to implement your system. Now that you have this knowledge and insight, you will produce a technical design detailing how you will build the most critical pieces of the system.

Your Technical Design will include:

- Implementation Language including *why* you selected it
- Implementation Frameworks including *why* selected it (obviously it's good experience, so leave that out and get into why your selection benefits the client in the long run)
- [Entity Relationship Diagram](https://mermaid.live/edit#pako:eNp1Uk1vwjAM_StWdtkk-AHtreJDmhgFFdhh6w5ea9qINqmcsIkB_30p7bSVjlziOM_2e7aPItEpCV8QjyVmjGWswJ1REMHpNBzqI4TBfDIejqPH50kEPmBR6E_zizo2Zn2MZakyYMqkM9FKrcJ9-U4My1kPVeKO-k5Hprj2vr5BhWzbmufmWk6i1SK8wVGaDqhPMWX5QWyeZELKkKMHsVjnBEXruIvFdcy95z3AVrKxIZbk8AtVHMDzIMmRMbEuHSBT0x9K-wmgwCa291HlWhFs_vRIKguYUUdxR2NfUoIc_df4AUxnN_Rf5CfUAbXF5kG4mQaj9SZyxXSttKZoNXwRa9DsJuW01vP3L5M0YiBK4hJl6pbpwi4WNienVvjOTJF3dUvODod7q1cHlQjf8p4GYl-laKldvx9nhepFa_fcYmHo_A0pm9Hm) and associated table of field descriptions
   All of the data your system manages and how each data type is related will be visually depicted here and the fields along with the data types will be described in the associated table.
- Services
   Your system will rely on services such as authentication, inventory management, and shopping cart management. Here you will show the modules, classes, and methods associated with each service and their relationship to one another. Someone reviewing this artifact should understand the actions each of these services can provide and what each method returns.
- Seed data
   When you start your application, what is already in the system? We call this "seed data". Typically that includes at least one administrator account, your inventory items and photos, etc.
- Data storage plan
   How will your application store data? Your choices are CSV, JSON, and SQL. Describe the libraries and technologies you will use to store data. For example, if you are using C#, you might use Dapper or Entity Framework for data access to write to your embedded SQLite database. Remember that the data you change/add must remain available the next time you start the application - this is a class project, but it needs to operate like a real application and starting fresh every time you launch is not realistic.
- [Coding Style Guide](https://www.cs.cornell.edu/courses/JavaAndDS/JavaStyle.html)
   Here you will link to your language's coding style guide, plus add any coding style instructions you expect all developers to follow. The ultimate goal is that all code follows a consistent style and appears to have been written by one person. Think about what will help future developers will need to understand your system, including commenting guidelines, naming conventions, filename conventions, etc.

The audience for your Technical Design is a developer - not your client (me). For the purpose of this project, assume that the developer is an outsourced engineer that speaks your language, but is in another country and timezone. Also assume that remote developer is me (surprise!). Therefore, your Technical Design must answer a lot of questions effectively and with high precision to avoid midnight phone calls and long meetings answering questions that should have been written into your Technical Design. Ask yourself if your outsourced developer can execute your design based on what you have written? If not, then you need to revise your Technical Design. 

After your Technical Design is complete, you will produce yet another 5 minute video presentation going over the Technical Design. In this case, your audience is your remote developer (who happens to be me, but not in guise of your client). Therefore, you need to introduce the material, call out what is important, describe areas of high risk, etc. Remember that the developer can read, so just reading the document to the developer is a waste of time... give the developer some perspective.

### Writing Center Bonus

Do not forget that you can get up to two extra points on your final grade visiting the Writing Center (1 visit = 1 point, 2 visits = 2 points).

### Detailed Component Requirements and Grading Rubric

*Coming soon.*

---

## Implementation

`35% = 105 of 300 points`

Finally, you are ready to produce your application! You have planned most of the semester and you know exactly what to make.

Now you will execute the requirements by implementing your User Interface Design and Technical Design. Your goal is to make your implementation look as close to the User Interface Design as possible.

You will submit your implementation to your client (me) via Github. It will include:

- well-written code that follows your language's style guide. Do not use Java conventions in a Python app.
- a readme.md in the source that includes:
   - a brief description of your application (from an end-user point of view),
   - environment requirements, such as "MacOS or Linux or Windows" (be very specific the systems and operating systems where you application can run),
   - steps to clone and build the application on a fresh machine. Be very specific - I will be attempting to follow these steps on my machine and they better have all of the steps, dependencies, gotchas, database schema scripts, warnings, etc. I need to get your application working without a lot of fuss.
   - any other important information you need to pass along to someone trying to setup and run your application.

There are many good articles on writing an excellent read.me. [I recommend reviewing a few so you do a great job producing this very important document.](https://bulldogjob.com/readme/how-to-write-a-good-readme-for-your-github-project)

I cannot stress how important is that your code compiles and runs. The whole point of software is to solve a problem. Code that does not compile cannot begin to solve a problem. Make sure your system runs, even if it does not meet every requirement or the UI looks awful. All of the work you have done till now was the *necessary journey* to refine your thoughts to the point you could produce a great application, but NONE OF IT MATTERS if the application does not run. Ultimately our work is about working software that solves a problem... your end user almost certainly does not care how fantastic your requirements and planning and designs were if the solution does not work.

Pro Tip: I recommend that every team member review your implementation's readme.md file and try to configure your implementation in a fresh directory. This will help you see steps you have overlooked. I think great work makes it easy on the end-user to get started quickly without having endlessly Google and troubleshoot to try out your work.

As always, you will produce a 5 minute presentation and check it in along with your implementation. Your presentation will demonstrate the process to setup and execute the application. I want to see it compile and run, then perform a purchase as a user. Next, stop the application, then start it again and run the sales report, thus demonstrating that sale performed in the first run was persisted to data storage. Finally, show the record you wrote to data storage (so open the CSV or JSON file or run a SQL query).

If you have time, show the project structure and call out anything awesome you did or techniques you embraced such as dependency injection. I will also find it interesting if you show how you separated UI concerns from your services and data storage code. I love talking about code, so entertain me if you have time in your 5 minute presentation.

This presentation *proves* that your application works and your source code compiles. That is critical because it is possible I might not be able to make your source code work on my machine, particularly if you have a complex setup (which I recommend avoiding, but that is your decision).

### JetBrains Professional IDEs

I will provide everyone with a full license to all JetBrains products. You can also get them free yourself with your KSU ID. I tell students this every semester and they still do not try these excellent products, so perhaps since I already procured the license you will give these a try. Note that I get nothing in return from JetBrains. I am just tired of developers not insisting on using the best tools for the job, so hopefully you will explore a few and find out what is best for your work.

Many developers go to great lengths to get VS Code or BB Edit or Textmate or "insert name of free thing here" to do what they need and that is fine, but you should also learn whether the productivity tools from companies like JetBrains will make your work go faster, find bugs faster, and produce better code.

NOTE: I like JetBrains IDES because they have a wide breadth of cross-platform offerings for all popular languages and they all work similarly so your Linux work in Java more easily translates to expertise working in Windows with Python. This is one of my favorite features of their product line since it lets me focus on the problem rather than "how do I compile and debug in [thing here]."

PRO TIP: I routinely ask people I am considering hiring "what tools do you like to use?" You can learn a lot about an engineer by the tools they select. The best tools, no matter who makes them, make you faster and help you produce better work. I routinely see people who will select an important tool simply because it is free, rather than perhaps paying $100 for an outstanding tool that will make them more productive and produce better work in less time. Open source/free is great, but sometimes you get more from a licensed product. Great engineers often buy their own tools, their own keyboards and mice, etc. if the company they work at does not provide great tools (also note that the best companies provide great tools and work environments). It's stupid to pay someone $100,000 and get cheap over a tool that makes that expensive employee far more productive.

PRO TIP 2: I will not hire an experienced engineer who says they do not care what tools they use. To me, that shows a lack of craftsmanship and passion for your art. Further, I will escort you out of the building and push you into the street if you say you use Windows Notepad to write your code. Windows Notepad sucks.

PRO TIP 3: I love mechanical keyboards. Not really a tip, but we are talking about important tools here. If you haven't tried one, you might be missing out on a very sublime experience. 

### Detailed Component Requirements and Grading Rubric

*Coming soon.*

-----

## Final Presentation

`20% = 60 of 300 points`

This is the end. You are done! The holidays are almost here and this course has an OPTIONAL final exam!

Once your implementation is ready, you will produce a polished 5 minute presentation of your working application. Your audience is your client (me). Assume that your client (me) brought 40 members of his team (all of you) with him to view the final presentation.

This is where you get to shine. Many final presentations just stagger me. By now you will know how to make a great presentation for the target audience.

Your 5 minute final presentation will include:

1) A run through of your application that demonstrates every screen and logging on as both a user and an administrator.
2) A comparison of your final application's user interface and your Marvel UI design. Explain why or why not your implementation met your design and what you learned from that. In real life, when your mockup does not match your final implementation, your client may be upset... it's like an architect designing a soaring skyscraper and the builder delivers a large tent. If your final work does not match your design, own it and learn from it. 
3) Anything awesome you want to show off.

After the entire class views your final presentation, your client (me) will ask you some questions. Your team must be present - everyone must participate.

We will use two lecture periods for final presentations. Each presentation and Q&A session will take about 10-12 minutes.

### Detailed Component Requirements and Grading Rubric

*Coming soon.*

-----

## Peer Evaluation

`10% = 30 of 300 points`

Hopefully you have an outstanding team experience during this project. If not, hopefully you learned something about how challenging working in a team can be and how important it is to have the right people on the team with you.

In this component, you will rate each of your teammates *and yourself* between 0 and 30 points. You are welcome to give everyone a top score including yourself. Or you can award less. 

Each student will receive the average of what was awarded by their teammates and themselves. For example, if you get a 30, 30, 10, 30 from yourself and your 3 teammates, your Peer Evaluation score will be (100 / 120) * 30 = 25 points`, or 83.3%.

You do not have to provide a reason for your scores and I certainly will not pass a reason along if you do give me one. Scores are therefore anonymous in that regard.

If you get less than top scores from your teammates, please ask yourself what you could have done to contribute more, to better support the project.

Here is some guidance you might consider:

- Do not penalize someone's score with whom you did not communicate your concerns with already. Have the courage to speak up when a problem occurs, not far after the fact. We are all here to learn, so make problems in the team a learning experience rather than a punishment at the end of the semester. There is an old adage that anyone you fire should already know it's coming because you already communicated your expectations.
- Everyone is here to learn, so perhaps pull back your penalty if you saw growth over the semester. Sometimes teammates who start out poorly end up learning what they need to do to support the team. This is growth.

Generally the only students who get poor scores from their teammates were the students who simply did not participate or let the team down in a big way during some critical piece.

So be a great team member and step up to the project. If you are not a great coder, help the great coder in the group test. If you are not a great writer, proofread the requirements. If you are the leader, do not be an a-hole, work on your diplomacy, and learn a bit about [Servant Leadership](https://www.forbes.com/sites/forbescoachescouncil/2020/03/11/traditional-leadership-vs-servant-leadership/?sh=493498c6451e). This project covers many disciplines, so everyone has a chance to be a great contributor for some piece of it.

### Detailed Component Requirements and Grading Rubric

*Coming soon.*
