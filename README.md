# MySql_Assignment1


1. Count the number of Salesperson whose name begin with ‘a’/’A’.
   
   select count(*) from salespeople 
   where sname like 'a%';
   
2. Display all the Salesperson whose all orders worth is more than Rs. 2000.

   select sname from salespeople s 
   left join orders o on s.snum=o.snum 
   where o.amt>2000;
   
3. Count the number of Salesperson belonging to Newyork.

   select count(*) from SALESPEOPLE 
   where city='Newyork';
   
4. Display the number of Salespeople belonging to London and belonging to Paris.

   select * from SALESPEOPLE 
   where city='London' or city='Paris';
   
5. Display the number of orders taken by each Salesperson and their date of orders.

   select o.odate,s.sname from orders o 
   left join salespeople s on o.snum=s.snum;
