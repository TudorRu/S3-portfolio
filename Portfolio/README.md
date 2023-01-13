<h1 align="center">Individual and Group Project</h1>
<h3>Table of content</h3>


<h2 align="center">Catering application</h2>
<h3>Project description</h3>
<p>
For the group project, our team has chosen to go with developing a solution for 'Info Support’ - a large company, developing mostly in the Artificial Intelligence (AI), Information Technology (IT) and Software areas.
They require a software solution for their new restaurant, which will be opening at the begging of 2023, that will ease the workflow of the employees
and make it more comfortable for their clients to order, pay and overall to improve their expierience. 
This will increase the number of clients, reduce the number of misunderstood orders and make the process faster and thus enabling more orders to be made.
Guests should be able to order without interacting with a waiter in any way and also view the status of their orders in real time as they are being prepared.
</p>
<h3>Requirements</h3>
<hr>
<div id="FRequirements"
  <h4>FR-01 - The waiter should be able to view the available tables</h4>
  <h4>FR-02 - The waiter must be able to start a new session when seating guests<h4>
  <h4>FR-03 - The waiter must be able to view when an order is ready to be delivered</h4>
  <h4>FR-04 - The guest must be able to view menu in the application<h4>
  <h4>FR-05 - The guest must be able to modify selections for his order</h4>
  <h4>FR-06 - The guest must be able to view the contents of his cart</h4>
  <h4>FR-07 - The guest must be able to view the orders he made in this session</h4>
  <h4>FR-08 - The guest should be able to view the status of his order</h4>
  <h4>FR-09 - The bartender should be able to select and item from the order to prepare</h4>
  <h4>FR-10 - The bartender should be able to move the item he prepared to ready</h4>
  <h4>FR-11 - The cook should be able to select and item from the order to prepare</h4>
  <h4>FR-12 - The cook should be able to move the item he prepared to ready</h4>
  <h4>FR-13 - The manager should be able to view statistics of the restaurant</h4>
  <h4>FR-14 - The manager should be able to export the statistics outside the application</h4>
  <h4>FR-15 - The manager should be able to add new table to the application</h4>
</div>
<h3>User stories</h3>
<hr>
<div id="UStories"
  <h4>US-1 - As a waiter I want to start a new session, so that the clients can start ordering<h4>
  <h4>US-2 - As a waiter, I want to be able to view if an order is ready, so I can serve the guests.</h4>
  <h4>US-3 - As a waiter, I want to view the status of the tables, so that I can assign new clients to the right table.</h4>
  <h4>US-4 - As a guest, I want to view the menu to decide what to order</h4>
  <h4>US-5 - As a guest, I want to add/remove items from my order so I can prepare my order.</h4>
  <h4>US-6 - As a guest, I want to see the items listed in my order, so I can make my final decision.</h4>
  <h4>US-7 - As a guest, I want to make an order so I can eat.</h4>
  <h4>US-8 - As a guest, I want to see what I have ordered during my session, in case I want to repeat the order.</h4>
  <h4>US-9 - As a guest, I want to view my order to know the state is in.</h4>
  <h4>US-10 - As a cook, I want to select the item in the order to prepare, so that I am the only one that works on it.</h4>
  <h4>US-11 - As a cook, I want to be able to move an item to ready, so that it can be delivered to the guests.</h4>
  <h4>US-12 - As a bartender, I want to select the item in the order to prepare, so that I am the only one that works on it.</h4>
  <h4>US-13 - As a bartender, I want to be able to move an item to ready, so that it can be delivered to the guests.</h4>
  <h4>US-14 - As a manager, I want to view the statistics of the restaurants, to see where we may improve our services.</h4>
  <h4>US-15 - As a manager, I want to export the statistics to view them outside of the application so I can manipulate them in any way.</h4>
  <h4>US-16 - As a manager, I want to add tables to the restaurant, so that I can expand the seating arrangements.</h4>
</div>
<h3>C4 model</h3>
<hr>
<div id="C4">
<h4>C1</h4>

<img src="https://github.com/TudorRu/S3-portfolio/blob/512ab53a6d982fc62688bef93d79e9576439bbc5/Images/C1-group.png" width="800" height="600">
  
<p>
This is a model of our high-level architecture. We have 5 parties that will be making use of our application. We have the cook, and the bartender who look at open orders that are listed in our application and process them. The waiter assigns clients a seat and makes sure the orders are delivered. In addition to this they make sure a session is closed properly. The manager can see the data of all the past orders, as well as add more tables to the restaurant. The client is a customer of the restaurant. They place orders and get assigned a seat by a waiter. They can only modify their own order. 
In addition to this we also have an external payment system.
</p>
    
