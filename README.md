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


### About using Rhino JSR-223 engine with JDK8
[Read post from openjdk.java](https://wiki.openjdk.java.net/display/Nashorn/Using+Rhino+JSR-223+engine+with+JDK8)

### About javax-scripting

When you go to java.net to get [scripting project](https://java.net/projects/Scripting), you will find it closed.
However, there are some mirror on github: https://github.com/scijava/javax-scripting
This fork is a mod to build JSR-223 engine with JDK8 guided by the post on openjdk.java.net

### rhino engine from mozilla
https://developer.mozilla.org/en-US/docs/Mozilla/Projects/Rhino


### build


