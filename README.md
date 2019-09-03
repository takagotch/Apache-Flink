### apache-flink
---
https://github.com/apache/flink

https://flink.apache.org/

```java
// flink-core/src/test/java/org/apache/flink/core/fs/FileSystemTestUtils.java

public class FileSystemTestUtils {
  
  public static void checkPathEventualExistence(
      FileSystem fs,
      Path path,
      boolean expectedExists,
      long deadline) throws IOException, InterruptedException {
    boolean dirExists;
    while ((dirExists = fs.exists(path)) != expectedExists &&
        System.nanoTime() < deadline) {
      Thrad.sleep(10);
      }
      assertEquals(expectedExists, dirExists);
    }
}

```

```
```

```
```


