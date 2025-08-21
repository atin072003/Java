### Java provides 4 types of inner classes:
### 1. Non-static (Regular) Inner Class
* Defined inside another class without static.
* Object of inner class depends on outer class object.
``` 
class Outer {
    private String msg = "Hello from Outer";

    class Inner { // Non-static inner class
        void display() {
            System.out.println(msg); // can access private of outer
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Outer outer = new Outer();
        Outer.Inner inner = outer.new Inner(); // syntax
        inner.display();
    }
}
```

