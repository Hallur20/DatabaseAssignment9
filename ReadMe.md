<h1>Assignment 9 Database</h1>

<h4>1: Rewrite the query down below as an expression in relational algebra</h4>

```sql
select customers.customerName, offices.city as office_city
from customers, employees, offices
where 
	customers.salesRepEmployeeNumber = employees.employeeNumber and 
	employees.officeCode = offices.officeCode and
    customers.city = offices.city;
```

<img src="https://latex.codecogs.com/svg.latex?P\;of\!fice\char`_city/o.city(\sigma\;c.salesRepEmployeeNumber=e.employeeNumber(\sigma\;e.of\!ficeCode=o.of\!ficeCode(\sigma\;c.city=o.city(customers\;x\;employees\;x\;of\!fices))))"/>

<h4>2: Add row counts to the subexpressions</h4>

<img src="https://latex.codecogs.com/svg.latex?\Pi\;c.customerName,of\!fice\char`_city(\sigma\;P(\rho\;of\!fice\char`_city/o.city(customers^{122}\;x\;employees^{23}\;x\;of\!fices^{7})^{19642})^{14})"/>

<h4>Rewrite to a better expression</h4>

<img src="https://latex.codecogs.com/svg.latex?where\;P=c.salesRepEmployeeNumber=e.employeeNumber\wedge\;e.of\!ficeCode=o.of\!ficeCode\wedge\;c.city=o.city"/>

<img src="https://latex.codecogs.com/svg.latex?\Pi\;c.customerName,of\!fice\char`_city(\sigma\;P(\rho\;of\!fice\char`_city/o.city(customers\;x\;employees\;x\;of\!fices)))"/>

<img src="https://latex.codecogs.com/svg.latex?\Pi\;c.customerName,of\!fice\char`_city(\sigma\;P(\rho\;of\!fice\char`_city/o.city(customers^{122}\;x\;employees^{23}\;x\;of\!fices^{7})^{19642})^{14})"/>
