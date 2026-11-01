# Apply-more-filters-in-SQL

## Overview - Querrying numbers and dates using operators as filter

### Task 1. Retrieve login attempts after 2022-05-09
SELECT *
FROM log_in_attempts
WHERE login_date > '2022-05-09'
<img width="431" height="97" alt="task 1" src="https://github.com/user-attachments/assets/927c0dbe-0257-42d0-9696-21ee8a06b242" />


### Task 1b. Expanding the date range to include 2022-05-09 from the previous querry
SELECT *
FROM log_in_attempts
WHERE login_date >= '2022-05-09';
<img width="436" height="117" alt="task 1b" src="https://github.com/user-attachments/assets/591eb9f3-737d-4150-b6ae-b4314ea2a3bf" />


### Task 2. Retrieve logins in a date range, narrowing the focus of the search to exclude login attempts made after 2022-05-11
SELECT *
FROM log_in_attempts
WHERE login_date BETWEEN '2022-05-09' AND '2022-05-22';
<img width="431" height="101" alt="task 2" src="https://github.com/user-attachments/assets/793599c3-e2b7-4244-afe7-c570ee86a946" />


### Task 3. Investigate logins at certain times - in this task, i will be investigating logins that were made before '07:00:00'.
SELECT *
FROM  log_in_attempts
WHERE login_date < '07:00:00';
<img width="432" height="108" alt="task 3" src="https://github.com/user-attachments/assets/030a9f0f-7105-4604-833c-b1e71ac5912d" />

### Task 3b Modifying the previous query to return logins between '06:00:00' and '07:00:00'.
SELECT *
FROM log_in_attempts
WHERE login_time BETWEEN '06:00:00' AND '07:00:00'
ORDER BY login_time;
<img width="438" height="144" alt="task 3b" src="https://github.com/user-attachments/assets/9a13cf8e-cdad-4637-85e7-95faf2c00b55" />


### Task 4. Investigate logins by event ID - investigate login attempts based on event ID numbers
SELECT event_id, username, login_date
FROM log_in_attempts
WHERE event_id >= 100;
<img width="431" height="91" alt="task 4" src="https://github.com/user-attachments/assets/c6def029-d759-4d5e-a1f6-2dc23c179596" />

### Task 4b Modifying the previous return to reduce the search between 100 and 150
SELECT event_id, username, login_date
FROM log_in_attempts
WHERE event_id BETWEEN 100 AND 150;
<img width="420" height="77" alt="task 4b" src="https://github.com/user-attachments/assets/dae35b86-9360-4a57-a5d4-42c25f30dfdf" />

