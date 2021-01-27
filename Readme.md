1. Compile and run BadThreads.java:



```java

public class BadThreads {



    static String message;



    private static class CorrectorThread

        extends Thread {



        public void run() {

            try {

                sleep(1000); 

            } catch (InterruptedException e) {}

            // Key statement 1:

            message = "Mares do eat oats."; 

        }

    }



    public static void main(String args[])

        throws InterruptedException {



        (new CorrectorThread()).start();

        message = "Mares do not eat oats.";

        Thread.sleep(2000);

        // Key statement 2:

        System.out.println(message);

    }

}

```



2. The application should print out "Mares do eat oats."

- Is it guaranteed to always do this?

- If not, why not?



3. Would it help to change the parameters of the two invocations of Sleep?



4. How would you guarantee that all changes to message will be visible in the main thread?



Please type your answers and submit. 