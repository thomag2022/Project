# Web Application Data Entry

## Video Demo: [Final Project Video](https://www.youtube.com/watch?v=rsmm31qCk8w "Final Project Video")

## Description

The project is a web application where users can enter and save information about topics they have learned about. The reason for developing this application is to develop a better understanding of python while implementing methods such piping from database to client, role based authentications, etc.

Technologies used:

- Python
- Javascript
- HTML
- Django
- Django-bootstrap4
- sqlite3 with Heroku

## How the webpage works?

The program is relatively straight forward. The user can register a username and password to gain access. During registration a user will need to enter the following fields:

- Username
- Password (Cannot be similar to other personal info, must contain at least 8 characters, cannot be a commonly used password, cannot be entirely numeric)
- Password Confirmation
- After input user will click the Register button

Once a user has registered, they will gain access to the topics log where entries may be added.

- **Topics Page: This page becomes available once a user registers**
  - Clickable Topics will be present when/if any are created
  - "Add a new topic" link for creating new topics can be accessed
- **Entry: Description about the topic that was learned about is accessible.**
  - After clicking on a "Topic", entries are shown
  - Located below the topic and above the entries is an "Add new entry" link
  - For each entry, a date and time will be shown for when they were created
  - Each entry has an "edit entry" link for updates or changes

### Directing Path

For every path the user is checked for authentication. In short this refers to as the user's username and password given is correct and what privileges are granted. An example would be a user is only aloud to see and edit their own topics and entries. If an admin is authenticated then this user will have the ability to see and edit topics along with entries for every user.

### Database

The database is the location where all topics, entries, and users are stored. The database is supported by an embedded database called SQLite engine used by Heroku.

## Potential Refinements

Like most applications, this applications presents room for improvements.

**Possible improvements:**

- Enhance the user's experience when interacting with the web application.
- Provide the ability to upload images and videos for each topic.
- Increase what information is requested from a user when they register.
- Add a profile page for users that showcase what topics and information they are interested in.
- Implement more than two buttons at the top of the page for improved navigation
- Add better security measures while users interact with application

## How to launch application

1. Confirm that django is installed
   * In the terminal create a new directory called learning_log
   * Switch to directory in terminal
   * Then type python -m venv ll_env
   * In Windows terminal enter ll_env\Scripts\activate
   * After activating virtual environment enter pip install django
   * Once django is install the output should say Successfully installed django-2.x.x pytz-xxx.x sqlparse-0.x.x
2. Clone the code: `git clone https://github.com/thomag2022/Project`
3. Once installed run the command `python manage.py runserver`
4. In your browser go to `localhost:8000`
5. The application should now be available and thank you for viewing!
