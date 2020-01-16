# Assessment: Real-World Application - Part A

## Description of Website

### Purpose
The weExplore website is designed to accompany and facilitate weExplore, in running and managing events.

weExplore is a not for profit organisation based in Clayton, Victoria, providing health education to promote holistic health and well-being for the communities. Their mission is to promote a holistic healthy lifestyle. They do this by educating their members in physical, emotional, mental and spiritual health through running events such as cooking classes, pilates, and health seminars. 

The purpose of the website is to provide the ability for weExplore to create events and post them to the site there webpage where their members can sign up to attend the events and receive information about upcoming events.

Finally, it allows the administration of weExplore to have access to a master database of their members. This lets the administration have a greater understanding of their member’s metrics and needs to be able to cater specifically to events of their liking. 

Currently weExplore use MeetUp and word of mouth to promote their events to the community. Through the build of a custom website, weExplore will have further reach and a consistent event management system. 

### Functionality

The main functionality of the weExplore website is the ability for administrators to create events and for members to sign up and confirm their attendance for the events. 

It will contain a feed with upcoming events that are available for members to attend in an easy, informative and friendly design. The website will exemplify the passion and dedication weExplore has to health education and holistic wellbeing. 

Furthermore, the website will allow the administrators of weExplore to have access to a database of their users and the events the users are attending. This will allow them to gain a comprehensive understanding of their user’s wants, needs, and interests concerning their health. 

Finally, the weExplore website will be the primary point of information for the members to find out more about the company, services offered and contact information. This will be accessible through different pages of the website. 

The site will have a main navigation bar to allow ease of accessibility for all pages. It will contain the main events component with a singular event component and the ability to “click” attending events. 

Furthermore, it will contain the functionality to sign-up, login, and sign-out of the members portal. As well as signing in to the administrator portal and display the admin dashboard to create, edit and delete events. 

### Features

Members sign-up/login
- Authentication, encryption, and token generation.

A feed of upcoming events that is viewable by all visitors on the site, not just members.
- Ability to filter by interests/date/length of the program and location 
- Calling of API from different endpoints.

The ability for members to sign-up to an event and/or program.
- Use of Google Calendar plugin for members to receive a calendar invite to the events/programs.
- Automated emails sent to attendees reminding them of upcoming events.
- Automated email blast to members about upcoming or related events. 

Static pages holding information about and contact details of weExplore
- Email sign up/ subscription service.
- Minimal and accessible layout of information

Admin dashboard
- Ability to create/edit/delete an event where the event feed updates instantly.
- A custom event creation form for administration.
- Ability to access and view attendees of organised events.

### Target audience
The target audience for the weExplore website is the wider community of Clayton, Victoria who are seeking health advice, education and a group that has similar interests in health and wellbeing. 

#### The current members’ metrics are: 
Roughly the age range is between mid 20’s all the way through to mid 40’s. Consisting of a variety of demographics and socioeconomic status, however, predominantly the members are of middle socioeconomic status. The members consist of students from surrounding universities particularly from Monash university, young professionals and young families. 
The target audience will initially consist of the current member base that is part of the MeetUp group. However, the aim is to expand the reach to more members of the community who are seeking and in need of support with their health and overall wellbeing. 

### Tech Stack

Database Management:
- MongoDB Atlas

Application:
- Amazon S3
- Javascript
- Node.js 
- Express.js
- Mongoose
- React.js
- Html & CSS/SASS
- Jest

DevOps:
- Github

Deployment:
- Heroku
- Netlify

Project Management/Misc: 
- Trello
- Slack
- Google Docs

## Dataflow Diagram  
Below are diagrams of level 0 and level 1 of the dataflow for the *we Explore* web application  
 ![DFD level 0](./assets/DFD-level0.jpg)  
 ![DFD level 1](./assets/DFD-level1.jpg)  

## Application Architecture Diagram

The application’s architecture is using MERN stack. The diagram demonstrates the interaction between the services, frameworks and applications. The high level overview is further discussed below. 

![Application ArchitectureDiagram](./assets/App-Architecture-Diagram.jpg)

## User Stories
The user stories were generated using the agile user story methodology. User stories were created using the

*As an [user] I want to [desired function] so that [desired outcome].* 

User stories are essential to agile projects as they allow for the ability of the team to put people (end users) first. To build functionality and components that satisfy the user’s needs and wants. The creation of the user stories allowed our team to understand what we were building and why we were building these components. User stories ensure that our design and development are human-centered.  

Our process below follows the structure of generating user personas. Then creating non-technical user stories for these personas.   
Below each user story, we have generated technical functions, features, and components that are required to meet the definition of done for each user story.   
In kanban style, these user stories will populate our backlog and become one unit of work for a member of the team to complete during the build phase.  

### Administration User Persona
**Role:** Administration, Manager of weExplore  

**Motivation:** To help members of the community achieve good health and overall wellbeing, provide access to the community to health services and health education. Create a successful and impactful not for profit. To better understand their members and their health needs and/or wants.  

