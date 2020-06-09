# CTFLearn-Basic Injection

Today we are going to work upon one of the most basic and also the most primarily taught topic in ethical hacking. We are going to work with SQL injection.

## What is SQL injection?
* SQL injection is a code injection technique that might destroy your database. It is one of the most common web hacking technique. We basically introduce a malicious SQL input onto a web page input.

### Statement:

* [Link to the problem](https://web.ctflearn.com/web4/)

![sql,sqli,sql injection,CTFlearn,easy](https://raw.githubusercontent.com/SecOnset/SeconsetFile/master/writeups_pratyaksh/CTFLearn/CTFLearn%20SS/SQLi.png)

***
So, let us visit the link to the problem, once we land onto the problem page, we are given a web page input field.

![hacking problems, problems, sqli, sql injection](https://github.com/SecOnset/SeconsetFile/blob/master/writeups_pratyaksh/CTFLearn/CTFLearn%20SS/SQLiproblem1.png)

***
Okay, so looking at this the most common way, I can think of to get started is either visiting the source page or using the inspect element. SO, let us dive into it. You can visit the source page by either right clicking and selecting "view page source" or directly press "ctrl+u".

![source page, sqli](https://github.com/SecOnset/SeconsetFile/blob/master/writeups_pratyaksh/CTFLearn/CTFLearn%20SS/sourceSQLi.png)

Hmm, interesting stuff. Let us try inputing those names.
***
![ctflearn](https://github.com/SecOnset/SeconsetFile/blob/master/writeups_pratyaksh/CTFLearn/CTFLearn%20SS/sqliluke.png)

* For the first two names(Hiroki and Noah) we are prompted with absolutely nothing but, once we enter the name "Luke", we are given an output, with the name and data as,"Data: I made this problem.".

At this point we should realise that this input field is connected with a database. So, now we can start experimenting the most basic SQL injection payload, i.e. 'OR '1'='1

What the above payload basically represents is a simple SQL statement, i.e, `SELECT password FROM table_name WHERE name ='' OR '1'='1`

By adding the **OR** keyword and **`'1'='1`**, we are basically adding a simple OR statement here that will return us TRUE even if any one of the condition is true. So, in the statement, `SELECT password FROM table_name WHERE name ='' OR '1'='1`
, if the input value even if it is false, but the '1'='1' is always true. So, we are returned with all the values in the particular table of the database.

![sqli](https://github.com/SecOnset/SeconsetFile/blob/master/writeups_pratyaksh/CTFLearn/CTFLearn%20SS/sqlianswer.png)

We are now retrieved with a flag here that is, FLAG:***th4t_is_why_you_n33d_to_sanitiz3_inputs***. 





