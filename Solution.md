# Solution

1. *Compile and run BadThreads.java:*

* Done ✔

2. *The application should print out "Mares do eat oats."*

- *Is it guaranteed to always do this?*

**No, it is *likely* to happen, but not guaranteed.**

- *If not, why not?*

**The two key statements do not have a 'happens-before' relationship.**


3. *Would it help to change the parameters of the two invocations of Sleep?*

**No, this can increase the *likelyhood* of the execution occurring correctly, but still does not guarantee it.**

4. *How would you guarantee that all changes to message will be visible in the main thread?*

**Either invoke the `.join()` function on the thread instance before referring to the message variable, or encapsulate the variable in and object and access it via synchronized methods.**

*Please type your answers and submit.*

