# Notes of the Java developer

## Java 8
### Lambda functions
1. Method reference is another way of creating anonymous methods. Basically, what is does is - it creates
   implicit lambda function that invokes the specified method underneath. For example,
   ```java
    Stream.of(1.5, 2.1, 3.2).map(Double::intValue).collect(Collectors.toList());
   ```
   is the shorthand of
   ```java
   Stream.of(1.5, 2.1, 3.2).map(d -> d.intValue()).collect(Collectors.toList());
   ```
2. There are 4 types of method reference:
    1. Instance method reference. Reference to parameter object's method
    2. Other object's method reference. Reference to another instance's method.
       For example, `System.out::println`
    3. Static method reference. For example, `Arrays::asList`
    4. Constructor reference. Used to create new object using no-arg constructor. 
       For example, `HashMap::new`