---
layout: default
title: EmptyCup Assignment
---

_This assignment is for students applying for the [internship](/academy/internship) starting Jan 2024._


The assignment is a single mobile web page. It is the only test in the selection process
for the [EmptyCup Internship](/academy/internship/) starting January 2024. 



### Assignment

![Portfolio Assignment Page](/images/portfolio-assignment.png)

You can find the [exact design spec here](https://www.figma.com/file/20X8K2LQCic6q0rymE6eAb/Portfolio?type=design&node-id=0%3A1&mode=design&t=EetjKRzW11jt8xqf-1). You can hide all the comments using the keyboard shortcut __Shift + C__.

The page lists all the designers who are active on EmptyCup's platform. Any homeonwers interested in finding a designer who they can collaborate with can come to this listings page where they can see all our users who are available for business.


### 1. Web page + Styling

Your objective is to create a single mobile web page that looks exactly like the given design.

Styling matters a lot. EmptyCup's users are designers and have a very sensitive taste. They will ditch the product and worse, lose respect for EmptyCup & it's products, if the styling is off. So, the first requirement is that the page you create should look exactly like the figma design. You can use the same fonts and icons as in the Figma file by downloading the icons from Figma itself. 

__This demonstrates your ability to work with HTML & CSS code. When it comes to writing software for production environment, HTML CSS fluency is paramount. You probably used websites before where some buttons are not visible or the content layout is screwed up. That was because the person who wrote the HTML didn't get it right. So, this is the most basic test.__


_NOTE: DO NOT request edit access to the Figma file. You can duplicate the file and edit it if you wish to play around with the design_

### 2. Shortlisting

Once you have the page ready, you should work on making the page dynamic through Javascript. For this, you should add the shortlisting functionality. For every listing, on the right there are 4 action items. Details, Hide, shortlist, report. You have to implement the functionality for the 3rd shortlist button. The shortlist button is a toggle button. If selected, the icon inverts (line icon to fill icon and vice versa). Fill icon indicates that the listing has been shortlisted. All shortlisted listings can be viewed using the "Shortlisted" filter on the top bar. The "Shortlisted" filter is also a toggle icon. When it is toggled on, only shortlisted listings are shown below. If toggled off, all listings are shown.

__If you can implement this, it shows you have a decent command over writing Javascript. EmptyCup is a web based interior design tool. So, our product is heavily dependent on Javascript. If you can implement this, you will be able to handle a lot of our codebase.__

_You can ignore the rest of the action buttons on each listing._

### 3. Backend integration

The next step is to get the data for all the listings. This data shouldn't be hardcoded in the HTML files. It needs to be queried from the backend. The best way to implement this is by deploying a simple python based REST API using Flask that returns all the listings data as a JSON object. 

If you haven't worked on any REST API project before, the best way to start would be by saving the data in a static JSON file that will be served along with the HTML page. The javascript linked in the HTML page will load the JSON file as a static asset just like loading an image. Once you have that working, you can create a separate API server to serve this JSON from a DB.

__If you can implement this, it shows that you have full stack capabilities. A full stack developer is way more efficient because there are no communication overheads between frontend and backend work. At EmptyCup, all your work will have both frontend and backend components.__

_If you don't have experience with backend development, you can start with using Flask on Python. There are good Flask Tutorials on YouTube to get you started. There are some good tutorials for API development by Miguel Grinberg for REST API development on Flask._

### 4. Deployment

There are 2 modules in deployment:

1. Local deployment for development
2. Public cloud deployment for demo

For local deployment, you should use Docker. If you are not aware of Docker, you can find a lot of simple tutorials to setup docker locally. You will have to create containers for all the services that you need to run your app properly including the DB. Ideally, a local dev deployment should work without an internet connection. Once you create the containers, you should be able to orchestrate those containers using `docker-compose`. Ideally, it should be possible for someone to just pull your repo and deploy locally without any instructions from you. Make use of the _README.md_ file.

Once you have the build working locally on docker, you should figure out how to deploy publicly. Frontend code is static and can be deployed by a service like Netlify. Deploying on netlify will not be very complex. You can even have simple link between your Github repository and Netlify, so that whenever you push your code changes to Github, Netlify automatically deploys the latest code. Deploying backend code is a little more complex. Depending on the cloud and the backend technology you use there are multiple options. At this point, probably the easiest would be to get a cloud vm and run the API server there. Deploying to AWS Lambda or Azure Functions should also be possible. You can also deploy the docker containers directly.

__If you can deploy publicly, it shows that you have a good understanding of devops as well. Most beginners neglect devops thinking code is the important part. But devops is as important as programming and is the gateway to bring your programming skills into the real world.__

_Deployment needs a good understanding of basics of computer science like OS and networking. If you miss something crucial, it can become frustrating easily. If you get stuck, you can ask for help on the Slack community channel_


### Submission

~~The deadline for assignment is: 6.00 AM on December 1st.~~

_Due to conflicting timelines, a deadline extension has been granted for a few colleges. Please refer to the notice from your placement team for the actual deadline. The evaluation happens on a rolling basis. So, if you finish and submit early you, you will have a definite advantage._

To submit the assignment, you need to submit 2 files: 

1. A zip file containing all your code with the name "Your Name.zip". The zip file should yield a "Your Name" folder containing all the code when it is unzipped. Please make sure your codebase contains a _README.md_ in the root folder which gives step by step instructions to run and preview your code. The zip file with your code has to be named in the format "Your Name.zip". DO NOT add further any extra words like Final or ' -2' etc. There is an automated system that picks up your assignment and categorizes it for evaluation. So please follow the instructions precisely.

2. A screen recording demo of your work in action. The video should show the demo of the webpage including the shortlisting functionality (~1min). It should then show your database schema (~1min). After that it should show the hierarchy of all files in your source code folder(~1min). It should show the backend code for your API routes(~1min). It should show the UI components (~1min). You should explain each module with a voice over. You can use [Loom for screen recording](https://www.loom.com/) or any other software you're comfortable with.

You can submit the 2 files by emailing them to __tryouts@emptycup.in__ with the subject __EmptyCup Assignment 2023 - Your Name__. Based on your submission, you will be shortlisted for an online code review. This will be a online video call where we'll walk through your code line by line and discuss it with you as we would when merging your code into production.

_Sometimes, college email addresses get blocked when sending large files outside the organisation. Hence, it is recommended that you submit with your gmail account. In the email, please mention your college name._

_If there is a problem attaching the files to your email, you can use Google drive to upload and share the assignment code & demo video. The filename guidelines should still be followed._

_The assignment can be submitted multiple times. Only the final submission will be considered for evaluation. So, DO NOT wait till the deadline to submit your assignment. If you are submitting the assignment for the second time. Please reply on your exisiting email thread. DO NOT create new email threads for each submission._

_We request you to please keep your repository private on Github. You can grant private access to your mentor, if and when they ask. If we detect plagiarism, everyone involved may be disqualified._

_CAUTION: We strongly advise that you don't waste your time and our time by copying or duplicating code from someone or somewhere else. There will be a detailed code review at the end where a mentor will walk through your entire codebase. We are atleast as smart as you and we will know. Even if we don't, you won't be able to maintain that image for more than a week when you start your internship as the work will be intense and you won't be able to copy or get outside help. We will take strong action if we find out you misrepresented your work._


### Evaluation

Once you submit, your work will be evaluated based on the following criteria:

__Correctness__: Whatever little you implement should work flawlessly. In the real world, you don't get 80% marks for 80% correct, you get 0%. If it doesn't work, it doesn't work.

__Completeness__: If you complete the whole assignment with the frontend, backend and deployment, you will have an advantage over someone who submits a partial implementation. This just shows hard work.

__Code quality__: Good quality code is clean, well organized, readable, concise and simple. Writing simple code is much harder than writing complex code. It shows your elegance in structuring your code. 

Apart from the above technical criteria, we also evaluate your communication during the code review. Here are a few things taken into consideration. For eg:

 
1. Do you think through before communication? It is important to have as much clarity as possible before you initiate a conversation. Otherwise, you will get that clarity in the conversation at the expense of the other person's time and attention.

2. Is your communication itself clear? If you don't present your work clearly, the other person will have to spend their attention not on your code, but on understanding you. 

2. Are you logical in your communication? If you take everything personally, it becomes hard to give feedback on your work so that it can be improved. Can you accept a flaw and focus on fixing or improving it rather than taking it personally and arguing about it?


If you have finished the assignment and have time, energy & drive, there are a few things you can do to stand out:

1. Implement new functionality. An excellent challenge would be implementing the gallery view. In the gallery view, each listing will also have a few images of their work uploaded by the designer. Each listing will have an instagram like image carousel above the listing details. For this you have to improvise the UI design yourself. This will also test your backend ability because you have to manage file uploads and asset storage in the cloud. Implementing this will show that you can take ownership of a feature which will be a huge plus in your evaluation.

2. Implementing using our stack, especially Svelte for frontend. You need not use our stack to submit the assignment. But, choosing to learn our stack will show your ability to learn something fast and your drive to excel. Besides, if you join the company you'll have to master this stack anyways.

3. Your own idea on how to improve the project with justification about why that is not just a minor polish to boost your ego.


### Mentorship

[Join the EmptyCup slack community for any questions or doubts regarding the assignment.](https://join.slack.com/t/emptycupacademy/shared_invite/zt-256nm43bn-BNQb_UeEn3mI2QrnjMJ9GA)

1. Mentorship will be provided based on your performance. If you're showing promise, we will help and guide you as much as we can. Mentorship is not a right. It is a privilege that needs to be earned. The irony is that if you google and try to figure out as much as you can, we will try to help you as much as we can. If you don't do everything you can to help yourself (starting by googling), we won't be interested in helping you.

2. Don't get blocked on response from mentors just to proceed. The default state is Go. No one will come and give you permission to proceed. Just keep going. A mentor is not a coach who will drive you. You have to bring the drive yourself. A mentor will only help you if you get stuck and guide you if you're on the wrong path. But the initiative and the drive have to come from you. 

3. The more specific your request is, the more likely you'll receive guidance. If you say: "I need help with backend deployment", mentors probably will not bother. You can figure that out on your own. But if you ask: "I implemented using Django and don't need 2 separate docker containers to deploy locally. Should I still separate frontend and backend?", the mentor will respond quickly.

That said, if you get stuck or are not sure how to proceed, you can ask on Slack for help. We will try to address and help out as much as we can. We just don't want you to take mentorship for granted.

Here is some general guidance on how to go about the assignment:

1. A lot of students get inspired and start with high expectations. Then, as they face errors or roadblocks become demotivated and give up. Instead, you should start with the expectation that this work will not be easy. A reasonable expectation for someone who knows basic web development well is to finish the entire assignment in 100 hours. So, grit your teeth and start with a prepared mindset.

2. Interviews and tests involve a lot of parameters that are out of your control. There is a big hand of chance in the equation. The idea might not strike you. You might get hit with an unexpected question. You might not be able to communicate properly. The interviewer might be in a bad mood or exhausted at the end of the day. We adopted an assignment model to make it possible for hard work, persistence and determination to shine through despite random chaos. Be persistent, don't give up and you'll have a good time.

3. Motivation is very expensive. Don't expect you'll have the same motivation tomorrow. Get started whenever you are motivated and make it easy for yourself to get back to work. Don't push yourself to burnout, leave some gas in the tank everyday, so that you feel like coming back the next. Read more about [staying motivated](/academy/motivation).

Follow [EmptyCup's linkedin page](https://in.linkedin.com/company/emptycup) for knowing more about the company, our culture and our work. 

__If you have any questions or queries, please ask on the Slack channel__.


### Certification

Anyone who successfully completes the assignment ~~UPDATE: 21-11-23 (even just the first stage)~~ will receive a "Certificate of Accomplishment" from EmptyCup regardless of selection for internship. Your github id will be added as a contributor to EmptyCup's open source project repository. You may also request your mentor for a referral.

This assignment is purely for evaluation purposes and EmptyCup will not be using your code even for the open source projects without your explicit permission.