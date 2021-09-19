# Better Java Bean
When you think to write any Java classes (bean) that have been designed to store any values inside, you should think about following items.

1. Any code that used for assign value(s) to be an object. You should consider writing at bean class first.
   * The reason - bean class has been designed to store values so value assigning code should be considered to write it in the bean class itself first. As you could gather the assigning knowledge in bean class, it will be beneficial to refactoring in the future.

2. Any bean class must use at least Getter or Setter annotation of [Lombok](https://projectlombok.org/). Note!! If Lombok seems useless on that bean class. That's mean your bean class should not be considered to be a bean class in practical.
   * The reason - Lombok is good library that help your bean class look cleaner. It hide yourget/set methods and you could focus on value assigning code more.

3. In any methods that assigns values in multiple fields of a bean object, it needs to convert that assigning into a new method on a bean class, or bean builder class, or factory class, or converter class.
   * The reason - code will be easy to understand on intention to make any changes on bean object.
