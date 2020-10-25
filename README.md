# Refactoring

## PA1-Bouncyyahomie
From Bouncyyahomie's https://github.com/OOP2020/pa1-Bouncyyahomie

### cursor() Method
In the `ku/util/ArrayIteratir.java` class
From this https://github.com/OOP2020/pa1-Bouncyyahomie/blob/master/ku/util/ArrayIterator.java

consider this code: 
```java
      public int cursor() {
        return cursor += 1;
    }

    /**
     * @see java.util.Iterator#next()
     */
    @Override
    public T next() {
        if (hasNext() == false)
            throw new NoSuchElementException("No more elements");
        else
            cursor();
            return array[cursor - 1];
    }
```

* Refactoring Sign:

  * Weird code don't need to extract method
  
* Refactoring: delete cursur() method and just put cursor += 1 in next() method.

```java
      /**
     * @see java.util.Iterator#next()
     */
    @Override
    public T next() {
        if (hasNext() == false)
            throw new NoSuchElementException("No more elements");
        else
            cursor += 1;
            return array[cursor - 1];
    }
```
  
 