<h4>C2</h4>

<img src="https://github.com/TudorRu/S3-portfolio/blob/512ab53a6d982fc62688bef93d79e9576439bbc5/Images/C2-group.png" width="800" height="700">
 
<p>
When scoping into our high-level architecture, we can see that our application is split up into 3 parts. We will be having a front-end application written in Vue.js, a back-end application written in .NET and a MySQL database. The backend communicates with the front-end using web sockets, which means that the data in our front-end will be updated in real-time. The communication to our database will be done using an ORM, which ensures that we do not spend too much time writing SQL queries. 
</p>
<h4>C4</h4>

<img src="https://github.com/TudorRu/S3-portfolio/blob/512ab53a6d982fc62688bef93d79e9576439bbc5/Images/C4-group.png" width="800" height="550">
    
<p>
The goal of our class diagram is to think of every function of our application and think of how this will look in code. A customer can start a session, which consists of one or multiple orders. Every time a customer makes a new order, a new order is added to the session. An order consists of multiple menu items, which consist of multiple ingredients. The reason for having an ingredient class is to keep track of stock levels in real time to display in the application what dishes are available. At the end of a session a customer can pay, and the order is saved in the database.
</p>
</div>

<div id="Database"
<h3>Database design diagram</h3>
<hr>    
 
<img src="https://github.com/TudorRu/S3-portfolio/blob/512ab53a6d982fc62688bef93d79e9576439bbc5/Images/Database-diagram.png" width="800" height="550">
</div>
<h3>Technologies</h3>
<hr>
<h4>Front-end</h4>
<p>
For the front-end we initialy decided to go with Vue.js, however our front-end developer ultimately decided to go with Nuxt.js which s a free and open source JavaScript library based on Vue.js, Node.js, Webpack and Babel.js. Nuxt is inspired by Next.js, which is a framework of similar purpose, based on React.js.

The framework is advertised as a "Meta-framework for universal applications". The term universal is used here with the meaning that the goal of the framework is to enable users to create web views in JavaScript utilizing the Vue.js single file component system and that can function both as in-browser single page application (SPA) views as well as server-rendered web views which are then (after server rendering) "rehydrated" to full SPA functionality. Additionally, the framework enables users to have the content, or parts of it, fully pre-rendered on the server and served in the manner of static site generators.
For my individual as you will see, I have used Vue.js and also I have helped in developing the front-end in our group project, so if I would to make a 
comparison, I can say that Nuxt.js trully makes your life easier and it's easier to understand.
</p>
<h4>Back-end</h4>
<p>
For the back-end we decided to go with .Net Core 6 because we are already familier with C# language from previous study year.
.NET (pronounced as "dot net"; previously named .NET Core) is a free and open-source, managed computer software framework for Windows, Linux, and macOS operating systems.[3] It is a cross-platform successor to .NET Framework. The project is primarily developed by Microsoft employees by way of the .NET Foundation, and released under the MIT License. 
</p>
<h3>Quality Assurance</h3>
<hr>
<p>
For the moment we didn't formulate a test plan nor made any tests for our application. The ideal way of working in my opinion is in TDD(test driven development where you first create the test, which will fail, and then implement the method that make the test to pass. This will make the refactoring and maintanance of the application a lot easier. 
</p>
<h4>UI</h4>
<p>
To make sure that the application we envisoned matches with the expectation of our clients we have created wireframes and prototypes of all the views of the application and we have presented them to our clients in our first 2 sprints. Based on their feedback we have tweeked the wireframes once again in order to get their approval for the final version of the application.
</p>
<h3 id="BProcess">Business Process</h3>
<hr>
<p>
  In order to showcase how the application will impact the business, I have created 2 business processes diagrams.
</p>  

<img src="https://github.com/TudorRu/S3-portfolio/blob/a8c60c239d64573353d1214ab5798b4722cff9ed/Images/business-without.png" width="1000" height="750">
  
<img src="https://github.com/TudorRu/S3-portfolio/blob/a8c60c239d64573353d1214ab5798b4722cff9ed/Images/business-with.png" width="1000" height="750">
    
