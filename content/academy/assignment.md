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

The page lists all the designers who are active on EmptyCup's platform. Any homeonwers interested in finding a designer who they
can collaborate with can come to this listings page where they can see all our users who are available for business.


### 1. Web page + Styling

Your objective is to create a single mobile web page that looks exactly like the given design.

Styling matters a lot. EmptyCup's users are designers and have a very sensitive taste. They will ditch the product and worse, lose respect for EmptyCup & it's products, if the styling is off. So, the first requirement is that the page you create should look exactly like the figma design. You can use the same fonts and icons as in the Figma file by downloading the icons from Figma itself. 

This demonstrates your ability to work with HTML & CSS code. When it comes to writing software for production environment, HTML CSS fluency is paramount. You probably used websites before where some buttons are not visible or the content layout is screwed up. That was because the person who wrote the HTML didn't get it right. So, this is the most basic test.

__If you can create a page that is an exact replica of this design, you can submit your assignment, even if you don't have the rest of the functionality implemented.__

_If you finish this successfully on your own and submit, a mentor will get in touch with you to guide you and share useful learning resources if you need to learn something new._

### 2. Shortlisting

Once you have the page ready, you should work on making the page dynamic through Javascript. For this, you should add the shortlisting functionality. For every listing, on the right there are 4 action items. Details, Hide, shortlist, report. You have to implement the functionality for the 3rd shortlist button. The shortlist button is a toggle button. If selected, the icon inverts (line icon to fill icon and vice versa). Fill icon indicates that the listing has been shortlisted. All shortlisted listings can be viewed using the "Shortlisted" filter on the top bar. The "Shortlisted" filter is also a toggle icon. When it is toggled on, only shortlisted listings are shown below. If toggled off, all listings are shown.

__If you can implement this, it shows you have a decent command over writing Javascript. EmptyCup is a web based interior design tool. So, our product is heavily dependent on Javascript. If you can implement this, you will be able to handle a lot of our codebase.__

_You can ignore the rest of the action buttons on each listing._

### 3. Backend integration

The next step is to get the data for all the listings. This data shouldn't be hardcoded in the HTML files. It needs to be queried from the backend. The best way to implement this is by deploying a simple python based REST API using Flask that returns all the listings data as a JSON object. 

If you haven't worked on any REST API project before, the best way to start would be by saving the data in a static JSON file that will be served along with the HTML page. The javascript linked in the HTML page will load the JSON file as a static asset just like loading an image. Once you have that working, you can create a separate API server to serve this JSON from a DB.

__If you can implement this, it shows that you have full stack capabilities. A full stack developer is way more efficient because there are no communication overheads between frontend and backend work. At EmptyCup, all your work will have both frontend and backend components.__

_If you don't have experience with backend development, you can ask your mentor for useful references to learn how to build a REST API backend in python._

### 4. Public cloud deploy


Once you have both the frontend and backend ready, you should figure out how to deploy them publicly. Frontend code is static and can be deployed by a service like Netlify. Deploying on netlify will not be very complex. You can even have simple link between your Github repository and Netlify, so that whenever you push your code changes to Github, Netlify automatically deploys the latest code.

Deploying backend code is a little more complex. Depending on the cloud and the backend technology you use there are multiple options. At this point, probably the easiest would be to get a cloud vm and run the API server there. Deploying to AWS Lambda or Azure Functions should also be possible.

__If you can deploy publicly, it shows that you have a good understanding of devops as well. Most beginners neglect devops thinking code is the important part. But devops is as important as programming and is the gateway to bring your programming skills into the real world.__

_Deployment needs a good understanding of basics of computer science like OS and networking. If you miss something crucial, it can become frustrating easily. You should speak to your mentor and discuss your deployment plan before._


### Evaluation

The deadline for assignment is: __6.00 AM on December 1st__

DO NOT wait for the deadline as the assignment can be submitted again and again. Only the final version will be considered for evaluation. Besides, as soon as your first stage is complete, you will be assigned a mentor who will help and guide you. Your mentor's recommendation will give you a big advantage in final evaluation. So, submit as early as possible and as soon as you finish the basic web page layout and styling.

To submit the assignment, you need to submit 2 files: 

1. A zip file containing all your code with the name "Your Name.zip". Please make sure your codebase contains a _README.md_ in the root folder which gives step by step instructions to run and preview your code.
2. A screen recording demo of your work in action.  

You can submit the 2 files by emailing them to __tryouts@emptycup.in__ with the subject __EmptyCup Assignment 2023 - Your Name__

_NOTE_: 

1. The zip file with your code has to be named in the format "Your Name.zip"
2. The demo file with your screen recording has to be named in the format "Your Name.mp4" (or whatever file extension)

_Please do not put the recording file inside the zip._

_If your file size is large, gmail may not allow you attach the file directly. In that case please upload the file onto google drive and share the link. Gmail may offer to do this automatically._

_Sometimes, college email addresses get blocked when sending large files outside the organisation. Hence, it is recommended that you submit with your gmail account._

You only need to finish the first stage (web page with styling) to be considered for the internship position. But, the more you are able to accomplish, the better your chances will be. Besides, these are very useful skills that can help you level up your profile. So, you should see this not just as a test, but a learning opportunity. Our mentors will be available through out to help and guide you.

Unlike a typical interview or test, you are encouraged to Google as much as you can and learn while doing the assignment. You'll remember whatever you learn to finish this assignment much better than anything you learnt from your textbooks for your exams. 

__We request you to please keep your repository private on Github. If you need, you can grant private access to your mentor. If we detect plagiarism, everyone involved may be disqualified.__

_CAUTION: We strongly advise that you don't waste your time and our time by copying or duplicating code from someone or somewhere else. There will be a detailed code review at the end where a mentor will walk through your entire codebase. We are atleast as smart as you and we will know. Even if we don't, you won't be able to maintain that image for more than a week when you start your internship as the work will be intense and you won't be able to copy or get outside help. We will take strong action if we find out you misrepresented your work._


### Mentorship

1. A lot of students get inspired and start with high expectations. Then, as they face errors or roadblocks become demotivated and give up. Instead, you should start with the expectation that this work will not be easy. A reasonable expectation for someone who already knows web development well is to finish the entire assignment in 100 hours. So, grit your teeth and start with a prepared mindset.

2. Interviews and tests involve a lot of parameters that are out of your control. There is a big hand of chance in the equation. The idea might not strike for you. You might get hit with an unexpected question. You might not be able to communicate properly. The interviewer might be in a bad mood or exhausted at the end of the day. We adopted an assignment model to make it possible for hard work, persistence and determination to shine through despite random chaos. Be persistent, don't give up and you'll have a good time.

3. Motivation is very expensive. Don't expect you'll have the same motivation tomorrow. Get started whenever you are motivated and make it easy for yourself to get back to work. Don't push yourself to burnout, leave some gas in the tank everyday, so that you feel like coming back the next. Read more about [staying motivated](/academy/motivation).

Follow [EmptyCup's linkedin page](https://in.linkedin.com/company/emptycup) for knowing more about the company, our culture and our work. 


### Certification

Anyone who successfully submits the assignment (even just the first stage) will receive a "Certificate of Accomplishment" from EmptyCup regardless of selection for internship. Your github id will be added as a contributor to EmptyCup's open source project repository. You may also request your mentor for a referral.

This assignment is purely for evaluation purposes and EmptyCup will not be using your code even for the open source projects without your explicit permission.