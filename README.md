# Project 8 - Pentesting Live Targets

Time spent: **X** hours spent in total

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

Vulnerability #1: SQL Injection

![](https://github.com/hetobias/Week8-WebSecurity/blob/master/blue_sql.gif)
- The blue site had SQLi vulnerability as shown in the gif. By adding ' OR SLEEP(10)=0--' to the end of the URL it will cause the web page to load for 10 seconds.

### Steps to Replicate
1. Access the "Find a Salesperson" tab
2. Click on any person
3. In the URL add ```' OR SLEEP(10)=0--'``` to the end.



Vulnerability #2: Session Hijacking/Fixation

![](https://github.com/hetobias/Week8-WebSecurity/blob/master/blue_sessionhijacking.gif)
- This vulnerability allows us to change session and log in without logging in.

### Steps to Replicate
1. Log into the Green page with Chrome or Firefox. ```https://104.198.208.81/green/public/staff/login.php```
2. Acess this page to obtain the session. ```https://104.198.208.81/green/public/hacktools/change_session_id.php```
3. Open another browser that is not the one used in step 1. And access this ```https://104.198.208.81/blue/public/hacktools/change_session_id.php```
4. Copy and paste the session obtained in step 2 into the Blue page session and change it.
5. Click log in on Blue page and you should automatically be logged in without inputting any user credentials.


## Green

Vulnerability #1: __________________

Vulnerability #2: __________________


## Red

Vulnerability #1: __________________

Vulnerability #2: __________________


## Notes

Describe any challenges encountered while doing the work