<p>
  After analyzing the diagrams, we can conclude that a bottleneck can form when multiple tables want to order at the same time because one waiter will be assigned on a number of tables at the same time. This will ease the customer's ability to order and will speed up the whole process, improving the quality of service. Another issue that the application solves is the communication in kitchen and at the bar as well as between the waiters with kitchen and bar. When the products are ready to be delivered, the waiter will be notified automatically that the order is ready to be delivered.
Also, if the guests want to order again, they don't have to call the waiter and issue the order, they can simply open a new order and launch it with ease.
Finally when guests want to pay, they will simply do it by paying within the application, remove extra steps from the process.
</p>

<h3 id="CAwareness">Cultural Awareness</h3>  
<hr>
<h4>What is Cultural Awareness?</h4>
<p>
The definition of the word culture is a complex one and it refers to the characteristics and knowledge of a group of people, including social behaviors, norms, beliefs, arts, and customs.
Culture helps distinguish one group of people from another as we are wired to attach different meanings and react to situations in different ways. This document is the product of my interest in on the subject of cultural awareness as it is an important subject in software engineering due to the fact that teams are comprised of members coming from different nationalities. The main goal is to understand the differences between my and my team-mates’ culture and how to better communicate and collaborate.
</p>

<h4>Why is it important</h4>
<p>
Having cultural awareness in a software development team can help to promote a more inclusive and respectful working environment, which can improve team dynamics and lead to more effective collaboration. It can also lead to more creative and innovative solutions, as different perspectives and experiences are brought to the table.
</p>

<h4>Cultural Awareness in group project</h4>

<p>

In this semester I had the opportunity to collaborate with individuals from The Netherlands and Bulgaria. In the below diagram, I have plotted the indexes for each country based on Hofstede’s 6 cultural dimensions. Because Romanian and Bulgarian cultures are alike, I have decided to focus on Romanian versus The Netherlands differences.

</p>

<img src="https://github.com/TudorRu/S3-portfolio/blob/0a7d1bf4238238a17ca18e3fd245ed4608116522/Images/hofstead.png" width="1100" height="650">
  
<p>
When comparing Power Distance dimension, The Romanian score is quite high compared to the Dutch one and this can be seen when discussing with teachers, myself having a more formal approach, accepting hierarchical order , while Jan and Arnold, being more independent and their attitude towards our teachers being more direct and informal.

The difference in Individualism comparison is quite high, which may cause problems if not being taken into account, the Dutch placing more emphasis on their own well-being and interests while Romanians being more interested in how others are doing, taking responsibility for fellow members of their group.

The Masculinity index both for Dutch and Romanian society are on the lower spectrum, considered to be a Feminine societies, where we value equality, solidarity and then to care for the quality in our working life. This may be a plus for us because we tend to solve conflicts by compromise and trying to understand each other’s needs.

Both of our cultures have high Uncertainty Avoidance scores, however Romanians tend to be more strict and are intolerant of unorthodox behavior, having difficulties adapting to new situations. The Dutch although having a more pragmatic nature, they are flexible and are willing to change depending on the situation.

Although the Long-Term Orientation scores are high for both nationalities, I’ve seen a difference in the way we plan and manage problem solving. In the Netherlands they tend to try solving the issue in a more direct way, focusing on the direct objective, rather than thinking of all the consequences and implications that may follow. Both of these means having their pros and cons, in my opinion we complement quite well, bringing balance to the team.

When it comes to Indulgence dimension, our cultures are more different, the Romanian one being of Restraint, where I have noticed that I have a tendency to cynicism and pessimism. In the Netherlands people tend to be enjoying life more and value their free time more. The Dutch optimism and the Romanian pessimism combination can be a beneficial both of them brining important insights to a certain situation and assessing it in a more real to the truth way. 
</p>
  
<p>
  For this semester I've decided to fully research on this matter and a deep-dive using DOT framework into this subject can be found <a href="https://github.com/TudorRu/S3-portfolio/blob/8b631f1f5427178031692091a8fd14238dad3cef/Research%20documents/Cultural%20awareness%20.docx">here</a>
</p>

<h3 id="Agile">Agile</h3>
<hr>

<h4>What is Agile?</h4>
<p>
Agile is a project management approach that emphasizes flexibility, collaboration, and rapid iteration. It is often used in software development to help teams deliver high-quality software quickly and efficiently.
</p>

<h4>Popular Agile frameworks</h4>

<h5>Scrum</h5>

<p>
Scrum is an Agile framework for managing complex projects. It was originally developed for software development, but it has since been adopted in other fields as well.

