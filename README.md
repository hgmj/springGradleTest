# An Example of Spring Boot Project with Dependency Injection and Hibernate
## Documents I used:

* http://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/

* http://blog.netgloo.com/2014/10/27/using-mysql-in-spring-boot-via-spring-data-jpa-and-hibernate/

## To run it:

* Download the repo to your laptop.

* Open your terminal and go to the project directory, and run ```./gradlew --daemon bootRun```.

* The application will be started at ```localhost:9000``` with the connect to new Tekuma DB. 

* If you want to query an user with user name of "tekuma". Open your browser and do ```http://localhost:9000/get-by-userName?userName=tekuma```.

* If you want to add an user. Do something like: ```http://localhost:9000/create?userName=testUserName&loginName=testLoginName&loginPwd=testLoginPwd```.
 
## How to monitor DB:

* It is suggested to user MySQL Workbench to connect to out new DB at AWS RDS. Refer to [this article](http://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_ConnectToInstance.html).

* In MySQL Workbench: click ```Setup New Connection```.
    * Hostname=The hostname defined at https://console.aws.amazon.com/rds/home?region=us-east-1#dbinstances:.
    * Port=3306
    * User name and password: Ask Kun Qian :).
    
* Make a query like ```select * from tekumadb.tk_user_t;```.