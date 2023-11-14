# The context and the problem
The top management of UberParrot Inc. was faced with a problem of employee productivity. In order to increase work efficiency,
they decided to get rid of the existing task tracker and replace it with a newly created 'Awesome Task Exchange System (aTES)'.
The aim of the new tracker (aTES) is to increase employee productivity by an unknown percentage.
A new task allocation system has been introduced to ensure staff development and to force employees to train in different areas.
The assignment system selects an assignee in an innovative intellectual way (random =D ).
In order to increase staff motivation, the management also decided to introduce a corporate accounting system. Employees
are paid according to the number of tasks they complete.

# General requirements
## Task Tracker
1. [ ] Task tracker have to be organized as a separate dashboard which is available for the staff of the company 
   UberParrot Inc.
2. [ ] Authorization to the task tracker can be done by using the general authorization service of UberParrot Inc
   (we have an innovative algorithm based on beak shape).
3. [ ] Task tracker operates only tasks. Projects, sprint and so on are out of scope. Parrots cannot memorize how to
   operate with it.
4. [ ] Any employee can create a task in the task tracker (administrator, developer, manager, worker, etc.). A task has 
   status (done or not), description, assignee (randomly chosen parrot except managers and administrators).
5. [ ] Managers and administrators should have a button to shuffle tasks. Pressing the button should result in the 
   reassignment of any open task to a randomly selected member of staff (except managers and administrators). An 
   employee must start with a reassigned task if they didn't finish a previous task before the shuffle.
    1. [ ] It is possible to assign a task to any existing user in the system (except managers or administrators).
    2. [ ] It is only possible to assign a task by using the shuffle button, no other variants are possible.
    3. [ ] Pressing the Shuffle button causes all open tasks to be shuffled between existing users.
    4. [ ] Pressing the Shuffle button is not limited, i.e. it is possible to press it every second.
    5. [ ] There is no limit to the number of tasks that can be assigned to a single user. So it is possible for a user 
       to have no assigned tasks or any number of assigned tasks.
    6. [ ] Every existing task must be assigned. It is not possible to have a task without an assignee.
6. [ ] Each employee should be able to get a list of assigned tasks
7. [ ] Each employee should be able to mark an assigned task as finished

## Accounting
1. [ ] Accounting is available on a separate dashboard which is available for administrators and accountants
   1. [ ] Regular parrots are also have an access to the accounting. But they can view only their own account state
      (audit log and sum)
   2. [ ] Administrators and accountants have an access to a general statistic on earned money
      (amount of money earned by Top-managers and daily statistic)
2. [ ] Authorization to the accounting should be done by using the general authentication service of UberParrot Inc.
3. [ ] Each employee has an account with an amount of earned money. The account has audit log with full set of records on
   each decreasing and increasing of the sum and detailed description of tasks
4. [ ] Costs:
    - [ ] The cost of tickets must be calculated only once, when the ticket is created (or with a short delay).
        - [ ] Costs do not depend on a worker
        - [ ] Assignment fee formula: rand(-10..-20)$.
        - [ ] Finalisation reward formula: rand(20..40)$.
        - [ ] Assignment fee should be charged to the assigned worker's account when the task is assigned
        - [ ] The completion reward should be added to the worker's balance when the task is completed.
        - [ ] A negative balance should be carried over to the next day. The only way to pay off the debt is to complete
        enough tasks during the day
5. [ ] The Accounting Dashboard should show the amount of money earned by the Top Management to date.
    - [ ] The amount earned by top management can be calculated as (sum(completed task amount) + sum(assigned task fee) * -1).
6. [ ] Required activities at the end of the day:
    - [ ] Calculate the amount of money earned by an employee
    - [ ] Send a report by e-mail
7. [After the payment (at the end of the day) the balance should be zero, the record of the payment should be added to the audit log.
8. [ ] The dashboard should show information by days, not the whole period at once.

# Analytics
1. [ ] Assess to aTes system analytics must be organised as a separate dashboard available only to administrators.
2. [ ] Admins must be able to see the amount of money earned by top management and a list of parrots with a negative balance.
3. [ ] Must be able to see the most expensive task per day, month or period.
    - [ ] The most expensive task is a task with the highest price completed in the period.
    - [ ] An example:
        03.03 - the most expensive task - 28$
        02.03 - the most expensive task - 38$
        01.03 - the most expensive task - 23$
        01 March - 03 March - the most expensive task - 38$

# Additional technical details
1. Real-time updating of information is not included.
2. High load is not expected. Approximate number of users per minute is about 100 parrots.
3. No technology stack restrictions
4. All rights to aTES are owned by UberParrot Inc.
5. Highly requested not to hurt any parrot during the creation of the system.