In Scrum, a project is divided into a series of short iterations called "sprints." Each sprint is typically a few weeks long and has a specific goal, such as completing a certain feature or fixing a set of bugs. At the beginning of each sprint, the team holds a planning meeting to determine which tasks will be completed during the sprint. The team then works on these tasks throughout the sprint, with the goal of completing as much work as possible.

Scrum uses a number of roles to guide the work of the team. The "Scrum Master" is responsible for facilitating the process and helping the team to follow Scrum practices. The "Product Owner" is responsible for defining the features and requirements for the project. And the "Development Team" is responsible for completing the work and delivering value to the customer.

One of the key principles of Scrum is transparency. The team is expected to be transparent about its work and progress, and to regularly review and assess its performance. This helps the team to identify problems and improve its process over time.
</p>

<h5>Lean</h5>

<p>
Lean is a project management approach that is based on the principles of lean manufacturing, which was developed by Toyota to optimize the manufacturing process and reduce waste. In software development, Lean is focused on maximizing value and minimizing waste by eliminating unnecessary activities and focusing on what is most important to the customer.

One of the key tools that Lean teams use is the "Lean canvas", which is a visual representation of the key elements of a business model. The Lean canvas helps teams to identify the value they are delivering to customers, the activities that are necessary to deliver that value, and the resources that are required to support those activities. This helps teams to focus on what is most important and to eliminate unnecessary work.
</p>

<h5>Extreme Programming</h5>

<p>
Extreme Programming (XP) is a software development methodology that is designed to deliver high-quality software quickly and efficiently. It is based on a set of values and principles that emphasize collaboration, simplicity, and frequent delivery.

One of the key benefits of Extreme Programming is that it helps teams to deliver working software quickly and to respond to changing customer needs. By emphasizing collaboration and frequent delivery, XP helps teams to stay focused on delivering value to customers and to minimize waste.

</p>

<h4>Agile in group project</h4>

<p>

For our group project, we used Scrum, where we devided project in 5 sprints, each having 4 weeks.
Because we had multiple people leaving the project, we found ourselfs a bit lost, not sticking to the framework. However there were some sprints where our Scrum Master started each group project day with a daily stand-up which consists of everybody saying what is going to work on. The day ended with a stand-down on which we reflected on what was accoplished. Often our some of our group members left early which was an inconvienence because not always everyone was present.

At the end of every sprint we had a session of presentation with our clients on which we presented the work results of our sprint and together with them we planned the deliverables for the next sprint. We also listen to their feedback and changed our application based on requests. Finally the day will with a sprint retrospective where we openly spoken about what went well, what we should change and what we must not do.


The Agile tool that helped us develop our application is Azure Devops. In the second sprint we filled in the backlog(User Stories) that were decided with out product owner, and because our repositories were also there, it was easy for us to keep track which task and user stories where completed at every push. By using the sprint function we would assign every sprint a series of user stories that had to be completed, which helped us create burned down charts thus making it easier for Samuil to check how many hours were invested in that sprint. However not always this was the case due to the fact that not all of our team mates were using this function which made things a bit chaoting.

<h5>Sprint Board</h5>

<img src="https://github.com/TudorRu/S3-portfolio/blob/2be4867579556d966a5d62c7eb4d0fa864ad33bf/Images/board.png" width="1100" height="550">


<h5>Burned-down chart</h5>

<img src="https://github.com/TudorRu/S3-portfolio/blob/2be4867579556d966a5d62c7eb4d0fa864ad33bf/Images/burneddown.png" width="1100" height="650">

</p>

