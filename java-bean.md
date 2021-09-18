# Better Java Bean
When you think to write any Java classes that have been designed to store any values inside, you should think about following items. 

1. Any code that used for assign value(s) to bean object. You should consider to write at bean class first.
   * Reason - Bean class has been designed to store values so value assigning code should be considered to write it inside bean class itself first. If not, why you put value assigning code outside bean class that has been designed for assign values.

2. Any bean class must used at least Getter or Setter annotation of [Lombok](https://projectlombok.org/). Note!! If Lombok seems useless on that bean class. That's mean your bean class should not be considered to be bean class in practical.
   * Reason - Lombok is good library that help your bean class look cleaner. It hide yourget/set methods and you could focus on value assigning code more.

3. In any methods that assigns values in multiple fields at a bean object, it needs to convert that assigning into new method on bean class or bean builder/factory class.
