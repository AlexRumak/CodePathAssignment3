# CodePathWeek4
Web Security Assignment 3
Cross Site Forgery Protection and penetration testing.

Submitted by: Alexander Rumak

Time spent: 6 hours spent in total

##Login Page Vulnerabilities:
Initially the implementation for the login page called for a different error if the login failed due to an incorrect password or an incorrect username. This violates the priniciple of security through obscurity, as a hacker could build a list of active usernames from the error messages. I corrected this issue in my implementation by displaying the same error for a login failure, regardless of the cause.

Two other potential faults that could arise are the following:
* First, the connection given to users to the mysql database during transactions is that of the root user. This gives a hacker the potential priveledges of the root user. The connection should be altered to be weaker than a root user.
* Second, and more obvious, is that a master password is used for login. But, this is a given, and to correct this will likely be covered in the future.

##Bugs Encountered:
I encountered some bugs in the penetration testing files for this project. This is reflected in the user-story. The page for the SQL injection test and the page for the CSRF test refresh their content endlessly, unless manually cancelled. The results of the tests can be seen in the user story very briefly, however. Once the page refresh is manually cancelled and the test is run, the results show that the tests failed to penetrate my system for a very brief moment (after which, the page begins to refresh like mad again...).

##User Stories Implemented:

The following required functionality is complete:

* [\*] Test for vulnerabilities.
* [\*] Configure Sessions.
* [\*] Login Page.
* [\*] Require login to access staff area pages.
* [\*] Logout Page.
* [\*] Add CSRF protections to state form.
* [\*] Ensure the application is not vulnerable to XSS attacks.
* [\*] Ensure the application is not vulnterable to SQL injection attacks.
* [\*] Run all tests from Objective 1 again and confirm that your application is no longer vulnerable to any test.

The following optional features are implemented:

* [\*] Bonus Objective 1
* [ ] Bonus Objective 2
* [\*] Bonus Objective 3
* [ ] Bonus Objective 4
* [ ] Advanced Objective: Create cookie encryption


##User Story walkthrough:
<img src='https://github.com/AlexanderRumak/CodePathAssignment3/blob/master/user_stories/assignment03_1.gif' title='Video Walkthrough' width='' alt='Video Walkthrough' />
[https://github.com/AlexanderRumak/CodePathAssignment3/blob/master/user_stories/assignment03_1.gif]
