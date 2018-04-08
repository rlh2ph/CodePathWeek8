# Project 8 - Pentesting Live Targets

Time spent: **7** hours spent in total

> Objective: Identify vulnerabilities in three different versions of the Globitek website: blue, green, and red.

The six possible exploits are:
* Username Enumeration
* Insecure Direct Object Reference (IDOR)
* SQL Injection (SQLi)
* Cross-Site Scripting (XSS)
* Cross-Site Request Forgery (CSRF)
* Session Hijacking/Fixation

Each version of the site has been given two of the six vulnerabilities. (In other words, all six of the exploits should be assignable to one of the sites.)

## Blue

Vulnerability #1: SQL Injectiuon (SQLi)
![Alt Text](https://github.com/rlh2ph/CodePathWeek8/blob/master/SQLInjection.gif)
  - The red and green sites allow for commas after a user id, and will redirect to the appropriate page, but the blue page says that the database query failed, which is why we know it is vulnerable to SQL Injections

Vulnerability #2: Session Hijacking/Fixation
![Alt Text](https://github.com/rlh2ph/CodePathWeek8/blob/master/Session.gif)
  - On two different browsers, Firefox and Chrome, we can get two different sessions and change the session on the attacker's session to the admin session. The attacker is now logged in as the admin and has all of the admin privileges.


## Green

Vulnerability #1: Username Enumeration
![Alt Text](https://github.com/rlh2ph/CodePathWeek8/blob/master/UsernameEnumeration.gif)
  - The green site gives a bolded message for log ins that were not successful with valid usernames, but non bold responses for log ins with non existent usernames.

Vulnerability #2: Cross Site Scripting (XSS)
![Alt Text](https://github.com/rlh2ph/CodePathWeek8/blob/master/XSS.gif)
  - The green site allows for scripts to execute when feedback is submited, which is why XSS works


## Red

Vulnerability #1: Insecure Direct Object Reference (IDOR)
![Alt Text](https://github.com/rlh2ph/CodePathWeek8/blob/master/IDOR.gif)
  - The url for the red site allows for the id parameter to be edited to pass in other ids that are not visible sales people

Vulnerability #2: Cross Site Request Forgery (CSRF)
![Alt Text](https://github.com/rlh2ph/CodePathWeek8/blob/master/CSRF.gif)
  - By process of elimination, the red site is vulnerable to CSRF. Also, the site is vulnerable in the way that it allows an attacker to intercept a post request and change the values and then forward the request along.


## Notes

Describe any challenges encountered while doing the work
