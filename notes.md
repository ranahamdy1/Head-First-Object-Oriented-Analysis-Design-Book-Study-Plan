## What is object ?
- object is anything in the world like person, pen , tree .....
- object composed of : 1-Data  2-Operation()
## What is Class ?
بحدد حاجه والكل بيمشي عليها
## What is inheritance ?
That’s when one class inherits behavior from another class, and can then change that behavior if needed. 

> super: is a special keyword. It refers to the class that this class has inherited behavior from.

## What is Polymorphism ?
Polymorphism is closely related to inheritance. When one class inherits from another, then polymorphism allows a subclass to stand in for the superclass

## What is Encapsulation ?
Encapsulation is when you protect information in your code from being used incorrectly.

> ## 📌 what does loosely coupled mean ?
- Loosely coupled is when the objects in your application each have a specific job to do, and they do only that job. So the functionality of your app is spread out over lots of well-defined objects, which each do a single task really well.

> ## 📌Anonymous Class
- هو نوع خاص من Inner Class.
- ليس له اسم.
- يتم تعريفه وإنشاء كائن منه في نفس الوقت.
- غالبًا يُستخدم لتنفيذ interface أو كلاس مجرد
  
EX:

```
interface Greeting {
    void sayHello();
}

public class Main {
    public static void main(String[] args) {
        Greeting greeting = new Greeting() {
            @Override
            public void sayHello() {
                System.out.println("Hello from anonymous class!");
            }
        };

        greeting.sayHello();
    }
}
```
- 🔁 لو حبينا نكتب نفس الكود بكلاس "عادي" له اسم، كان هيكون كده:
```
class GreetingImpl implements Greeting {
    @Override
    public void sayHello() {
        System.out.println("Hello from named class!");
    }
}

public class Main {
    public static void main(String[] args) {
        Greeting greeting = new GreetingImpl();
        greeting.sayHello();
    }
}
```
