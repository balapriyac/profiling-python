  ```
  # using cProfile in the script
  0
  ...
  999
  Slept for 20 seconds
  
  #profiing output

         1008 function calls in 20.024 seconds

   Random listing order was used

   ncalls  tottime  percall  cumtime  percall filename:lineno(function)
        1    0.000    0.000    0.000    0.000 {method 'index' of 'list' objects}
     1001    0.005    0.000    0.005    0.000 {built-in method builtins.print}
        1   20.018   20.018   20.018   20.018 {built-in method time.sleep}
        1    0.000    0.000    0.000    0.000 /usr/lib/python3.10/cProfile.py:117(__exit__)
        1    0.000    0.000    0.005    0.005 /home/balapriya/profiling-python/main.py:5(func)
        1    0.000    0.000   20.018   20.018 /home/balapriya/profiling-python/main.py:10(another_func)
        1    0.000    0.000    0.000    0.000 /home/balapriya/profiling-python/main.py:15(useful_func)
        1    0.000    0.000    0.000    0.000 {method 'disable' of '_lsprof.Profiler' objects}
        
 # profiing output ordered by time  add to script: profile_result.sort_stats(pstats.SortKey.TIME)
         1008 function calls in 20.020 seconds

   Ordered by: internal time

   ncalls  tottime  percall  cumtime  percall filename:lineno(function)
        1   20.018   20.018   20.018   20.018 {built-in method time.sleep}
     1001    0.002    0.000    0.002    0.000 {built-in method builtins.print}
        1    0.000    0.000    0.002    0.002 /home/balapriya/profiling-python/main.py:5(func)
        1    0.000    0.000    0.000    0.000 /home/balapriya/profiling-python/main.py:15(useful_func)
        1    0.000    0.000   20.018   20.018 /home/balapriya/profiling-python/main.py:10(another_func)
        1    0.000    0.000    0.000    0.000 /usr/lib/python3.10/cProfile.py:117(__exit__)
        1    0.000    0.000    0.000    0.000 {method 'disable' of '_lsprof.Profiler' objects}
        1    0.000    0.000    0.000    0.000 {method 'index' of 'list' objects}

# output: run cprofile at the command line
# python3 -m cProfile main.py
         1009 function calls in 20.021 seconds

   Ordered by: standard name

   ncalls  tottime  percall  cumtime  percall filename:lineno(function)
        1    0.000    0.000   20.021   20.021 main.py:1(<module>)
        1    0.000    0.000    0.000    0.000 main.py:14(useful_func)
        1    0.000    0.000    0.002    0.002 main.py:4(func)
        1    0.000    0.000   20.019   20.019 main.py:9(another_func)
        1    0.000    0.000   20.021   20.021 {built-in method builtins.exec}
     1001    0.002    0.000    0.002    0.000 {built-in method builtins.print}

```

![image](https://github.com/balapriyac/profiling-python/assets/47279635/43c13a2a-df5c-47e0-b3eb-2999299245d1)
![image](https://github.com/balapriyac/profiling-python/assets/47279635/ec42a058-6895-4e30-a6f3-e9d3d211cda1)
![image](https://github.com/balapriyac/profiling-python/assets/47279635/fbf10352-cf28-4c6d-bc07-12b58dd4b55d)



        1   20.019   20.019   20.019   20.019 {built-in method time.sleep}
        1    0.000    0.000    0.000    0.000 {method 'disable' of '_lsprof.Profiler' objects}
        1    0.000    0.000    0.000    0.000 {method 'index' of 'list' objects}

