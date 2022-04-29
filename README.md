![ScreenShot](https://user-images.githubusercontent.com/98576037/164997295-1689bcf2-99a0-4300-9d2b-5c2ae03ac2c2.png)

# **SALARY CALCULATOR**

## **INFORMATION**

* **Salary calculator: It is a system that calculates an employee's salary along with the expenses of money.**

## **TECHNOLOGIES USED**

* **JAVA**

## **CONTENTS**

* **SalaryCalculator** and **Employee** class information has been created.

* The employee's name is specified.

* **Employee class**: Includes employee's first and last name, salary, hours worked, years worked, taxes, bonuses, salary increases, taxes and bonuses, and salary and total salary.

## **CODES**

```Java

        public class Salarycalculator {

            public static void main(String[] args) {

                Employee emp = new Employee("John Smith", 2000, 45, 1985);

                emp.employeeInfo();

            }
        }

```

```Java

        import java.util.Calendar;

        public class Employee {

            String name;

            double salary;

            double workHours;

            int hireYear;

            double tax;

            double bonus;

            double total;

            double increaise;

            double bonusPrice = 0;

            Employee(String name, double salary, int workHours, int hireYear){

                this.name = name;

                this.salary = salary;

                this.workHours = workHours;

                this.hireYear = hireYear;

                this.total = this.salary;

                this.increaise = 0;

                this.bonus = 0;

                this.tax = 0;

            }

            void taxCalculate(){

                if(this.total > 1000.0){

                    this.tax = this.total * 0.03;

                    this.total = (this.total - this.tax);

                    System.out.println("Tax: " + this.tax);

                }else{

                    this.tax = 0;

                    System.out.println("Tax: " + this.tax);

                }
            }

            void bonus(){

                if(workHours > 40){

                    this.bonus = this.workHours - 40;

                    this.bonus *= 30;

                    this.bonusPrice = bonus;

                    System.out.println("Bonus price: " + this.bonusPrice);

                }else{

                    this.bonus = bonus;

                    System.out.println("Bonus price: " + this.bonus);

                }

            }

            void increaiseSalary(){

                this.total = this.salary;

                int now = Calendar.getInstance().get(Calendar.YEAR);

                int time = now - hireYear;

                if(time < 10){

                    this.total *= 0.05;

                    this.increaise += this.total;

                    System.out.println("Salary increase  :" + this.increaise);

                }

                if(time > 9 && time < 19){

                    this.total *= 0.10;

                    this.increaise += this.total;

                    System.out.println("Salary increase  :" + this.increaise);

                }

                if(time > 19){

                    this.total *= 0.15;

                    this.increaise += this.total;

                    System.out.println("Salary increase  :" + this.increaise);

                }
            }

            void employeeInfo(){

                System.out.println("--------------------------------------");

                System.out.println("Employee Name : " + this.name);

                System.out.println("Employee Salary : " + this.salary);

                System.out.println("Employee WorkHour : " + this.workHours);

                System.out.println("Employee Work Start Year  : " + this.hireYear);

                this.taxCalculate();

                this.bonus();

                this.increaiseSalary();

                System.out.println("Salary with tax and bonus : " + (this.salary - this.tax + this.bonus));

                System.out.println("Total salary :" + (this.total + this.salary));

            }
        }


```

```bash

    Employee Name : John Smith
    Employee Salary : 2000.0
    Employee WorkHour : 45.0
    Employee Work Start Year  : 1985
    Tax: 60.0
    Bonus price: 150.0
    Salary increase  :300.0
    Salary with tax and bonus : 2090.0
    Total salary :2300.0

```

<br />

## **LINK**

* Click here https://github.com/Fogo9/SalaryCalculator.git to access the Github page for this project.

<br />

## **LICENSE**

* This software is licensed By Tuncay Demir under the MIT license.

<br />

>[Patika.dev](https://app.patika.dev/fogomurphy)

<br/>

| Name |  Email |
| ---- |  ----- |
| Tuncay | tuncaydemir682@gmail.com |
