# notes

## hackerrank
_________________________________________________________________________________________________________________________________________________________________________________
NumberFormat use .getCurrencyInstance(Local.US) and not 
                 .getNumberInstance(Local.US) if want to display currency in format with symbol like$.<br/>

<br/>
Calendar cal = Calendar.getInstance();<br/>
        cal.set(month, day, year);<br/>
        int ans = cal.get(Calendar.DAY_OF_WEEK);<br/>
_________________________________________________________________________________________________________________________________________________________________________________
<br/>
To format date and time:<br/>
DateTimeFormatter myFormatObj = DateTimeFormatter.ofPattern("dd/MM/yyyy HH:mm:ss");
String formattedDate = myDateObj.format(myFormatObj);<br/> 
_________________________________________________________________________________________________________________________________________________________________________________
<br/>
`substring`<br/>
substring (start,end) - output: start,end-1
substr = str.substring(7, 17);<br/>
_________________________________________________________________________________________________________________________________________________________________________________
<br/>
pls remember even if the values are same then too stringbuffer are not equal.
_________________________________________________________________________________________________________________________________________________________________________________
<br/>
https://docs.spring.io/spring-boot/docs/current/api/org/springframework/boot/test/autoconfigure/web/servlet/WebMvcTest.html
https://www.javatpoint.com/spring-boot-actuator
_________________________________________________________________________________________________________________________________________________________________________________
<br/>
`stereotype annotations`<br/>
The Spring Framework provides you with some special annotations. These annotations are used to create Spring beans automatically
in the application context.<br/> 
The main stereotype annotation is @Component.
There are some Stereotype meta-annotations which is derived from @Component those are
**@Service**: Used to create Spring beans at the Service layer,
**@Repository**: Which is used to create Spring beans for the repositories at the DAO layer, and
**@Controller**: Which is used to create Spring beans at the controller layer.<br/>
https://docs.spring.io/spring-framework/docs/3.0.0.M3/reference/html/ch04s04.html<br/>
_________________________________________________________________________________________________________________________________________________________________________________
<br/>
`REST` (Representational State Transfer)<br/>
https://teletype.in/@andrewgolovko/lazy-and-eager-instantiation - 
Singleton Beans are eagerly instantiated
Prototype Beans are lazily instantiated by default however, if Singleton Bean has a dependency on Prototype Bean, 
then Prototype Bean Instance will be created eagerly to satisfy dependencies for Singleton Bean<br/>
_________________________________________________________________________________________________________________________________________________________________________________
<br/>
@PropertySource("classpath:/com/${my.placeholder:default/path}/app.properties")
Advice is associated with point-cuts.
Advice contains certain task that is to be performed when a point-cut is found. 
It defines the crosscutting behavior at join points - Types: after, before, around<br/>
_________________________________________________________________________________________________________________________________________________________________________________
<br/>
`AOP`<br/>
for AOP - https://mossgreen.github.io/Spring-Certification-Spring-AOP/
Aspect-Oriented Programming (AOP) complements Object-Oriented Programming (OOP) by providing another way of thinking about program structure. The key unit of modularity in OOP is the class, whereas in AOP the unit of modularity is the aspect. Aspects enable the modularization of concerns such as transaction management that cut across multiple types and objects. (Such concerns are often termed crosscutting concerns in AOP literature.)<br/>
Spring uses proxy objects to implement the method invocation interception part of AOP. 
Such proxy objects wrap the original Spring bean and intercepts method invocations as 
specified by the set of pointcuts defined by the cross cutting concern.<br/>
_________________________________________________________________________________________________________________________________________________________________________________
Following are various methods of Object class −

- protected Object clone() - Used to create and return a copy of this object. <br />
- boolean equals(Object obj) - Used to indicate whether some other object is "equal to" this one. <br />
- protected void finalize() - garbage collector calls this method on an object when it determines that there are no more references to the object. <br />
- Class<?> getClass() - Used to get the runtime class of this Object. <br />
- int hashCode() - Used to get a hash code value for the object. <br />
- void notify() - Used to wake up a single thread that is waiting on this object's monitor. <br />
- void notifyAll() - Used to wake up all threads that are waiting on this object's monitor. <br />
- String toString() - Used to get a string representation of the object. <br />
- void wait() - marks the current thread to wait until another thread invokes the notify() method or the notifyAll() method for this object. <br />
- void wait(long timeout) - marks the current thread to wait until either another thread invokes the notify() method or the notifyAll()<br />
                          method for this object, or a specified amount of time has elapsed. <br />
- void wait(long timeout, int nanos) - marks the current thread to wait until another thread invokes the notify() method or the notifyAll() method for this object, <br />
                                     or some other thread interrupts the current thread, or a certain amount of real time has elapsed. <br />
