# AP-Assignment-4
Create a JUnit test suite that runs multiple test classes together.

TestClass1.java
import org.junit.jupiter.api.Test;
import static org.junit.jupiter.api.Assertions.assertEquals;

public class TestClass1 {
    @Test
    void testOne() {
        assertEquals(2, 1 + 1);
    }
}
TestClass2.java
import org.junit.jupiter.api.Test;
import static org.junit.jupiter.api.Assertions.assertTrue;

public class TestClass2 {
    @Test
    void testTwo() {
        assertTrue(5 > 3);
    }
}
TestSuite.java
import org.junit.platform.suite.api.SelectClasses;
import org.junit.platform.suite.api.Suite;

@Suite
@SelectClasses({
    TestClass1.class,
    TestClass2.class
})
public class TestSuite {
    // This class is used only to group tests
}