**Pain-points:** Do not have a central point of call where they can promote their services, events and contact details. Do not have access to a master database of their members, so they do not understand their clientele or have definitive data on what members are going to what events.  

#### User story #1
**As the director of weExplore I want the ability to create and promote our events in one place so that our community knows where to find out information and to reduce work time for me.**  
Technical Features/ Definition of done:  

#### User story #2
**As the director of weExplore I want to have access to our master database so that I understand the needs and wants of our members and can cater to these findings.**  
Technical Features/ Definition of done:  

#### User story #3
**As the director of weExplore I want an admin only login so that I can access the database and create events with the assurance of security and proper authentication.**  
Technical Features/ Definition of done: 

### User Persona's
#### User Persona #1 
**Role:** Community member, has been attending weExplore events regularly, young professional.  

**Motivation:** Attends weExplore events as it is a safe and supportive community. Wants support with their nutrition and cooking ability. Attends regular seminars on healthy cooking and is learning a lot about good nutrition on a budget.  

**Pain-points:** Has to continue to regularly check MeetUp.com for new events, is not a member of weExplore and would like to be. Sometimes they cannot attend the events and would like to inform weExplore of attendance change.

#### User story #1  
**As a member of weExplore I want to be able to securely login and have my credentials remebered so that weExplore have my details and I have a personalised experience**  
Technical Features/ Definition of done:
- Users will sign up on the signup page.  
- API end point for user sign-up/login   
- Signup page contains a React/Redux form component. The initial state of the inputs is null until the user enters their details and hits submit. The component stores the user’s inputs into an object that is sent via a post request to the back-end server.  
- Express will take the information provided by the Front-end and send that data into the Mongo database to be stored.  
- After the user has completed their registration, they will remain logged in.  
- When signup is completed, they are either redirected back to the home page or back to the event page they were looking at depending on the situation.   
- Authorisation token is generated in the back-end and sent to the header to allow user to interact with events. 
- Sign-up form fields are run through validations to ensure correct formating and presence. 
- Passwords are hashed and salted for security  

#### User story #2
**As a member of weExplore I want to be able to sign up for an event and get a reminder on the web application so that weExplore are aware of my attendance and I can be organised**  
Technical Features/ Definition of done:
- Users can browse and explore all events without signing in 
- To attend an even a user must log in or sign up
- Users browse through all events on the event page where an API endpoint is created to get all events  
- Events are presented in the form of cards where the user can click on the card and routes to the single event page where an API endpoint is created to get a single event based on an ID
- Once they click attend on an event, it prompts the application to send their user’s ID to an array stored inside the event’s database and sends the user a calendar invite through Google Calendar using its API.    
- where they browse the events page for upcoming events. Events are presented in the form of cards where the user can click on the card, which routes them to the event. On this event page, the information will come from database, which uses a get request and the event ID to populate that data into the react component. 
- At the bottom of the page, there will be a bar with a button ‘attend’. For user to attend the event, they would need to press this button. The button will store the user’s ID and send a post request to the server where the user’s ID is stored inside an array for the event.   

  


#### User story #2
**As a member I want to be able to search for events by category or date so that I can find the events suited for my needs and not have to scroll through all the events.**  
Technical Features/ Definition of done:

#### User story #3
**As a busy user I want to be able to change my attendance status online to an event so that I can let weExplore know I will no longer be attending and won’t feel bad.**   
Technical Features/ Definition of done:  


#### User Persona #2
**Role:** New member of the community and has driven past weExplore, yet to attend any of the events but is seeking support for their mental health.  

**Motivation:** Is wanting to take action for their mental health and find a supportive group or community where they can learn how to take better care of themselves. Drives past weExplore and has googled their company/organisation.  

**Pain-points:** Struggling to find information about what weExplore does. Wants to reach out but only finding a meetup.com website, is seeking something of a more professional standard or has their own website. Wants to know what services and events weExplore host.  

#### User story #4
**As a not yet user of weExplore I want to be able to know more about weExplore so that I can make an informed decision on whether I want to user their services or not.**  
Technical Features/ Definition of done:  

#### User story #5
**As a user I want to read reviews or testimonials on past events at weExplore so that I can assess whether the events are worth going to and of good value.**  
Technical Features/Definition of done:  


#### User Persona #3  
**Role:** Has attended one event at weExplore with a friend. Really enjoyed the Pilates class.  

**Motivation:** Wants to lose some weight and strengthen their core through a non-impactful but hard-working exercise. Needs regular accountability. Also wants some more advice with overall wellbeing and nutrition.  

**Pain-point:** Wants to go to more events at weExplore as really likes the Pilates class but unsure of what other events weExplore has to offer. Would like regular updates on what is going on at the centre and of any changes. Would like a link or website to forward to family and friends who would benefit from weExplore.  

#### User story #6
**As a new user of weExplore I want to be able to contact them so that I can learn more information that is specific to me.**  
Technical Features/ Definition of done:  

#### User story #7
**As an attendee of an event to weExplore I want to know who is going to be presenting and their qualifications so that I know the event I am attending is worthwhile and legitimate.**  
Technical Features/ Definition of done:     











