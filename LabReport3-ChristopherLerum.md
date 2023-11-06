<h1>Lab Report 3 - Bugs and Commands -Christopher Lerum</h1>
<h3>Part 1</h3>

A failure-inducing input for the buggy program, as a JUnit test and any associated code

    import static org.junit.Assert.*;
    import org.junit.*;
  
    public class myArrayTests {
        @Test
        public void test1ReverseInPlace() {C:\Users\Jonathanl\Documents\GitHub\lab3\ArrayExamples.java
            int[] input1 = { 1,2,3 };
            ArrayExamples.reverseInPlace(input1);
            assertArrayEquals(new int[]{ 3,2,1 }, input1);
        }
    }

An input that doesn’t induce a failure, as a JUnit test and any associated code

    public class myArrayTests {
        @Test
        public void test2ReverseInPlace() {
            int[] input1 = { 1 };
            ArrayExamples.reverseInPlace(input1);
            assertArrayEquals(new int[]{ 1 }, input1);
        }
    }
    
The symptom, as the output of running the tests
![image](lreport3.PNG)

The bug, as the before-and-after code change required to fix it
before
    
    public class ArrayExamples {

    // Changes the input array to be in reversed order
      static void reverseInPlace(int[] arr) {
        for(int i = 0; i < arr.length; i += 1) {
          arr[i] = arr[arr.length - i - 1];
        }
      }
    }
after

    public class ArrayExamples {

    // Changes the input array to be in reversed order
      static void reverseInPlace(int[] arr) {
        int temp = 0; 
        for(int i = 0; i < arr.length/2; i += 1) {
          temp = arr[i];
          arr[i] = arr[arr.length - i - 1];
          arr[arr.length - i - 1] = temp;
        }
      }
    }
    
In order to fix reverseInPlace, you need to change the for loop to properly swap elements in the array to reverse the order. A temp variable should be used to properly store one of the elements during the swap.

