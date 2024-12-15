# InterviewExperiences
infosys interview questions-Round1 
==================================
==>Collections in java
==>difference between treemap and hashmap in java
==>does null keys allowed in hashmap and treemap
==>spring boot aop
==>how we can handle exceptions
==>what is rest controller
==>what if i dont want to handle exceptions(use throws)
==>finally block
==>stream api to filter even numbers
==>about project
==>how to call one microservice from another microservice


infosys round 2 Interview
===========================
==>How to swap two strings without using third variable
class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Try programiz.pro");
        String s1="Hello"; String s2="World";
        s2=(s1+s2);//HelloWorld
        s1=s2.substring(s1.length());//World
        s2=s2.substring(0,s2.length()-s1.length());
        System.out.println(s1);
        System.out.println(s2);
    }
}

==>What are atomic variables in java
==>can I compile program using jre only-->No,we need jdk for compilation
==>Is JVM platform independent or dependent->JVM is platform dependent,and the byte code is platform independent


JP morgan hackerrank questions
======================================
1)merge overlapping intervals
2)given two arrays,find maximum count of pairs such that a[i]>b[j] such that each element paarticipate only once.

JP morgan round1
============================================
1)Given some code,asked to review it for any improvements or bugs.
2)Minimum partition problem.

Given the space currently used on each partition of an existing drive and the total capacity of each partition, determine the minimum number of partitions needed to hold all the data. There are two arrays given as inputs, used and totalCapacity. The first array represents the space used in each partition, and the second represents the total capacity of each partition.

Return the minimum number of partitions required to accommodate all the data without exceeding any partition's total capacity.

Example

used [3, 2, 1, 3, 1] totalCapacity = [3, 5, 3, 5, 5]

The data can be moved around like so:

Move all the data (3 units of space) from the first partition to the second. This empties the first partition, and fills the carond nartition.


JP Morgan Round 2
========================================
System design round.(url shortner problem)

JP Morgan round 3
============================
Behavioural questions and project related questions.


Deloitte interview questions Round1
=====================================
General project related questions(project architecture,aws services used,teams involved,how testing is performed)

Deloitte interview questions Round2
========================================
Java questions

1)given this code,how many test cases needed for 100% code covearge
 if(cond1 && cond2)
{
}
else 
{
}

2)what are lambda expressions and how do you write it.Given a funbctional interface and asked to write lambda expressions. 
interface Test
{
    int addValue(int num1,int num2);
}
    Test t=(num1,num2)->num1+num2;
    t.addValue(3,5);

3)Multithreading in java and executor framework.Given 5 api calls taking some time how do you increase performance by multi threading.
  
   ExcecutorService  service=Executors.newFixedthreadPool(5);
Runnable r=()->{};

      for(int i=1;i<=5;i++)
{
        service.execute(r);
}

4)Enums in java and asked to crate wekeekend enum with saturday as 6 and sunday as 7 values.I wekenend name is given then need to return week number and vice versa.
Why did you use private constructors and in which scenario we need to use private constructors.
    public enum Weekend

{ 
    SATURDAY(6),
    SUNDAY(7),

    private int weekNumber;

   public int getWeekNumber()
{
   return this.weekNumber;
} 

  private Weekend(int weekNumber)
{
   this.weekNumber=weekNumber;
}

}


5)Spring boot questions
==>In how many ways we can create spring beans in java.
==>spring boot profiles
=>Have you worked on data jpa or jdbc ,why do we use them.

6)Aws questions
==>what is dynamodb gsi,lsi,primary key and seconday key,dnamodb streams
==>s3  versioning,can we create events using s3,how to retrive a file if we delete it.
==>what is task in ECS and what is service in ecs
==>Different IAM policies.
==>difference between scan and query in dynamodb.

NCR Voyix interview questions
==================================


1)java questions
==========================
==>About Project.
==>What is serialization in java and why we need to serialize.
==>Multithreading in java->Thread Life Cycle
==>Write a program to demonstrate deadlock situation in multi threading
==>Semaphores
==>Write a program to remove alternate duplicates from a String.
import java.util.*;
class Main {
    public static void main(String[] args) {
        System.out.println("Try programiz.pro");
        String s="this is a program testi";
        
        Map<Character,Integer> map=new HashMap<Character,Integer>();
        
        StringBuilder sb=new StringBuilder();
        
        for(int i=0;i<s.length();i++)
        {
            char c=s.charAt(i);
            map.put(c,map.getOrDefault(c,0)+1);
            if(c==' ' || map.get(c)%2!=0)
            {
                sb.append(c);
            }
        }
        System.out.println(sb.toString());
        
    }

output:this  a progm esti

==>Implement factory design pattern and what problem does factory design pattern solve.

==>difference between hashmap and hashset

==>ConcurrentHashMap

==>Binary trees

==>Failsafe and failfast iterators in java

==>In which situations we need to use arraylist,linkedlist,map

==>What is Time Complexity and timecomplexity of ArrayList,HashMap,LinkedList

2)Spring boot questions
===============================
==>how we can create objects in spring boot
==>what is @Autowired
==>what annotations do you know in spring boot