<h2 align="center">SkillRent</h2>
<h3>Project description</h3>
<p>
For the individual project I have decided to develop a application which will allow users to sell their knowledge and skills and provide their expertise. A user can be either one that provides services or one that buys services. The buyer is able to chose from a large variety of categories and from the best suited provider. Other similar websites are Fiverr, Toptal, Upwork, Upteam and many more.
</p> 
<h3>User stories</h3>
<hr>
<h4>User</h4>
<h4>US-1 - As a user I want to create an account so that I can fully take advantage of the website’s features.<h4>
<h4>US-2 - As a user I want to log in to my account so that I securely access the website’s features.</h4>
<h4>US-3 - As a user I want to log out of my account so that no one else can access it.</h4>
<h4>US-4 - As a user I want to edit my account so in case of a misspell happens or if my
details change.</h4>
<h4>US-5 - As a user I want to delete my account in case I don’t want to use the
platform anymore.</h4>
<h4>US-6 - As a user I want to be able browse the offered services list so that I can
chose one that fits my needs.</h4>
<h4>US-7 - As a user I want to be able to filter by categories the offered services list so
that I can quickly find one that fits my needs.</h4>
<h4>US-8 - As a user I want to be able to sort the list by price, high to low and low to
high, so that I can better find the one that fits by budget.</h4>
<h4>US-9 - As a user I want to hire someone so that he can do a job for me.</h4>
<h4>US-10 - As a user I want to be able to chat with the person I hired so that I can
communicate to him the details.</h4>
<h4>US-11 - As a user I want to be able to rate the person who did a job for me so that
other users can make an idea of the quality of services that he provides.</h4>
<h4>US-12 - As a user, I want to be able to post my skill offer, so that other users can hire me to do a job for them.</h4>
<h4>US-13 - As a user, I want to be able to edit my skill offer, so that I can change the details.</h4>
<h4>US-14 - As a user, I want to be able to remove my skill offer, so that it is not posted on the website.</h4>
<h4>Administrator</h4>
<h4>US-15 - As an administrator I want to log in my account with username and password to have minimum security level.</h4>
<h4>US-16 - As an administrator I want to log off from my account so that it is not used by someone else.</h4>
<h4>US-17 - As an administrator I want to be able to issue bans, in case users don’t comply to website terms and conditions.</h4>
<h4>US-18 - As an administrator I want to be able to issue unbans, in case users have proven that were banned for no reason.</h4>
<h4>US-19 - As an administrator I want to search for accounts in the list based on their username to be more efficient at my job.</h4>
<h4>US-20 - As an administrator I want to be able to create new administrator accounts
so that I have full control of who’s going to join as an administrator.</h4>
<h4>US-21 - As an administrator I want to have a list with all the user accounts and their status so I can have a better overview over them.</h4>
<h4>US-22 - As an administrator I want to search for accounts in the list based on their username to be more efficient at my job.</h4>
<h4>US-23 - As an administrator I want to be able to delete users’ skill offers, so that I can remove the inappropriate ones.</h4>
<h3>C4 model</h3>
<hr>
<h4>C1</h4>

<img src="https://github.com/TudorRu/S3-portfolio/blob/f769cc90a1b48f6cb76467a6c2448a6c179aa307/Images/C1-individual.png" width="800" height="500">

<h4>C2</h4>

<img src="https://github.com/TudorRu/S3-portfolio/blob/f769cc90a1b48f6cb76467a6c2448a6c179aa307/Images/C2-individual.png" width="800" height="650">

<h3>User friendly</h3>
<hr>
  
<h4>Why is it important?</h4>
<p>
Every developer should make sure that their application is user-friendly because it can lead to increased customer satisfaction and loyalty.
User experience is very important and it helps to ensure that a product or service is user-friendly, efficient, and enjoyable to use.
by considering the needs and preferences of users throughout the design process, UX can help to create products and services that are more accessible and 
inclusive for a wider range of people.
</p> 
  
<h4>Wireframes</h4>

<p>
Idealy when you are creating wireframes, you would also like to get immediate feedback from your product owner, in order to change your designs to their preference and needs, however given the circumstances of the individual project, I had no product owner, so I had to stick to my original design when developing the pages.
  
Some examples of the wireframes can be seen below.
</p>

<img src="https://github.com/TudorRu/S3-portfolio/blob/08125eab844343a84eb40247d981bd675073a52b/Images/Home%20screen.jpg" width="1000" height="600">
  
<img src="https://github.com/TudorRu/S3-portfolio/blob/08125eab844343a84eb40247d981bd675073a52b/Images/My%20profile%20page.png" width="1000" height="600">

  
<h4>Usability testing</h4>
  
<p>
When it comes to usability testing that are multiple ways to conduct it, such as moderated or unmoderated, remote or in person and explorative or comparative. Having access to my colleagues daily at work and my close ones due to holidays at home, I've decided to go with in person testing. I did not want to test my website on my university colleagues because I was affraid they would view it from a programmers point of view, which it wasn't what I was looking for, my goal being to obtain a normal user's angle. 

The plan was to let them navigate the whole website and then ask them a series of open-ended and close-ended questions in order to extract information on issues that I was taking into account and also them, providing them the oportunity to let me know what I needed to change in order to make the website user friendly. 
  
Although the testing was in person, I have decided to plot the resuls of some of the questions in order to better visualise the results   
</p>
  
<h4>The questions</h4>

<h5>Do you where the home button is?</h5>

