# JDBC Lesson Notes
[JDBC Handout]https://github.com/gocodeup/handouts/blob/master/content/java-iii/jdbc.md

### This Lesson is split up into two parts.

1. Introduce new syntax
  - Build out Album example with JDBCLecture Class
  - Make sure Database and Tables are migrated
  - Make sure MySQL dependency is in pom.xml
  - Connect to SQL using IntelliJ

2. Implement new syntax with full MVC example
  - Build out Contacts example with full MVC
  - Make sure contacts_db is created and migrate table
  - Create Contact.java Bean
  - Create Contacts interface
  - ContactListDao (Contacts implementation) w/o connection
    - Contacts are added manually in Constructor
  - Refactor DaoFactory to use ContactListDao
    - Test ContactListDao and test the application
    - Add ContactIndexServlet, ContactViewServlet
  - Create MySQLContactsDao w/Connection (contacts are added with seeder file)
  - Add Config class inside Dao directory to protect configurations