3)java script and mongodb questions
==>promises in java script
==>how mongodb stores and retrieves data 
==>Transaction management in mongodb
==>Is your angular project built using modular system.



NCR Voyix Round 2
========================
==>Mostly asked on javascript
==>Project architecture,where have you used microservices
==>Http methods and status codes
==>What is hoisting and why hoisting doesnt work for arrow functions
==>function add(n)
{
setTimeout(()=>{console.log(n+250)},0);
}
console.log("before additon");
add(50);
console.log("after addition");

After executing the above code I am getting respose as below
before addition
after addition
300

But he asked me to modify the code so that the output looks like below
before addition
300
after addition

==>memorization:Instead of recomputing for same input it will get the value from cache,asked a program to implement it.
program:
function add(n)
{
 let map=new Map();
  if(map.has(n))
{
  console.log("cache hit");
  return map.get(n);
}
console.log("cache miss");
let result=n+250;
map.set(n,result);
return result;
  
}
add(50);

===>Write a function getCart that accepts orderId and return a promise,promise should print  cart object if orderid is not empty and it should print empty if empty string is given
code:
function getCart(orderId)
{
   return new Promise((resolve,reject)=>{

     if(orderId.trim()=="")
{
  resolve({pid:101,pname:'mobile',category:'electronics'});
}
else
{
 reject("order is empty");
}
}

}

getCart(101).then((product)=>console.log(product)).catch((error)=>console.log(err));
getCart("").then((product)=>console.log(product)).catch((error)=>console.log(err));

==>Program for selection sort

Oracle interview Round 1
======================
==>what is service discovery in microservice
==>StringBuffer and StringBuilder
==>Spring MVC vs Spring boot MVC
==>cron jobs and spring boot scheduling
==>Functional Interfaces in java
==>Given a sorted array,find the first occurance and last occurance of given number.
class Main {
    public static void main(String[] args) {
        System.out.println("Try programiz.pro");
        int[] arr={5,5,5,5,5};
        int n=5;
       System.out.println("First Occurence:"+findFirstOccurence(arr,n));
       System.out.println("Last occurence:"+findLastOccurence(arr,n));
        
    }
    
    public static int findFirstOccurence(int[] arr,int n)
    {
        int fo=-1;
        
        int start=0;
        int end=arr.length-1;
        
        while(start<=end)
        {
            int mid=(start+end)/2;
            if(arr[mid]<n)
            {
                start=mid+1;
            }
            else if(arr[mid]>n)
            {
               end=mid-1;
            }
            else
            {
                fo=mid;
                end=mid-1;
            }
        }
        return fo;
        
    }
    
    public static int findLastOccurence(int[] arr,int n)
    {
        int lo=-1;
        int start=0;
        int end=arr.length-1;
        while(start<=end)
        {
            int mid=(start+end)/2;
            if(arr[mid]>n)
            {
                end=mid-1;
            }
            else if(arr[mid]<n)
            {
                start=mid+1;
            }
            else
            {
                lo=mid;
                start=mid+1;
            }
        }
        return lo;
    }


EPAM interview questions
==================================
Round 1:Completely focused on java
==================================
1)why java does not support multiple inheritance through classes
2)Output of below code
class A
{
    public static void m1()
    {
        System.out.println("A m1()");
    }
    
}

class B extends A
{
    public static void m1()
    {
        System.out.println("B m1()");
    }
}
class Main {
    public static void main(String[] args) {
        System.out.println("Try programiz.pro");
        A a=new B();
        a.m1();
       B b=new B();
       b.m1();
    }
}
output:
A m1()
B m1()
because static methods cannot be overriden,it is called method hiding,read more about it on chatgpt

3)output
class A
{
    public   void m1()
    {
        System.out.println("A m1()");
    }
    
}

class B extends A
{
    protected  void m1()
    {
        System.out.println("B m1()");
    }
}

answer:It will give compilation error because we cannot restrict subclass much further
private>default>protected>public
ex:if superclass has protected then subclass can have either protected or public but not private or default
        
4)Output of below code
class Main {
    
    static int calculate()
    {
        try
        {
            int a=5/0;
            return a;
        }
        catch(Exception e)
        {
            System.out.println("in catch block");
            return 20;
        }
        finally
        {
            System.out.println("In finally");
            return 30;
        }
    }
    