<img src="https://github.com/TudorRu/S3-portfolio/blob/89f66a28c9d0659780afd58e454c0e774d5a0c57/Images/Sonarcloud-before.png" width="800" height="400"> 
  
As you can see from the results, everyone knew that home button is the logo picture from the navigation bar, and I feel this is because
this is the norm when it comes to every other website out there and people got used to it.

<h5>Do you know how to sign in?</h5>  
  
<img src="https://github.com/TudorRu/S3-portfolio/blob/89f66a28c9d0659780afd58e454c0e774d5a0c57/Images/Sonarcloud-before.png" width="800" height="400">

<p>  
It was not suprise to me that everone answered "yes" to this question because the button can be seen in the navigation bar bearing the same description text.
</p>
  
<h5>Do you know how to sign up?</h5>    
  
<img src="https://github.com/TudorRu/S3-portfolio/blob/89f66a28c9d0659780afd58e454c0e774d5a0c57/Images/Sonarcloud-before.png" width="800" height="400">   

<p>  
Again, everyone knew where to click in order to sign up, although the text of the button is "Join", which is self-explanatory.
</p>
  
<h5>What would you like to improve when it comes to the website?<h5>

<p>  
When asked this question, I have received 2 answers that I found very useful and thought that by implementing them it would bring an upgrade to my website.
  
First was that when click the "Browse" button and landing on the Browse Gigs page, it did not show exactly what gigs where showing and that made the users being confused.
</p>
  
<img src="https://github.com/TudorRu/S3-portfolio/blob/89f66a28c9d0659780afd58e454c0e774d5a0c57/Images/Sonarcloud-before.png" width="800" height="400">

<p>  
So in order to fix this issue, I have decided to add a breadcrumb bar, which indicates the Browse page category and sub-category.
By default, I've decided to automatically select the first category and the first sub-category and showing all the gigs from there.
</p>
  
<img src="https://github.com/TudorRu/S3-portfolio/blob/89f66a28c9d0659780afd58e454c0e774d5a0c57/Images/Sonarcloud-before.png" width="800" height="400">  

<p>
Second suggestion as related to the gigs card, the testers wanting to know, to whom it belongs that gig card.
</p> 
  
<img src="https://github.com/TudorRu/S3-portfolio/blob/89f66a28c9d0659780afd58e454c0e774d5a0c57/Images/Sonarcloud-before.png" width="800" height="400">
  
<p>  
To fix this, I've decided to add a picture icon followed by the username.
</p>
  
<img src="https://github.com/TudorRu/S3-portfolio/blob/89f66a28c9d0659780afd58e454c0e774d5a0c57/Images/Sonarcloud-before.png" width="800" height="400">
 
<p>  
Third complaint was again about the gig card, more precise, about not knowing what the asking prices is of the gig.

To tackle this issue I have added a footer to the card in which I'm displaying the starting price.
</p>
  
<img src="https://github.com/TudorRu/S3-portfolio/blob/89f66a28c9d0659780afd58e454c0e774d5a0c57/Images/Sonarcloud-before.png" width="800" height="400">  
    
<div id="fullStack">
<h3>Technology</h3>
<hr>
<h4>Front-end</h4>
<p>
In order to develope the front-end of my web application, I have went on and chose Vue.js. This decision was made because, having none to little experience with front-end, it was the same framework that we used for our group project, and I imagined that it was a good decision because if I were to get stuck at one point, I could always turn to the group project for inspiration.
Vue.js features an incrementally adaptable architecture that focuses on declarative rendering and component composition. The core library is focused on the view layer only. Advanced features required for complex applications such as routing, state management and build tooling are offered via officially maintained supporting libraries and packages.
Vue.js allows for extending HTML with HTML attributes called directives.[13] The directives offer functionality to HTML applications, and come as either built-in or user defined directives.
Along with Vue.js, I also decided to use bootstrap in order to create my components as it will lower the time spent on manually designing all the elements of the componenets.
</p>
<h4>Back-end</h4>
<p>
As well as with the group project, the best option for me was to use C# as the language for my back-end due to the fact that I am most familiar with it and it will take me less time to develop the application, unlike if I would have chosen Java.
.Net Core framework is rising in popularity and it has a big community which is willing to help and there a lot of tutorials online which can help me in writing the application with ease.
</p>
<h4>Structure</h4>
<p>At this moment the back-end solution is made out of 2 projects, first one that contains the actual api, logic and connection to the database and the second one that holds the tests. After discussing with Jean-Paul, I am planning to split the first project into multiple ones as it is best practice and it will take advantage of C# language true power in bringing multiple projects into 1 solution. It will be split into 3 separate projects: Business layer, Data Access Layer and Data Transfer Object layer.
</p>
<h4>Data persistance</h4>
<p>
For database I am using Azure MYSQL database, and in order to create my tables in the database and seed them I make use of Entity Framework Core that will greatly cut the coding time and will help me save, edit, delete and fetch data from my database.
</p>
</div>
<div id="qualityAssurance">
<h3>Quality Assurance</h3>
<hr>
<p>
Quality assurance is the term used in both manufacturing and service industries to describe the systematic efforts taken to ensure that the product delivered to customer meet with the contractual and other agreed upon performance, design, reliability, and maintainability expectations of that customer.
</p>
<div id="UTest">
<h4>Testing</h4>
<h5>Back-end</h5>
<p>
As of now, if have decided to make unit test for my controller classes which are responsible with retrieving data from my database and issuing responses based on the results.As you can see in the below picture my current code covarage is 9.5% on 147 lines of code and I'm planning to bring that up to above 40%, and to achieve that procentage I will also need to implement integration tests to ensure my controller classes can interact with my database and make the correct calls from it, without losing or changing pieces of data. However for this I will need to setup a proper test environment which will be done later in the development. 
</p>

