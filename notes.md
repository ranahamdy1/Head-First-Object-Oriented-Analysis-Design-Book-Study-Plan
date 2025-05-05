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