    public static void main(String[] args) {
       System.out.println(calculate());
    }
}

output:
in catch block
In finally
30


5)use of default methods in interfaces from java8
6)How implementation of hashmap changed from java8
7)can we use external variables like local variables and instance variable or static variables in lambda expressions in java,if so what are conditions
8)can we use intermediate operations in java streams without using terminal operations.
9)ArrayList Vs LinkedList,which is ideal for retieving and addition or deletion operations
10)How TreeSet stores data if we are adding custom objects
11)Failfast and Fail safe iterators,hashmap iterator is failfast or failsafe,what happens if we add any new element during iteration of hashmap and what is alternate for it.
12)How to start thread in java,what happens if we directly call run method.Can we call start method twice(No, a thread can only be started once,if we call twice it will throw Exception)
13)Method references in java
14)suppose if we want a thread to return some value after processing,how will you do it in java.
15)Program to find intersection of two LinkedLists.
16)Given list of employees,there is a field called email,find occurence of each domain like gmail.com,tcs.com,yahoo.com etc.....
import java.util.*;
import java.util.stream.*;
class Employee
{
    private String mail;
    
   Employee(String mail)
   {
       this.mail=mail;
   }
   public String getMail()
   {
       return this.mail;
   }
   
}
class Main {
    public static void main(String[] args) {
       List<Employee> empList=Arrays.asList(new Employee("arun@gmail.com"),new Employee("tanakam@gmail.com"),new Employee("arun@tcs.com"),new Employee("kumar@yahoo.com"));
       
      Map<String,Long> map=empList.stream().map(emp->emp.getMail()).collect(Collectors.groupingBy(s->s.substring(s.indexOf("@")+1),Collectors.counting()));
      map.forEach((key,value)->System.out.println(key+":"+value));
    }
}

UST Global Interview questions
================================
1)Given a list of transactions,find the total amount for each type of transaction

transList.stream().collect(Collectors.groupingBy(trans->trans.getType(),Collectors.summingInt(tarns->trans.getAmount()))).forEach((key,value)->System.out.println(key+":"+value));

2)difference between final and finally

3)difference between jpa and orm

4)About api security using jwt and oauth

5)difference between when and having in sql

6)how to unit test private methods in java.

7)Disadvantages of microservices 

8)How to trigger aws lambda 

9)Spring boot  stereotype annotations  

10)various design patterns in spring boot.

11)difference between @Primary and @Qualifier.

Cognizant interview questions
=============================
1)Circuit breaker pattern in microservices

2)Api gateway in microservices

3)Monolith vs microservices and advantages of microservices

4)Transient keyword in java

5)internal working of hashmap,what is collision and how to resolve collision.

6)different functional interfaces in java

7)why string is immutable in java

8)difference b/w jpa and hibernate

9)stereotypes annotations in spring boot

10)Spring boot profiles

11)Restcontoller vs controller

12)Excpetion handling in java and spring boot

13)@SprinBootApplication annotation

14)what happens if we dont keep @Repository annotation.

15)Spring boot actuators and how to design custom actuators.

16)How to do dependeny injection in springboot and Different types of dependency injection in spring boot,advantages and disadvantages of constructor injection.

17)Design an api which accept excel sheet,read excel sheet and covert into pojo object and store it in database.

18)given an integer array,sort it and remove duplicates and find second highest element using stream operations

Integer[] a={3,2,1,7,2,8,9,3,4,6,1}

List<Integer> list=Arrays.Stream(a).distinct().sorted().collect(Collectors.toList()); 

System.out.println(list);
System.out.println(list.get(list.size()-2));

Barraiser interview for thoughtworks
================================================ 
1)How java handles Memory.
2)Use of final,static,volatile keywords. 
3)How stream api works internally.
4)Where have you used stream api in your project.
5)In your project have you faced any memory issues and how have you resolved it.
6)How spring boot manages configuration using application.properties
7)How to handle configuration for differnent environments in spring boot(Spring boor profiles).
8)How to enable cross browser compatability in ui apps.
9)How to reuce load time of single page apps
10)How can we manage state in react
11)How to develop reusable components in react
12)How to write uint test cases effectively
13)What will you do if any unit test case fails in jenkins.
14)Use of constructors and setter methods and when to use both.
15)Design employee class having fields like name,title,salary and company class with two methods one is for adding employees and another one is for calculating total cost to company.

class Employee
{
private String name;
private String title;
private double salary;

//setters and getters 

}

class Company
{
   List<Employee> empList;
   double total=0.0;
   Company()
{
   empList=new ArrayList<>();
}

public void addEmployee(Employee e)
{
   emplist.add(e);
   total+=e.getSalary();
}

public double calculate()
{
   return salary;
}
 
}




