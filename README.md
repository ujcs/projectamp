# ProjectAMP
Academic Management Program (Managing courses and resources)

The readme for this project outlines the goals for the project and the tools that are (intended) to be utilized. It is anticipated that as the project comes together, any and all of it may shift to better integrate the various goals and any improvements users or contributors come up with.

This is a "in my spare time," "neat things to try," "let's give students a demo of how this might work" start to a project. However, the goals are real and the project is being open sourced as it might very well be of interest to others. I am confident that I can't be the only one managing this in clunky spreadsheets who is well aware there are much better (and more scalable) of accomplishing the functions described below.

*ProjectAMP has two main components: Course Management and Resource Management.*

**Resources Management:**

- Instructors (From application intake, skills matrix, course assignments, notes)
  - *The skills matrix being the most critical (this would be a porting of a spreadsheet to database)*
- Course Materials (What books or subscriptions are needed for a course, UNI or Student Responsibility. So tied to an individual course)

**Course Management:**

- Course Catalog listing all courses (All courses are tied to a particular program. Programs could be tied to a "school," though in just about every case a program should be sufficient. Courses can be found in multiple degrees, certificates, but degrees/certs will only be part of one particular program.)
- Course Planning (Calculating deadlines for development, issuing contracts, etc. based off of when the course is next slated to be taught.)
  - *Tying to skills matrix for instructor selection being the most critical (i.e. identifying who is qualified or capable of teaching a particular course)*

The approach is to make this a full web application to allow for scalability and modularization. Careful consideration was given to the strengths and weaknesses of various languages and approaches for the project, so while there are likely many other ways to accomplish the broad functions as described above, the below stack is what has been selected for initial development.

**Development Stack (Still under consideration and evaluation):**

PERN/MERN stack has been suggested as more responsive and scalable than utilizing Python. So the most likely stack of technology for this project is:

- PostgreSQL *(Though CockroachDB has been suggested as a drop-in replacement as it might be better in a Kubernetes cluster scenario. PostgreSQL scales better vertically, while CockroachDB scales better horizontally.)* Other than file attachments, all other intended data should work just fine with a traditional relational database.
- Express: Framework and API to work with Node.JS
- React: Front-end way for creating the UI, fast and efficient.
- Node.js: Runtime environment that scales well in many platforms.
- Front-end: Utilize a Tailwind CSS theme. However, while author is agreeable, licensing considerations from platform might impact. So functionality wise, modularization or a base "theme" that can be distributed via the project might need to be considered. (https://themeforest.net/item/lineone-multipurpose-admin-and-webapp-ui-kit-based-on-tailwind-css/38247812) 

**Unknown (Need to further research) tool needs/integration:**

- File Management (Attach PDFs or Docs to Instructors. Resumes for example. Attach reference documents such as proposals or change memos to courses.)
- User Management
- Front-end considerations (Anything particular for frameworks beyond HTML/CSS/JS?)
- Any additional consideration for running in Kubernetes environments? (Helm Charts, etc.)
- Backup/Restore Functionality. (Full application and just database options?)
- Proper handling of upgrades/updates to code base.

**Future Enhancement ideas**

- To-do dashboard and tracking for program directors (Issue contracts, courses to develop, etc)
- Integration with Email. 
  - Todo reminders, periodic summaries, etc.
  - New application alerts (if application portal functionality is integrated) 
- Application Portal
  - Instructors to directly submit applications to be reviewed by program directors.
  - Instructors reviewing skills matrix and suggesting updates? This may or may not be desired functionality as applicants also often indicate interest in areas, but might not have experience, so a judgement call by the program director if marking off as having that "skill"
- Fulltime vs part time faculty
- Budgeting (This might not be desirable as it could get messy in a hurry and be an extra level of data security needed beyond the normal PII.)
