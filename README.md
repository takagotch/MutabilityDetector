### mutabilitydetector
---
https://github.com/MutabilityDetector/MutabilityDetector


```java
import static org.mutabilitydetector.unittesting.MutabilityAssert.assertImmutable;

@Test public void checkMyClassIsImmutable() {
  assertImmutable(MyClass.class);
}
```

```java
// src/test/java/org/mutabilitydetector/unittesting/clientusage/MutabilityAssertTest.java

public class MutabilityAssertTest {

  private final Class<?> immutableClass = ImmutableExample.class;
  private final Class<?> mutableClass = MutableByHavingPublicNonFinalField.class;
  
  private final String expectedError = String.format("%n" + 
    " None.");
  
  @Test
  public void assertImmutableWithImmutableClassDoesNotThrowsAssertionError() throws Exception {
    assertImmutable(immutableClass);
  }
  
  @Test(expected = MutabilityAssertionError.class)
  public void assertImmutableWithMutableClassThrowsAssertionError() throws Exception {
    assertImmutable(mutableClass);
  }
  
  
  
}
```

```
```