<p>
In order to improve my code quality, I chose to use SonarCloud. This tool will scan my code after every push to the dev branch and will generate a report which will be published on the SonarCloud website. This will allow me to analyze and take in consideration which code needs to be refactored and reviewed before pushing to the main branch.Some of the features of this tools are code covarage, telling me how much of the actual code has been tested, duplicate code which will be responsible with showing me which code is repeated and how can it be refactored in such way that 0 duplication score will show and last, security review, where it will point out any exposed credentials.

Below, there are 2 screenshots, first one is an example of report of my code without tests and in the second one, you can see my code covarage going up as my
I implement unit tests.
</p>

  
<img src="https://github.com/TudorRu/S3-portfolio/blob/89f66a28c9d0659780afd58e454c0e774d5a0c57/Images/Sonarcloud-before.png" width="800" height="400">

<img src="https://github.com/TudorRu/S3-portfolio/blob/bad8ad26556d86c76c56283c7b9da0e3e780ba2f/Images/sonarcloud-after.png" width="800" height="400">

<h5>Front-end</h5>
<p>
To test that my front-end application is working properly, I've decided to implement unit tests where I check if my routes are working properly and also that my components are generating the correct elements.
In order to achieve this, I've opted for Jest which is a popular JavaScript testing framework. A pipeline will run after a push to the dev branch will be made, which is going to run all the tests run the coverage and publish the code coverage results to Azure DevOps Pipeline.

Below you can see an example of such a report.
</p>

<img src="https://github.com/TudorRu/S3-portfolio/blob/9a3f88a385723c7ea723094bfc8e3cd97461eb27/Images/cobertura.png" width="1000" height="500">

</div>
</div>
<div id="Pipeline">
<h3>Continuous Integration and Continuous Deployment</h3>  
<hr>
<p>
In order to automate testing and deployment of my back-end and front-end application, four pipelines have been created using Azure Pipelines, two for each repository.
Specific pipelines are triggered when ever pushes are being made either to dev or main branches. When a push to dev branch is being made, the tests will run and in case one or more will fail, the whole pipeline will fail, notifying the developer that push to main cannot be made.
In case the application is ready for release, a push to main will be made, which will trigger the building and deploying pipeline.

Below you can see a screenshot will the pipelines I have instated for both front-end and back-end.
Further I will explore the yaml files for all the pipelines and explain them
</p>
  
<img src="https://github.com/TudorRu/S3-portfolio/blob/c4f167fd71998f709d89e10ecf3ba2909370dacd/Images/pipelines.png" width="700" height="500">
    
<h4>Test pipeline for back-end</h4>

<h5>Build Task</h5>

<img src="https://github.com/TudorRu/S3-portfolio/blob/c4f167fd71998f709d89e10ecf3ba2909370dacd/Images/test-build-task.png" width="700" height="200">
  
<p>
This stage will test if my application will building without any errors with the correct build configuration.
</p>

<h5>Test Task</h5>

<img src="https://github.com/TudorRu/S3-portfolio/blob/c4f167fd71998f709d89e10ecf3ba2909370dacd/Images/test-test-task.png" width="400" height="200">

