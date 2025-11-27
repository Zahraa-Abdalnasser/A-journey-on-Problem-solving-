# SQL Problem solving 
# Using postgreSQL DBMS 
1- [Employees earning more than their managers ](https://leetcode.com/problems/employees-earning-more-than-their-managers/)
- Solution
```
select e.name as Employee
from Employee e join Employee m on (e.managerId = m.id) 
where e.salary > m.salary; 
```
2- [Dublicate Emails](https://leetcode.com/problems/duplicate-emails/description/)
- Solution
```
select Distinct p1.email as Email
from Person p1, Person p2
where (p1.email = p2.email) and (p1.id != p2.id); 
```
3- [Game play Analysis](https://leetcode.com/problems/game-play-analysis-i/description/)
- Solution
```
select player_id , min(event_date) as first_login
from Activity 
group by player_id
```
4- [Customer who never order](https://leetcode.com/problems/customers-who-never-order/description/)
- Solution
```
select name as Customers 
from Customers left join Orders on (Customers.id = Orders.customerId )
where  Orders.customerId  is null ;
```
