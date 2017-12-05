FlaskApp
A Comic Book Repository
Zack Bennett-Engler
2017


Description of Package Contents:

app.py - is the python file which runs the website, handles user input, and re-routes the user from one webpage to another.
diagrams - is a folder containing the UML and EER diagrams for the repository’s database.
flask - is a folder containing Flask, a python micro framework used to run the website.
mysql - is a folder containing the necessary .sql files to create the repository’s database in MySQL Workbench.
static - is a folder containing the static elements of the webpage, which consists of the JavaScript, jQuery, and CSS files. This folder also contains a folder in which user uploads will be stored.
Superman.pdf - is a Superman comic that can be used to demonstrate the website’s functionality. Or you can just read it.
templates - is a folder containing the html files for the website.
README - this.



Software Needed:

Python - the flask folder contains the necessary files for both flask, as well as Python v2.7.
jQuery - the static/js folder contains the necessary jQuery files.
MySQL - the user will need a MySQL username and password.
MySQL Workbench - for the repository’s database.



Building Instructions:

1. Open MySQL Workbench and run FlaskApp_mysql_code.sql, which is in the mysql folder, to set up the database. 
2. Using Terminal, navigate to directory where you have downloaded this project. For example, if the FlaskApp folder is on your desktop, input: 
	$ cd Desktop/FlaskApp
3. Run the app.py file, input:
	$ python app.py
4. Terminal should output something similar to:
	* Running on http://127.0.0.1:5000/ 
5. Open your desired web browser, and go to that specified local host.
6. Upload and read comics!



User Interaction:

One of my principal aims in creating this project was to make user interaction as simple as possible. Since uploading and reading comics is a simple idea, I thought that it should be just as simple for users to actually do just that. The home page simply directs the user to the Sign Up page, where they can create a profile. Then, the Sign In page allows the user to log in and access the repository. The user’s Dashboard contains all of the comics that have been uploaded by all users, except for the comics that users have makes as ‘private’. The dashboard displays a preview of the comics, and allows the user to like comics as well as read them by clicking the Thumbs Up icon. Next, My List is the user’s home page, where they can see all of the comics that they have uploaded, edit them, and delete them. Add Item allows the user to upload a comic to the repository. Here, they can specify a the comic’s title and any description about the comic they desire (issue number, year published, writers, artists, etc.). To upload a comic, click the ‘Browse’ button and navigate to the file you wish to upload and click ‘Choose’. A preview of the comic should appear in the box to the right. Then, the user can mark the comic as ‘private’, meaning only they will be able to see the comic once it has been uploaded. Finally, the user can mark the upload as already ‘Done’, signifying that they have already uploaded this comic, and are attempting to upload a newer version. (Note: this will not replace the old version, it will create a new instance in the database. The new and old version will be differentiated by the ‘Done’ mark, as well as the date and time that each was uploaded). Finally, the user can hit the ‘Publish’ button to actually upload the comic to the repository. The last of the header tabs is Logout, which allows a user to log out of the repository, sending them back to the website’s home page. 



Lessons Learned:

The purpose of this project was first, to create a website where people can share and read comics, and second, to expose myself new languages and technologies, and force myself to learn them. I believe I successfully accomplished both of those tasks, even though was a very difficult process to get there. I started this project with a little experience in HTML and CSS, but no knowledge of Python, Flask, JavaScript, or jQuery. Due to my lack of knowledge, a large portion of the time spent on this project, was simply learning these various languages, how to implement them, and how they interact with one another. After a few spots of trouble, however, I managed to learn enough to utilize them for the comic repository.

The first problem I ran into was with my UML model for the project. I had originally planned to have the user be able to specify the comic’s publisher, the publisher’s address, artists, writers, year published, among many other fields. I even had an option to differentiate between comic books and graphic novels. But, I realized that users would most likely not know all of this information about about the comic, and even if they did, they might not want to spend the time putting all that information into the repository’s database. So, as a solution, I simplified all of that information into a ‘description’ box, where the user can put in as much or as little information about the comic as they desire. This solution also does not limit the user to the fields that I, the architect of the database, have specified. For instance, the user could put in a plot summary, or the comic’s main characters, which are fields that I did not initially account for. This solution also simplifies the user experience as a whole, as well as the layout of the website.

The second problem I ran into was time constraint. Given the compressed time of a summer semester, I did not have enough time to host the app on a site such as Heroku. Therefore I was left with the repository remaining local to the computer that is running it. 

This change from hosted to local also presented a new problem, as I was forced to deal with the storage of the comics that are uploaded. Originally, I had intended to use an imgbb, a free image hosting site, to store the comics that the users have uploaded. But, due to app being local, as well as the time constraints, I could not accomplish this task. My solution was to create a subfolder in the static folder named Uploads, where I would store copies of the comics that users have uploaded. 

One problem, which was more of an annoyance than a problem, was the naming of the various procedures, functions, and tables in MySQL Workbench. The tutorial I used to help create the flask app was an app where users could create a bucket list for themselves. I modified this app to suit my needs for the comic book repository. However, all of those procedures, functions, and tables were named various things based on the concept of a bucket list. Therefore, I decided that it would be too labor-intensive and time-consuming to rename everything from “wishes” to “comics”. This is the reason that I have a table named ‘tbl_wishes’ with a ‘wish_id’ and ‘wish_title’, instead of a ‘comic_id’ and ‘comic_title’. 

The final problem I had in implementing this project had to do with a specification for the assignment itself. The assignment requires four tables for the database of the project. Since, however, I only had users and comics, I really only needed two tables for the project. As a partial solution, I implemented a ‘like’ feature to the website. I implemented the feature so that, by reading a comic, the user likes it. However, this only allows me to introduce one more table to my schema, and I still fall short of the four table requirement. 



Future Work:

I plan to continue working on this project, with the eventual goal of having it hosted online with a connection to imgbb. In addition to this long-term goal, a few short term goals I have include implementing a count on the number of likes each comic has. Using this count, I could display the most popular comics to the user, allow users to search comics by popularity in the past week, month, or year, among other possibilities. 



Last Notes:
I had such a fun time working on, and learning from, this project, and it was definitely one of the highlights of my year.
Thanks for a great semester!








