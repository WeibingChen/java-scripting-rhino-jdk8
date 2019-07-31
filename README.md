# Using Rhino JSR-223 engine with JDK8
### TL;DR


You will find [prebuilt js.jar and js-engine.jar](https://github.com/zeroboo/javax-scripting/releases/tag/v1.0.0) in the release tab. You can put these two jars in your CLASSPATH. When creating script engine in your app, you need to use "rhino" as engine name.

Using Rhino jsr-223 engine from Java
```java
import javax.script.*;
 
public class Main {
    public static void main(String[] args) throws Exception {
        ScriptEngineManager m = new ScriptEngineManager();
        // specifically look for "rhino" engine
        ScriptEngine engine = m.getEngineByName("rhino");
        System.out.println(engine.eval("33 + 232"));
    }
}
```
compile above using
 
```javac Main.java```
 
run it using
 
```java -cp js-engine.jar:js.jar Main```


### Using Rhino JSR-223 engine with JDK8
[Link from openjdk.java](https://wiki.openjdk.java.net/display/Nashorn/Using+Rhino+JSR-223+engine+with+JDK8)

### javax-scripting
Mirror of the final state of the java.net scripting project (http://java.net/projects/Scripting)

### rhino engine

### build


