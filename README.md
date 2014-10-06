sql-email-recent-job-failures
=============================

Will email the most recent SQL Job failures to a list of recipients. Tested in MS SQL 2005.

It's pretty simple,
1. Create the Stored Proceedure using the SQL in file ``create_sp_Email_Recent_Job_Failures``
1. Execute the SP and be sure to pass in your semicolon (;) delimited list of email recepients.
1. You can optionaly pass in the number of days back to look for failed jobs.

```SQL
  EXEC dbo.sp_Email_Recent_Job_Failures @to='me@mysite.com;you@yoursite.com' [, @NumberDaysBack = SMALLINT]
```
