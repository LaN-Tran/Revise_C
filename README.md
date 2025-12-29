# Learning C 

## Setup the environment to run and compile c/c++ code with VSC, windows

- For windows 11, VSC

  - Following all the steps in https://code.visualstudio.com/docs/cpp/config-mingw

  - To run build/link/compile C/C++ code without depending on the VSC environment, but use the Terminal, open the `command prompt` in VSC, then follow the instructions from **Reference - learning C material** (see below). If there is any troubles, see the section **trouble shooting**. 

- Trouble shooting

  1. `gcc` command can not be run from `cmd` (command prompt of windows). The error is

```
Compiling eror: The procedure entry point clock_gettime64 could not be located in the dynamic link library C:\msys64\mingw64\bin..\lib\gcc\x86_w64-minggw32\15.1.0\cc1plus.exe
```
 
   The solution: https://www.reddit.com/r/learnprogramming/comments/1lytphg/compiling_eror_the_procedure_entry_point_clock/

     - Move the `path to urct64` in the `PATH` variable up until the error is solved.
  

  2. `gcc -o hello hello.c` does not produce output file `hello.exe` when executed in `cmd` opened in vsc:

   - step 1: add the `path to urct64` to `System` - `PATH`, and make sure the path is ordered at the very top (referred to **trouble shooting - 1. above**) [ref](https://www.google.com/search?client=opera&q=why+gcc+command+can+be+executed+in+cmd+but+git+bash+in+vsc+can+not&sourceid=opera&ie=UTF-8&oe=UTF-8#fpstate=ive&vld=cid:4852da0b,vid:DDeFWwW_BYQ,st:87)

   - step 2: reload the vsc windows after step 1 [ref](https://stackoverflow.com/questions/67284061/gcc-running-in-cmd-but-not-in-visual-studio-code)
  
  3. `gcc -o hello hello.c` does not produce output file `hello.exe` when executed in `git bash` opened in vsc/ independently 
    
    - downgrade installed git bash [ref](https://github.com/doctest/doctest/issues/392)

    - But if the git bash already installed and setup probably in VSC, the faster solution is to not use bash to build/link/compile C code. Use `command prompt` to build/link/compile C code in VSC, use `git bash` only for managing.


# Reference

- Learning C material: https://beej.us/guide/bgc/html/split/hello-world.html

