# Code Representation Comparison

## Java Code

```java
package com.example;
import org.springframework.stereotype.Controller;

import java.util.List;

@Controller
public class Example<T> implements MyInterface {
    private int field;

    static {
        System.out.println("Static initialization");
    }

    {
        System.out.println("Instance initialization");
    }

    public Example(int field) {
        this.field = field;
    }

    public <U> List<U> genericMethod(U value) {
        return List.of(value);
    }

    public void exampleMethod() throws Exception {
        int localVariable = 10;
        if (localVariable > 5) {
            System.out.println("Local variable is greater than 5");
        }
        try {
        } catch (Exception e) {
            e.printStackTrace();
        } finally {
        }
        for (int i = 0; i < 5; i++) {
            System.out.println(i);
        }
        while (localVariable > 0) {
            localVariable--;
        }
        do {
            System.out.println("Do-while loop");
        } while (false);
        switch (localVariable) {
            case 0:
                System.out.println("Local variable is 0");
                break;
            default:
                System.out.println("Default case");
        }
        List.of(1,2,3).forEach(System.out::println);
    }

    public enum InnerEnum {
        VALUE1, VALUE2
    }

    public interface InnerInterface {
        void innerMethod();
    }

    public class InnerClass {
        public void innerClassMethod() {}
    }

    @FunctionalInterface
    public interface MyFunctionalInterface {
        void myMethod();
    }
}

interface AnotherInterface {}

class AnotherClass {}
