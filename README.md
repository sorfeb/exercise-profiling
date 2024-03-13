# JMeter before and after profiling SCREENSHOTS:
`/all-student`
## Before
![all-student test plan](https://github.com/sorfeb/exercise-profiling/assets/112263712/d5681de0-61a2-4a80-bcf4-24ae7992b0f7)
## After
![all-student test plan_after](https://github.com/sorfeb/exercise-profiling/assets/112263712/d304939e-d2d5-4311-8396-977deb90c713)

`/all-student-name`
## Before
![all-student-name test plan](https://github.com/sorfeb/exercise-profiling/assets/112263712/5d2fcb6d-2d17-4c9d-8906-361a7d59441d)
## After
![all-student-name test plan_after](https://github.com/sorfeb/exercise-profiling/assets/112263712/31d5620f-0c1d-4e60-834f-b1572c724a0e)

`/highest-gpa`
## Before
![highest-gpa test plan](https://github.com/sorfeb/exercise-profiling/assets/112263712/5bef4bb8-8012-4343-80f1-991984c150ba)
## After
![highest-gpa test plan_after](https://github.com/sorfeb/exercise-profiling/assets/112263712/251c92f8-9b5f-4ea3-bf7d-00ef1417e1fb)

As you can see in the `Sample Time` value from every screenshots, Every endpoint's "After" screenshot has significantly less `Sample Time` values compared to "Before". This tells us that the profiling and optimization worked, resulting more efficient runtime.  

# JMeter CLI Test results SCREENSHOTS:
`/all-student`
![all-student test plan_cmd](https://github.com/sorfeb/exercise-profiling/assets/112263712/5018a508-4725-4fc4-b8f4-a1bc806400f6)
`/all-student-name`
![all-student-name test plan_cmd](https://github.com/sorfeb/exercise-profiling/assets/112263712/0a521246-5d08-49b2-a8d1-86a8d1e6c900)
`/highest-gpa`
![highest-gpa test plan_cmd](https://github.com/sorfeb/exercise-profiling/assets/112263712/eb5cf235-765d-4119-bafa-367ea3e69ccb)

# Reflection
Please answer the following questions:
1. What is the difference between the approach of performance testing with JMeter and profiling with IntelliJ Profiler in the context of optimizing application performance?
   > `JMeter` is primarily used for **load testing** and **performance testing**. It simulates multiple users accessing the application simultaneously to measure its performance under various load conditions. JMeter provides information about how the application performs under different loads and helps identify performance bottlenecks such as slow database queries, inefficient algorithms, or resource contention issues by providing features for **creating test scenarios**, **defining virtual users**, and **configuring test parameters** (such as the n**umber of threads**, **ramp-up period**, and **loop count**).
   
   > On the other hand, `IntelliJ Profiler` is used for profiling Java applications to **identify performance bottlenecks**, **memory leaks**, and **CPU usage issues**. It provides detailed information about the execution of your application, including **method call traces**, **memory allocation**, **thread activity**, and **CPU usage**. IntelliJ Profiler allows to pinpoint specific areas of the codebase that causes to performance issues. It provides insights into methods consuming the **most CPU time**, **memory allocation patterns**, and **thread contention problems**.
   
2. How does the profiling process help you in identifying and understanding the weak points in your application?
   > It helped me to identify and understand weak points in the code by providing its **runtime behavior**, **resource usage**, and **performance characteristics**. From there, I am able to see which function or code block consumes the most time when ran. After that, I will optimize the code by making efficient algorithms and rerun everytime I refactor the code to check if the performance has improved or not. 
   
3. Do you think IntelliJ Profiler is effective in assisting you to analyze and identify bottlenecks in your application code?
   > Yes, because the GUI of the Profiler is integrated with the IDE, providing interactive information about runtime and usage of each function that has been ran by the application since the booting up process. The horizontal bar graphs of each representation of the runtime of each function proved helpful by making data visualisation easier.
   
4. What are the main challenges you face when conducting performance testing and profiling, and how do you overcome these challenges?
   > The main challenge was optimizing the code. I tried several attempts to optimize the code by changing the data structures used, algorithms, or changing language. The challenge in that is not knowing whether the refactorization of the code has been more effective than the former code or not. I overcame the challenges by searching the internet about optimizing codes similar to my case and implementing them to the application.
   
5. What are the main benefits you gain from using IntelliJ Profiler for profiling your application code?
   > I am able to easily see and estimate the efficiency and complexity of each functions from the fire graph. The ease of access to profiling in IntelliJ Profiler allows me to run the profiler multiple times quickly after each refactorization.

6. How do you handle situations where the results from profiling with IntelliJ Profiler are not entirely consistent with findings from performance testing using JMeter?
    > Actually the results of IntelliJ Profiler and JMeter aren't entirely differnt, instead the result show a somewhat similar findings. If there are incosistent findings, I will run each tester repeatedly and estimate the average findings from each IntelliJ Profiler and JMeter.
    
7. What strategies do you implement in optimizing application code after analyzing results from performance testing and profiling? How do you ensure the changes you make do not affect the application's functionality?
    > - I used `SQL queries` instead of for `loops` and `arrays` for collecting students
    > - Replaced `loops` and traditional `if-else` with `.stream()` to allow parallel data processing and reduce memory load
    >   I ensured the changes does not affect the application's functionality by reruninng profilings everytime I refactor my code and made sure it gave the same output as before optimization.

