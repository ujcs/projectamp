***The below is a compilation of existing notes on possible workflows, functions, etc. As the progress gets started, cleaning this up into defined user stories for a creating a development roadmap.***

**Entry:**

-> New application (in response for a particular program: ex: Computer Science adjuncts or designers) -> Enter in information -> Indicate designer/adjunct/skills that might *be relevant* 

- link or reference one or more files attached (pdf or doc)… embed files or link to network location? 

**During entry ability to flag “priority” ones or special note field. (Ie, stood out on first read, military service, notable teaching experience, etc)* 

-> New Program

-> New Certification tied to a program

-> New Course assigned to one or more certifications (Example, Networking is in mult certs. CS140 *could* exist in multiple certs in multiple programs)

**Extraction:**

- Course needs to be designed, filter on who has been flagged as having one or more of the relevant skills associated with that course. Assign designer or redesigner. Assign adjunct (per section offered) and adjuncts can be assigned to multiple sections. 

- Specific course, filter on who is applicable

**Possible pages:**

Instructors

Quick Check

Settings

- Skills
- Skills Categories
- Course Categories

Account settings (email/username, name, password etc)

**Courses page:**

- Upper right corner would be a New course button -> goes to a screen to add a course and select desired skills
- Main page content will list all courses with a category filter and a search bar at the top of the results table
- Clicking on a course will bring you to an edit course page (similar to the create course page)
- Option to delete a course would be on the edit course page

**Instructors page:**

\- Upper right corner would be a New Instructor button -> goes to a screen to add the instructor and assign skills

\- Main page content will list all instructors by default

 \- Ability to search by name using a search bar

 \- Ability to filter by selecting a course

 \- Ability to filter by selecting a course category

\- Clicking on an instructor will bring you to a instructor overview page

 \- Will list all eligible courses

 \- Allow editing skills

 \- Button to delete instructor

**Quick Check page:**

\- Main page content is a list of the skills categories with collapsing sections. Each section contains all the skills with a checkbox for each one.

\- Above the list is a search bar to search for particular skills. This would simply temporarily hide any that do not match the search until the search is clear

\- At the bottom is a button to View Course Matches which will then replace the main screen content with a list of courses that the selected skills would be good for

\- A button to reset the page

\- A button to create a new instructor based on the selected skills -> goes to the previously described create instructor screen with the skills already selected

Settings -> Skills Categories:

A simple page that just lists categories in a list with options to edit the name, delete them or create new ones.

Settings -> Course Categories:

A simple page that just lists categories in a list with options to edit the name, delete them or create new ones.

Corrected Settings -> Skills:

A simple page that just lists skills in a list with options to edit the name, delete them or create new ones. When creating or editing one you can select the skill category.

Database tables:

\- Skills (simple list of skills)

\- Skill Categories (simple list of skill categories)

\- Courses (simple list of courses)

\- Course Categories (simple list of course categories)

\- Instructors (simple list of instructors)

\- Skill Category Assignments (simple list with a FK to a skill and a FK to a skill category)

\- Course Category Assignments (simple list with a FK to a course and a FK to a course category)

\- Instructor Skill Assignments (simple list with a FK to a instructor and a FK to a skill)

So I imagine this workflow upon setup of the application as a whole:

Initial setup only done once (or adding/removing as needed):

1. Setup user account
2. Create Course Categories
3. Create Skill Categories
4. Create skills

**For each person:**

1. Add them or use the quick check
2. View things they can do

**Org Admin:**

\- Create/manage courses and everything

\- Create/manage sub-users who can also managed courses etc

**Manager:**

\- Create/manager courses and stuff

\- This is the sub-user of a org

**Instructor/user:**

\- Could potentially have each one added send a email to the person to create their account and have it so they can also update their own skills and see courses they are eligible to work with