_________________________________________________________________________________________________________________________________________________________________________________
<br/>
`Regular Expression`<br/>
- ^	The beginning of a line. <br/>
- $	The end of a line. <br/>
- \b	A word boundary (where a word starts or ends, e.g. space, tab etc.) <br />
- \B	A non-word boundary. <br/>
- \A	The beginning of the input. <br/>
- \G	The end of the previous match <br/>
- \Z	The end of the input but for the final terminator (if any). <br/>
_________________________________________________________________________________________________________________________________________________________________________________
https://www.buggybread.com/2014/09/java-interview-questions-and-answers-on_59.html
_________________________________________________________________________________________________________________________________________________________________________________
<br/>
`Big Decimal`<br/>
The BigDecimal class provides operations on double numbers for arithmetic, scale handling, rounding, comparison, format conversion and hashing.
It can handle very large and very small floating point numbers with great precision but compensating with the time complexity a bit.
A BigDecimal consists of a random precision integer unscaled value and a 32-bit integer scale. 
If greater than or equal to zero, the scale is the number of digits to the right of the decimal point. If less than zero, 
the unscaled value of the number is multiplied by 10^(-scale).<br/>
_________________________________________________________________________________________________________________________________________________________________________________
<br/>
`Big Integer`<br/>
certainty factor - 1,0,-1
isProbablePrime(int certainty) method is used to tell if this BigInteger is probably prime or if it’s definitely composite.
This method checks for prime or composite upon the current BigInteger by which this method is called and returns a boolean value.
It returns true if this BigInteger is probably prime, false if it’s definitely composite. 
If certainty is <= 0, true is returned.
/*  obj.add(obj)
    obj.multiply(obj) methods of BigInteger */<br/>
_________________________________________________________________________________________________________________________________________________________________________________
<br/>
`instanceof`<br/>
The java instanceof operator is used to test whether the object is an instance of the specified type (class or subclass or interface).
The instanceof in java is also known as type comparison operator because it compares the instance with type. 
It returns either true or false.<br/>
_________________________________________________________________________________________________________________________________________________________________________________
<br/>
`JAVA reflection`<br/> 
It is a very powerful tool to inspect the attributes of a class in runtime.
For example, we can retrieve the list of public fields of a class using getDeclaredMethods().<br/>
_________________________________________________________________________________________________________________________________________________________________________________
<br/>
`Comaprable Sort` Refer this example to see how compareto method is override and used to compare elements of 
List<Student>.<br/>
_________________________________________________________________________________________________________________________________________________________________________________
`object.cardinality` Method in Bitset class which returns Returns the number of bits set to true in this BitSet.<br/>
_________________________________________________________________________________________________________________________________________________________________________________
<br/>
`Java annotation`<br/> 
It is used to define the metadata of a Java class or class element. We can use Java annotation at the compile time to instruct the compiler about the build process. 
Annotation is also used at runtime to get insight into the properties of class elements.<br/>
_________________________________________________________________________________________________________________________________________________________________________________
<br/>
`Covariant Return Types`<br/>
Java allows for Covariant Return Types, which means you can vary your return type as long you are returning a subclass of your specified return type.<br/>
_________________________________________________________________________________________________________________________________________________________________________________
<br/>
`Varargs`<br/> 
The three dots (...) are used in a function’s declaration as a parameter.
These dots allow zero to multiple arguments to be passed when the function is called. The three dots are also known as var args.<br/>
_________________________________________________________________________________________________________________________________________________________________________________
<br/>
The heap is created when the JVM starts up and may increase or decrease in size while the application runs.<br/>
_________________________________________________________________________________________________________________________________________________________________________________
<br/>
Static variable gets memory only once in the class area at the time of class loading. Using a static variable makes your program more memory efficient 
(it saves memory).
Static variable belongs to the class rather than the object.<br/>
_________________________________________________________________________________________________________________________________________________________________________________
<br/>
Connecting a method call to the method body is known as binding.
In case of the static binding, the type of the object is determined at compile-time whereas, in the dynamic binding, the type of the object is determined 
at runtime.<br/>
_________________________________________________________________________________________________________________________________________________________________________________
<br/>
`Concurrent HashMap<>`<br/>
In ConcurrentHashMap, at a time any number of threads can perform retrieval operation but for updated in the object, the thread must lock the 
particular segment in which the thread wants to operate. This type of locking mechanism is known as **Segment locking or bucket locking**. 
Hence at a time, 16 update operations can be performed by threads.
Inserting null objects is not possible in ConcurrentHashMap as a key or value.<br/>
_________________________________________________________________________________________________________________________________________________________________________________
