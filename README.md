# wrpracti

use wrpracti_bookinfo;
-- write sql query to find salaries of all employees
select * from employees;
select Employee_ID,First_Name,Last_Name,Salary from employees;

-- write sql query to find unique designations of employees and return job name

select * from employees;
select * from jobs;
select distinct job_id,job_title as designations from jobs;



-- write sql query to list the employees'name, increase their salary by 15% and express as number of dollars
select * from employees;
select First_Name,last_name,concat('$',round(salary*1.15,2)) as 'salary in dollars' from employees;

-- assume salary in indian rupees and convert it into dollars and increse by 15%
select First_Name,last_name,(salary*1.15)/76.46 as 'salary in dollars' from employees;

--  write sql query to list the employees'name,and job id as a format of employee & job
select concat(first_name,' ',last_name,' ','&',' ', job_id) as 'employee & job' from employees;
