# 3-Sets-Of-Gov-Limits-in-Test-Class

This technique demonstrates how to get 3 sets of governor limits in a test class.

```java
@isTest
private class ContactTriggerHandlerTest {
  @TestSetup
  static void makeData() {
    // governor limit set 1

    Test.startTest();

    // governor limit set 2

    Test.stopTest();

    // governor limit set 1 resumes
  }

  @isTest
  static void myTestMethod1() {
    // governor limit set 1 resumes

    Test.startTest();

    // governor limit set 3

    Test.stopTest();

    // governor limit set 1 resumes
  }
}
```