<p>In the above picture, you can observe that the pipeline will automatically detect the test project and will run all the tests found, and generating a code coverage
report which will be analyzed in SonarCloud.
</p>
  
<h4>Deploy pipeline for back-end</h4>

<h5>Build docker image task</h5>

<img src="https://github.com/TudorRu/S3-portfolio/blob/c4f167fd71998f709d89e10ecf3ba2909370dacd/Images/build-docker-task.png" width="600" height="200">

<p>The Docker@2 task will build a Docker image and it is going to be pushed to Azure Container Registry.</p>

<h5>Deploy API</h5>  
  
<img src="https://github.com/TudorRu/S3-portfolio/blob/c4f167fd71998f709d89e10ecf3ba2909370dacd/Images/deploy-deploy-task.png" width="600" height="200">
   
<p>  
The AzureWebAppContainer@1 will  deploy the image to Azure App Container, which in reality is URL from which the api can be used from any computer or application with internet connection.(https://skillrent-api.azurewebsites.net)
</p>
  
<h4>Test pipeline for front-end</h4>
  
<img src="https://github.com/TudorRu/S3-portfolio/blob/c4f167fd71998f709d89e10ecf3ba2909370dacd/Images/test-node-task.png" width="300" height="200">

<p>
This task will install Node.js version 18 so that further steps can run.
</p>

<img src="https://github.com/TudorRu/S3-portfolio/blob/c4f167fd71998f709d89e10ecf3ba2909370dacd/Images/test-script-task.png" width="500" height="200">

<p>  
The above script will install Node Package manager followed by running the unit tests and also generating the code coverage.
</p>  

<img src="https://github.com/TudorRu/S3-portfolio/blob/c4f167fd71998f709d89e10ecf3ba2909370dacd/Images/test-publish-task.png" width="1000" height="300">

<p>
This task with publish the generated code coverage results to Azure DevOps using Cobertura tool.
</p>  
<h4>Build and deploy front-end</h4>
  
<img src="https://github.com/TudorRu/S3-portfolio/blob/c4f167fd71998f709d89e10ecf3ba2909370dacd/Images/deploy-frontend.png" width="1000" height="500">

<p>
The above job will build my front-end application and deploy it using Azure Static Web Apps./n
The webiste is live right now on https://thankful-plant-0513f9a03.2.azurestaticapps.net.
</p>
</div>

<h3 id="PManner">Professional manner</h3>
<hr>

<p>
  
During this semester I had some conversations with Jean-Paul, however I only got the idea and the values of these only towards the end, where, after a gap of 1 month I finally met with him and he fully explained to me why in The Netherlands, admiting that getting stuck on something or not being able to make progress is not nothing to be ashed of and the faster that this is established the better.

These conversations were followed by Jean-Paul opening a feed pulse checkpoint where I should make a brief summary of his feedback and what I should work on further.
An example of this can be seen in below screenshot.
</p>

<img src="https://github.com/TudorRu/S3-portfolio/blob/8736e17e99a8e0537933028274c799795a08f83e/Images/feedpulse.png" width="1000" height="450">

<h3 id="Ethics">Ethics</h3>
<hr>

<h4>Ethics in software engineering</h4>
<p>
Software engineering ethics is the study of moral principles and values that should guide the design and development of software. It is a branch of computer science ethics, which is concerned with the ethical issues related to the use of computers and technology.
  
Responsibility is one of the main key principles of ethics and refers to the fact that software engineers have to be resposible when creating software, making sure that it is reliable, safe and secure. Professionalism indicates that software engineers should behave in a professional manner and uphold the values and standards of their profession. This includes being honest, transparent, and respectful of others. Another key principle is fairness which means that the software created must fair and unbiased and shouldn't not perpetuate or amplify existing inequalities. Last, developers should be open and transparent about the design and function of their software, any potential risk or limitation must be brought forward so that users can be aware of them.
</p>
  
<h4>Resposibility in SkillRent</h4>
<p>
Although, I did not get the change to implement a login system, I have taken into account that users will be storing valuable informations regarding to their accounts, such as passwords and bank details. In order to prevent any sensitive information theft, I have considered to save bank accounts details and passwords only after hashing them by making use of SHA-256 algorithm. With this solution we will be making any text unreadble, rendering it useless to any attacks should succeed on our database.

Another step that will secure our database that I have already taken is by not utilizing any raw SQL quaries when using Entity Framework in order to fetch or manipulate data. By using LINQ I have ensured that SQL Injection attacks will be prevented.  
</p>
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  


